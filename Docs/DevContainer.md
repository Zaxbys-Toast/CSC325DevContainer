## Dev Container Environment
#### What is a Dev Container? 
* A dev container is a shell which runs an operating system that can be accessed using any device capable of running that operating system. 
* In this case any computer that has **Docker** installed will be able to run this dev container, ensuring that the developement environment is the same across all machines working on it. This eliminates the *it works on my machine* issue.

#### Configuration 
* This container runs on **Ubuntu Latest**
* Contains the following packages
    * wget 
    * curl 
    * git 
    * unzip 
    * xz-utils 
    * zip 
    * libglu1-mesa 
    * openjdk-8-jdk 
    * wget 
    * clang 
    * cmake 
    * ninja-build 
    * pkg-config 
    * libgtk-3-dev 
    * liblzma-dev 
    * libstdc++-12-dev
* These include all of the necessary dependencies for creating a flutter web app as well as running the Android-SDK

#### Integration with VSCode