# Creating and publishing a bower package
- I want to create a repository with some source files and some grunt tasks, but I only want to
publish a dist folder.
- To create a bower package you will need a git repository and a bower.json file.
- I created a bower.json using "bower init". On the main property I specified a file in the dist folder.
- I published my package using "bower register axelsbowerpaket https://github.com/Edminsson/mini_bower.git"
- To list available version of the package run "bower info axelsbowerpaket"
- Observe that the name property in bower.json does not have to be the same as the registered name.
- When I installed my newly created bower package in a new folder all the files got installed even the source files.
This is not what I wanted.
- I added the files and folders I did not want to be copied to the ignore section in bower.json. That helped.
- At first when I updated my registered packages I only registered them again with the same command that I used
the first time. I got a message telling me I had a "duplicate package". I did not even have a version in the bower.json
to start with. I added a version number but I stilled got the duplicate message.
- I created a tag using the commands "git tag 1.0.0" and "git push origin 1.0.0".
- It seems like you don't need to register the package several times. You do it once and then you create
new tags in your git repository.
- Tested to create new tags and then call "bower install axelsbowerupdate" and the new version was installed. 
