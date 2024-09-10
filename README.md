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
- ~~running container with~~ `sudo apptainer exec --net --network-args "portmap=3000:3000/tcp" exercise.sif node /bin/server.js` ~~gives me access to http://localhost:3000 from a browser (container is running in ubuntu server 22.04.4 running at virtualbox under windows 11, had to setup port forwarding in virtual box)~~
- runnnig container with `apptainer exec exercise.sif /bin/server.js` seems to work too
