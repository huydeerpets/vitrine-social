Issues and Progress
The control of the tasks and the progress of the tasks are being done in the Waffle. Click here to follow: https://waffle.io/Coderockr/vitrine-social

Installation Backend (Go)
We are using Go Modules in this project, so the project folder needs to be outside of yours GOPATH, or you will have to add the ENV GO111MODULElike onin your environment for the project to work inside GOPATH.

We recommend keeping the project out of yours GOPATH, so goit will not generate an unneeded module at the root of the project, or affect other projects goin your environment that you are not yet using Go Modules.

Summary of the opera, to start work just run the following commands:

git clone git@github.com: Coderockr / vitrine-social.git / not / your / go / path / vitrine-social ;

make setup # run the first time to install all dependencies and tools

make migrations # this may fail because of postgres warmup

make serve # is now running :)
Local Domains and Subdomains
Including the following domains in your /etc/hostsshould expedite the setup of your project:

127.0.0.1 api.vitrinesocial.test # use port 8000 (golang) 
127.0.0.1 images.vitrinesocial.test # use port 7000 (images-server) 
127.0.0.1 minio.vitrinesocial.test # use port 9000 (minio) 
127.0.0.1 vitrinesocial.test # use port 3000 (frontend)
Installation Frontend (React)
cd frontend

yarn

yarn start
Reicons
Move icons to assets / icons

yarn reicons
Auxiliary Commands (day-to-day)
We are keeping all the helper commands (create migration, run migrations, regenerate docs, etc) within Makefilethe project root.

To see what commands are available, run: make helpand all will be listed.

API Documentation
To access the latest version of the definition go to:

http://coderockr.com/vitrine-social/

How to update the documentation?

Contributing
Read our CONTRIBUTING.md to learn about our development process, how to propose bugfixes and improvements, and how to find issues to act on.
