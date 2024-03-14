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
* The main working directory is 

#### Integration with VSCode
* In order to do any of the following you must have the Docker desktop app open and be signed in.
* The Dev Container is able to be run within a VSCode remote connection. In order to do this navigate to the Docker file contained [here](../.devcontainer/Dockerfile). Once you have this open find the small blue rectangle in the bottom right of your screen. When you hover over it it should be labeled *Open a Remote Connection*. Click on this and reopen the file as a container. Once in the container you may use VSCode's built in terminal to navigate through the container.
* Already set up are several quality of life extensions designed to make editing the docker file and the devcontainer.json files easier. These extensions add the highlighting to code that is being written in flutter, docker, and json files.

#### Usage
* So far the DevContainer has been extremely useful in working on code across multiple computers. The container allows code to be tested and written without worrying if the computer that is being used has the correct dependencies installed. In order to edit code in the conttainer, you can navigate to the file you are editing through the terminal built in to VSCode.

#### Issues
* Android SDK licensing: I had a lot of trouble getting the android sdk to install and in order to actually get it working I ended up having to find the license key and manually insert it into a text file. I'm sure there is a better solution but I haven't had time to find it yet. 
* As of now the container is a little bit hard to navigate and I am still trying to get used to it. Additionally I am still getting used to Github so I'm fighting on two fronts. While it is difficult the benefits are already apparent and I am excited to learn everything I need to.
#### Conclusion
* This container is extremely useful to making flutter apps across different computers and making sure they work on all of the systems I would like to deploy to. It isn't perfect yet, but I will work on making changes where they are necessary as I find flaws.