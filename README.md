Operating Systems / System Architecture tutorial
================================================

Public repository for my 2013/2014 Operating Systems / System Architecture tutorial at the Karlsruhe Institute of Technology (KIT).


Get The Slides
--------------

 * Online: [http://osdev.trvx.org](http://osdev.trvx.org)
 * Local: Open index.html in your browser (opt. invoke "make local")


Building the slides
-------------------

Note: The build directory already contains the latest slides.

Jinja2 is used to simplify the build process.
Reveal.js is included as a git submodule, so you have to clone the repository recursively.

    git clone --recursive --branch gh-pages git://github.com/daniel-j-h/kit-tut-osdev.git
    cd kit-tut-osdev/slides
    make


Adding new slides
-----------------

All slides should extend from slide.tmpl and override the slides block.
Add your new .html file to the slides directory, metadata to the .json file, and re-run the commands above.
