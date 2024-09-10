# apptainer containers

There are only `name.def files`, these needs to be built with `apptainer build path/name.sif path/to/name.def`.

## exercise

### assigments

1. Create a custom container
   - Base Image: Alpine Linux
   - Install: Node.js and NPM
   - Include: A simple Node.js application
   - Define: Environment variable for the app port
   - Write: Custom runscript to start the application

### solutions

1. exercise.def
   - ~~running container with `sudo apptainer exec --net --network-args "portmap=3000:3000/tcp" exercise.sif node /bin/server.js` gives me access to `http://localhost:3000` from a browser (container is running in ubuntu server 22.04.4 running at virtualbox under windows 11, had to setup port forwarding in virtual box)~~
   - runnnig container with `apptainer exec exercise.sif /bin/server.js` seems to work too. Accessible at `http://localhost:3000`

## others
- first.def
  - simple container based on ubuntu 20.04 with sl executable, run with `apptainer exec first.sif /bin/games/sl`
- second.def
  - same as first.def but with `%runscript`, run with `apptainer run second.sif`
- htop.def
  - simple container based on ubuntu 20.04 with htop installed