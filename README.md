# apptainer containers

## exercise

### assigment

Create a custom container
- Base Image: Alpine Linux
- Install: Node.js and NPM
- Include: A simple Node.js application
- Define: Environment variable for the app port
- Write: Custom runscript to start the application

### solution

exercise.def
- run container with
```
sudo apptainer exec --net --network-args "portmap=3000:3000/tcp" exercise.sif node /bin/server.js
```
