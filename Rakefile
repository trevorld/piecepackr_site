require 'rake/clean'
CLOBBER << 'output'

CLEAN << 'content/images/knitr'
CLEAN << 'content/share/pnp'
CLEAN << 'content/share/rules'

rrst_files = Rake::FileList["content/**/*.Rrst"]
rst_derivatives = rrst_files.ext(".rst").existing
CLEAN << rst_derivatives
CLEAN << Rake::FileList["**/*.RData"].existing

if ENV.has_key?("debug") # rake debug=
    debug_str = " --debug"
else
    debug_str = ""
end

rule ".rst" => ".Rrst" do |t|
    sh "Rscript -e 'knitr::knit(\"#{t.source}\", \"#{t.name}\", encoding=\"UTF-8\")'"
end

file 'content/pages/pnp.rst' => 'content/share/demo_cfgs.RData'
file 'content/share/demo_cfgs.RData' => 'content/Docs/animations.rst'
file 'content/Docs/animations.rst' => Rake::FileList["content/Demos/*.Rrst"]

desc "Build website"
task :default => rrst_files.ext(".rst")
task :default do
    sh "pelican -o output -s pelicanconf.py content" + debug_str
end

desc "Deploy website to trevor.l.davis.com/piecepackr"
task :deploy => :default
task :deploy do
    do_dry_run = ENV.has_key?("dry_run") # rake deploy dry_run=
    cmd = "rsync -avh --delete output/ trevorldavis.com:public_html/piecepackr/"
    if do_dry_run
        cmd = cmd + " --dry-run"
    end
    sh cmd
end

desc "Test website on localhost:8000"
task :test => rrst_files.ext(".rst")
task :test do
    sh "pelican -o output -s pelicanconf.py --relative-urls content" + debug_str
    Dir.chdir("output") do
        sh "python3 -m http.server"
    end
end

