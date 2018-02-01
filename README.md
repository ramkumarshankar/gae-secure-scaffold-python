# Secure GAE Scaffold

Forked from the 'official' google [repo](https://github.com/google/gae-secure-scaffold-python)

No major changes, just a few minor simplifications for our project needs:  
- Remove closure compiler as a submodule, use the latest compiled jar instead available at (<https://dl.google.com/closure-compiler/compiler-latest.zip>)  
- Temporary fix (needs a bit more work) for java version detection in `jscompiler.py` in closure-library  
- Updated grunt jobs to use update closure compiler jar file

I might simplify this further by removing dependencies we do not need (such as closure templates, and add some watch jobs to speed up local development.

## Getting started

The steps are mostly the same, with one fewer step. You do not have to build the closure compiler. Here they are from the original project readme:

1.  `git submodule init`
2.  `git submodule update`
3.  `cd ../closure-templates && mvn && cd ..`
4.  `npm install`
5.  `mkdir $HOME/bin; cd $HOME/bin`
6.  `npm install grunt-cli`
    * Alternatively, `sudo npm install -g grunt-cli` will install system-wide
      and you may skip the next step.
7.  `export PATH=$HOME/bin/node_modules/grunt-cli/bin:$PATH`
    * It is advisable to add this to login profile scripts (.bashrc, etc.).
8.  Visit <https://cloud.google.com/appengine/docs/python/download>, and choose
    the alternative option to "download the original App Engine SDK for Python."
    Choose the "Linux" platform (even if you use OS X).  Unzip the file, such
    that $HOME/bin/google_appengine/ is populated with the contents of the .zip.

Please refer to the [original readme](https://github.com/google/gae-secure-scaffold-python/blob/master/README.md) for more detailed information.
