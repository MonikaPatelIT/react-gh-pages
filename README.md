
### Deploying React app on GitHub pages 


In this tutorial, I'll show you how I deployed a React app—which I created using create-react-app—to GitHub Pages.

## Prerequiristes 

install Git and of course should have git account 
install node.js
inatall npm 

## Let's start real worl

- install react to create react boilerplate application to start work on.

`$ npm install -g create-react-app`

- create react app called 'react-test-gh-pages'

`create-react-app react-test-gh-pages`

now you can see react-test-gh-pages folder in your working directory 

`cd react-test-gh-pages`

Start react application to check how does it goes

`npm start`

![image](https://user-images.githubusercontent.com/9668906/51879955-522c7a00-23da-11e9-9938-55713c62bc89.png)

let's go to git hub account and quickly create brand new repositiory to work on.

![image](https://user-images.githubusercontent.com/9668906/51880038-a7688b80-23da-11e9-8db4-d788db0a988b.png)

that's allwe need to do on github account now back to terminal

to upload your react app on git we'll follow these steps

```
#create a new git repository
$ git init
#add all changed file paths to staged changes
$ git add .
#commit all staged changes
$ git commit -m 'initial commit'
```
now add our repositiory and push all the changes on master 
```
#add remote repository
$ git remote add origin https://github.com/MonikaPatelIT/react-gh-pages.git
#pushed local repository to remote repository on GitHub
$ git push origin master
```

now  to install gh-pages which help to create gh-pages branch on github which holds all the build folder 
```
#install gh-pages package
$ npm install --save gh-pages
```

few chanegs in #package.json# file 

![image](https://user-images.githubusercontent.com/9668906/51880302-a4ba6600-23db-11e9-9084-e64c540afa7b.png)

Last step if it sucessfully deploy and published 
```
#deploy application
$ npm run deploy
```

If you are not lucky enough and having error something like this 

```
 One or more errors occurred.
bash: /dev/tty: No such device or address
error: failed to execute prompt script (exit code 1)
fatal: could not read Username for 'https://github.com': Invalid argument

npm ERR! code ELIFECYCLE
npm ERR! errno 1
npm ERR! hydra-chat@0.1.0 deploy: `gh-pages -d build`
npm ERR! Exit status 1
npm ERR!
npm ERR! Failed at the hydra-chat@0.1.0 deploy script.
npm ERR! This is probably not a problem with npm. There is likely additional logging output above.

npm ERR! A complete log of this run can be found in:
npm ERR!     C:\Users\{username}\AppData\Roaming\npm-cache\_logs\2018-02-27T03_21_59_227Z-debug.log
```

The try the following solution 

![image](https://user-images.githubusercontent.com/9668906/51880440-21e5db00-23dc-11e9-9a30-5badc2e2f603.png)

or 

![image](https://user-images.githubusercontent.com/9668906/51880474-3c1fb900-23dc-11e9-93fd-e9c892a7e9fe.png)

for the original soure issue link here [https://github.com/tschaub/gh-pages/issues/230](https://github.com/tschaub/gh-pages/issues/230)
