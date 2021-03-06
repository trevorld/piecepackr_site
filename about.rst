.. include:: links.rst

This is the associated website for the piecepackr_, ppgames_, piecenikr_, and tradgames_ R_ packages.  piecepackr_ is an R package designed to make configurable board game graphics. It can be used with the grid_, rayrender_, and rgl_ graphic systems to make board game diagrams_, board game animations_, and custom `Print & Play`_ layouts.  By default it is configured to make `piecepack game`_ diagrams_, animations_, and `Print & Play`_ layouts but can be configured to make graphics for `other game systems`_.  ppgames_ is an R_ package with functions for generating piecepack_ game graphics, rulesets, and books as well as functions to parse and visualize games recorded using "`Portable Piecepack Notation`_" format plus a Fuji-san solver.  piecenikr_ contains functions for visualizing `Looney Pyramids`_ games while tradgames_ contains functions for visualizing games played with traditional game systems (such as checkers sets).

This website contains several articles of documentation_ on how to use these R_ packages as well as some relevant theory and resources plus several demos_ of the software in action.  It also contains the download links for several `Print & Play`_ pdfs of the piecepacks configured in the `Print & Play demos`_ that can be used to build your own piecepack_.  Here is a "Site Map" of the articles on this site:

.. contents:: Site Map

Docs
----

These are in depth articles on specific subjects of interest to piecepackr_ users and/or piecepack_ designers including documentation_ of some of the key piecepackr_ and ppgames_ features:

#. `Intro to piecepackr's API <{filename}/Docs/intro.rst>`_
#. `Configuration lists`_
#. `Custom grob functions`_
#. `Animations`_
#. `3D projections <{filename}/Docs/projections.rst>`_
#. `Portable Piecepack Notation <{filename}/Docs/ppn.rst>`_
#. `Unicode piecepack symbols <{filename}/Docs/unicode_symbols.rst>`_
#. `Unicode piecepack diagrams <{filename}/Docs/unicode_diagrams.rst>`_
#. `Game starting arrangement functions <{filename}/Docs/game_starts.rst>`_
#. `Essential information sets of a piecepack <{filename}/Docs/essential.rst>`_
#. `Licenses FAQ <{filename}/Docs/licenses.rst>`_

Also consider looking at each of the R packages built-in documentation:

.. list-table:: Links to pretty html rendering of R packages' built-in documentation
   :header-rows: 1

   * - Package
     - Type
   * - piecepackr_
     - `development <https://trevorldavis.com/R/piecepackr/dev>`__, `release <https://trevorldavis.com/R/piecepackr>`__
   * - ppgames_
     - `development <https://trevorldavis.com/R/ppgames/dev>`__, `preview <https://trevorldavis.com/R/ppgames>`__
   * - piecenikr_
     - `development <https://trevorldavis.com/R/piecenikr/dev>`__, `preview <https://trevorldavis.com/R/piecenikr>`__
   * - tradgames_
     - `development <https://trevorldavis.com/R/tradgames/dev>`__, `preview <https://trevorldavis.com/R/tradgames>`__

Demos
-----

Print-and-Play Demos
~~~~~~~~~~~~~~~~~~~~

These are the `Print & Play demos`_ which demonstrate the code used to generate the `Print & Play`_ pdfs found on this site:

#. `piecepackr's default piecepack <{filename}/Demos/default_pnp.rst>`_
#. `Dual piecepacks`_
#. `"Orthodox" (Anatomy of a Piecepack Standard) piecepack <{filename}/Demos/orthodox_pnp.rst>`_
#. `Daniel Ajoy's Dingbats suited piecepack <{filename}/Demos/dingbats_pnp.rst>`_
#. `Rainbow Deck suited piecepack <{filename}/Demos/default_pnp.rst>`_
#. `Chinese Zodiac ranked piecepack <{filename}/Demos/zodiac_cn_pnp.rst>`_
#. `Chess-ranked piecepacks <{filename}/Demos/chess_pnp.rst>`_
#. `Reversi-friendly piecepack <{filename}/Demos/reversi_pnp.rst>`_

Visualizations for Specific Piecepack Games
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

These are demonstrations of using piecepackr_ and ppgames_ to make visualizations for specific `piecepack games <{tag}ppgames>`__:

#. `Backgammon <{filename}/Demos/backgammon_game.rst>`_
#. Several `chess <{filename}/Demos/chess_pnp.rst>`_ variants
#. `Cribbage <{filename}/Demos/cribbage_game.rst>`_
#. `Everest <{filename}/Demos/everest_game.rst>`_
#. `Relativity <{filename}/Demos/relativity_game.rst>`_ (featuring a rank-colored piecepack)
#. `Tablut <{filename}/Demos/tablut_game.rst>`_
#. `Triactor <{filename}/Demos/jcd.rst>`_ (featuring the JCD piecepack)

Other Game Systems
~~~~~~~~~~~~~~~~~~

These are demonstrations of using piecepackr_ to make diagrams for `other game systems`_ besides the piecepack_.

#. `Checkers <{filename}/Demos/checkers.rst>`_
#. `Dominoes and standard 6-sided dice <{filename}/Demos/dominoes.rst>`_
#. `Go <{filename}/Demos/go.rst>`_
#. `Hexpack <{filename}/Demos/hexpack.rst>`_
#. `Looney Pyramids <{filename}/Demos/looney_pyramids.rst>`__
#. `Tak <{filename}/Demos/tak.rst>`_

Integrating with other piecepack art assets
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Miscellaneous demonstrations to interact with outside piecepack art assets

#. `Generating alternative textures for James H. Vipond's piecepack components <{filename}/Demos/vipond_textures.rst>`_
#. `Triactor <{filename}/Demos/jcd.rst>`_ shows how to make a configuration using the images contained in the piecepack VASSAL module
