# nvidia-jetpack
Base aarch64 container with Nvidia JetPack (4.2.2, 4.3.0, etc) for testing and running on Xavier AGX (and with small mods on other Nvidia Jetson devices)


# Using JetPack 4.2.2
Dockerfile.jp4.2.2 is preconfigured for Xavier AGX. If you want to build a base container for a different Jetson product you have to pass a build argument to the docker build command. The name of the argument is `XAVIER_PRODUCT_CODE`. For Xavier AGX the code is P2888. [Here you can find the module numbers of other devices](https://docs.nvidia.com/jetson/l4t/index.html).
To make it simple:
* P3448 - Jetson Nano 
* P2888 - Jetson AGX Xavier 
* P3310 - Jetson TX2 
* P3489 - Jetson TX2i 

# Using JetPack 4.3.0
To use JetPack 4.3.0 you have to install, compared to 4.2.2 which downloads automagically during the build process from the Internet, the Nvidia SDK Manager on a Linux x86 machine and download the JetPack. The you need to copy a bunch (or all of them) of debian packages to the jetpack4.3/ directory from where they will be copied into the container and installed there.
