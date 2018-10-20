# funeos
fun with EOS



## Build

This command tells Meson to get ready to build our app using the prefix "/usr" and that we want to build our app in a clean directory called "build". The meson command defaults to installing our app locally, but we want to install our app for all users on the computer.

````
meson build --prefix=/usr
````

Change into the build directory and use ninja to build. Then, if the build is successful, install with sudo ninja install:

````
cd build
ninja
sudo ninja install
````

### i18n

* "POTFILES" that will contain paths to all of the files you want to translate
* "LINGUAS" should contain the two-letter language codes for all languages you want to provide translations for

Remember that each time you add new translatable strings or change old ones, you should regenerate your .pot and po files using the -pot and -update-po build targets from the previous two steps. 
If you want to support more languages, just list them in the LINGUAS file and generate the new po file with the -update-po target. 

Depuis "build"
````
ninja com.github.svan001.funeos-pot
ninja com.github.svan001.funeos-update-po
````
