# Creating and publishing a bower package
- I want to create a repository with some source files and some grunt tasks, but I only want to
publish a dist folder.
- To create a bower package you will need a git repository and a bower.json file.
- I created a bower.json using "bower init". On the main property I specified a file in the dist folder.
- I published my package using "bower register axelsbowerpaket https://github.com/Edminsson/mini_bower.git"
- When I installed my newly created bower package in a new folder all the files got installed even the source files.
This is not what I wanted.
- I added the files and folders I did not want to be copied to the ignore section in bower.json. That helped.
 
