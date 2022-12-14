# setup env
``npm install -g pnpm``

``npm install -g @microsoft/rush``

run ``rush update`` to install dependencies

run ``rush build`` to build all projects

run ``rush build -o admin`` to build only admin project
run ``rush build -o shop`` to build only admin project


# testing out rush
make a change to ``apps/shop/src/App.js`` and run ``rush build`` again
```
==[ shop ]=========================================================[ 1 of 2 ]==
"shop" completed successfully in 3.94 seconds.

==[ admin ]========================================================[ 2 of 2 ]==
"admin" was skipped.
```
you will see that rush only builds the apps where changes are detected. 

# setting up pre-commit git hooks
```
cd common/git-hooks
touch pre-commit 
rush install
```
rush should detect changes to files under git hooks 
and add them so that when you run ``git commit``
if trouble with permission make sure to run ``chmod +x pre-commit``

# create a new library
```
cd libs
npx tsdx create button
```
check package.json change its name to the same used in rush.json
install any dependencies that are used, like react etc. 




# Resources
https://rushjs.io/pages/intro/get_started/

https://tsdx.io/

https://pnpm.io/installation
(this project uses pnpm version 6.11.0)

https://www.linkedin.com/learning/building-monorepos-on-github/installing-shared-components

