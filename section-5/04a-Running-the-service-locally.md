# Steps involved: 

1. `java --version` - To check if java is installed
2. `sudo apt install openjdk-21-jre-headless`. Openjdk 21 is used since readme file of ad service mentions that at least jdk17 is needed. You have an option to either install 17 or 21. Go with the higher version.
3. `./gradlew` - Execute to check if you have permission to execute gradle wrapper. Alternatively, check permissions and see if the execute bit is set.
4. If execute bit is not set, use chmod +x gradlew to add the permission.
5. `./gradlew installDist` - To build ad service. Starts gradle daemon. 
    
    Refer readme: https://github.com/Devops-projects-Sri/ultimate-devops-project-demo/tree/main/src/ad. 
    Follow the instructions to build the service. 
    A build directory should be created.

    How do you find which directory will be built? 

    For this project, dev has provided env variables to be added where it is mentioned where the build folder will be (./). 

    /home/ubuntu/ultimate-devops-project-demo/src/ad will be the destination.
    
    ```bash
        export AD_PORT=8080
        export FEATURE_FLAG_GRPC_SERVICE_ADDR=featureflagservice:50053
        ./build/install/opentelemetry-demo-ad/bin/Ad
    ```
6. If you list the provided file, it should show that the executable is created in the specified location and file. 
    ```bash
    ls ./build/install/opentelemetry-demo-ad/bin/Ad
    ```
    Note: A batch file is also created for windows machine in the /home/ubuntu/ultimate-devops-project-demo/src/ad folder.
7. Execute next step from readme. We are creating the env variables. 
   You can also change the port to something else. We are going to go with 9090.

    ```bash
        export AD_PORT=8080
        export FEATURE_FLAG_GRPC_SERVICE_ADDR=featureflagservice:50053
        ./build/install/opentelemetry-demo-ad/bin/Ad
    ```	
	Ad service should now be running.


