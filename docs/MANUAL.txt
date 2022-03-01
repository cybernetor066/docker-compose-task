Connect to the Computer (Linux Machine) with Docker installation fully present.

npm install installs dependencies into the node_modules/ directory, for the node project you're working on. You can call install on another node.js project (module), to install it as a dependency for your project.

npm run build does nothing unless you specify what "build" does in your package.json file. It lets you perform any necessary building/prep tasks for your project, prior to it being used in another project.

npm build is an internal command and is called by link and install commands, according to the documentation for build: https://docs.npmjs.com/cli/build

This is the plumbing command called by npm link and npm install.

You will not be calling npm build normally as it is used internally to build native C/C++ Node addons using node-gyp.







# To test the app
# curl -i localhost:8000






# Development commands:
# DOCKER
sudo docker build -t cybernetor066/node-web-app:v1.0 .
sudo docker run -d --name node_web_server -p 8000:8000 cybernetor066/node-web-app:v1.0
sudo docker container exec -it node_web_server sh
sudo docker container ls
sudo docker container stop node_web_server
sudo docker container prune -f && sudo docker image prune -f


# Docker Compose
# cd into the scripts folder and enter this command
sudo docker-compose up
sudo docker container ls
sudo docker container ls -a
sudo docker container prune -f && sudo docker image prune -f
sudo docker container exec -it scripts_node_1 sh

sudo docker-compose down
curl -i localhost:8000





























