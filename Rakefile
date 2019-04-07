require 'rake/clean'
CLOBBER << 'output'

CLEAN << 'content/images/knitr'
CLEAN << 'content/images/pnp'

rrst_files = Rake::FileList["**/*.Rrst"]
rst_derivatives = rrst_files.ext(".rst").existing
CLEAN << rst_derivatives

rule ".rst" => ".Rrst" do |t|
    sh "Rscript -e 'knitr::knit(\"#{t.source}\", \"#{t.name}\", encoding=\"UTF-8\")'"
end

desc "Build website"
task :default => rrst_files.ext(".rst")
task :default do
    sh "pelican -o output -s pelicanconf.py content"
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
    sh "pelican -o output -s pelicanconf.py --relative-urls content"
    Dir.chdir("output") do
        sh "python3 -m http.server"
    end
end

