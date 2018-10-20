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
