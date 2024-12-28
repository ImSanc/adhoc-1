# Module 
A module is just a file that contains code you can export and reuse in other parts of your project.

- Why are they useful?
 - Encapsulation
 - Reusability
 - Avoid Global Scope Pollution

 # Package 
 A package is a collection of one or more modules, often bundled together and shared via a package manager (like npm)

- Packages are often stored in the node_modules folder in your project


## modules and packages are essential for structuring and scaling a project

# Zod inference 
- When we create a set of rule which is common in frontend and backend example structure of.
- As we have already applied a structure in the backend using zod for input validation
- we can re use it using zod using infer 

example : 
```typescript 
const signupInput = z.object({
  username : z.string(),
  password : z.string()
})

//creating a type inference 
type SignupParams = z.infer<typeof signupInput>