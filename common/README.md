# why create a common file?
- We have created a common file so that we can have access of it over in our front and back end 

# Now how to access this file across , one of the ways is NPM repositories
### how to create NPM repos?
- in package.json change the name to something like @imsanc/common as it should be a unique name 
- change the root path of main to the existing main index file eg : ./src/index.ts
- npm login to log into the npm repo

- Now publish it 
npm publish --access=public
note :- you have to host it as public as for private you need a paid account

- If you want to publish further more versions then you will have to add versions in package.json

- How to see which files you have published 
npm pack

- Now you dont want to upload ts files in the npm therefore we ignore src folders
for ignoring files and folders then we will have .npmignore there we will place the files and folder we want to ignore.

### Now if we have ignored src folder there will be only JS code available then how would TS will be able to identify the types?

- for this we need index.d.ts file to be created 
for this add " "declaration": true " in your package.json  which will create .d.ts file in the dist folder which can now be used to identify in .ts file.





