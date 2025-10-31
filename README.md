# swe-sr-1-3

## Setup

For guidance on setting up and submitting this assignment, refer to the Marcy lab School Docs How-To guide for [Working with Short Response and Coding Assignments](https://marcylabschool.gitbook.io/marcy-lab-school-docs/how-tos/working-with-assignments#how-to-work-on-assignments).

Here are some useful commands to remember.

```sh
npm i                   # install dependencies
git checkout -b draft   # switch to the draft branch before starting

git add -A              # add a changed file to the staging area
git commit -m 'message' # create a commit with the changes
git push                # push the new commit to the remote repo
```
## Question 1

Read the documentation for `findIndex` and `indexOf` on MDN:
- [findIndex](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/findIndex)
- [indexOf](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/indexOf). 

Explain the difference between the methods and explain when you would choose one over the other. Provide examples to enhance your response.

### Response

Add your response here...

`indexOf` is an **array method** that takes in a **parameter** to search for in the array. It will then `return` the first **index** of that **parameter**, if there is no instances of that value it will then only `return` -1.

Example:

```js
const arr = [4,9,8];

console.log(arr.indexOf(4)) // Prints 0
console.log(arr.indexOf(0)) // Prints -1
```

`findIndex` is also an **array method** but is a **higher order array method** that takes a **callback function**. It will also `return` either the **index** of the desired value or -1 if nothing adheres to the condition. However, the special thing about this method is that it can have any condition such as returning the first element that is higher than 10. Basically it doesn't have to equal to a specific value and can equal anything you enter in the **callback function**.

```js
const arr = [4,9,8];
const index = arr.findIndex((ele) => ele > 7);
console.log(index); // Prints 1

const index2 = arr.findIndex((ele) => ele > 10);
console.log(index2) // Prints -1
```
