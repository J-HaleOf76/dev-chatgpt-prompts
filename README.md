# 🤖 DEV ChatGPT Prompts

Welcome to my personal collection of ChatGPT prompts for developers!

This repository contains a list of powerful ChatGPT prompts that can help you get the creative juices flowing. Whether you are a beginner or an experienced pro, these prompts can help you think outside the box and find new solutions to problems.

The list is divided into categories: [ prompts for coders, students, marketers, and content writers ]. So no matter your profession, there is something here for everyone! Let’s dive right into these powerful ChatGPT prompts that can help take your creativity to the next level!

## Table of Contents

Prompts for Coders

- [Direction / Advise / Questions](#direction--advise--questions)
- [Adding Documentation](#adding-documentation)
- [Explain Code](#explain-code)
- [Ask for alternatives](#ask-for-alternatives)
- [Code Refactoring](#code-refactoring)
  - [Refactor Code](#refactor-code)
  - [Modernizing Old Code](#modernizing-old-code)
  - [Adding Coding Best Practices or Principles](#adding-coding-best-practices-or-principles)
  - [Detecting and Fixing Errors](#detecting-and-fixing-errors)
  - [Debug a React component](#debug-a-react-component)
  - [Create Unit Tests](#create-unit-tests)
  - [Transpiling Code](#transpiling-code)
  - [Responsive Design](#responsive-design)
  - [Internationalization](#internationalization)
  - [Add comments to code](#add-comments-to-code)
- [Code Generation](#code-generation)
  - [Create Functions](#create-functions)
  - [Add Functionality](#add-functionality)
  - [Create Boilerplate Code](#create-boilerplate-code)

## 🚩 Tips

Like many things in life, with GPT-4, you get out what you put in. In this case, providing more context, instructions, and guidance will usually produce better results.

Here are some tips and techniques to improve:

- **Split your prompts:**
Try breaking your prompts and desired outcome across multiple steps. Keeping prompts to have a single outcome has shown to produce better results than combined prompts. For example, ask for a review, then ask for a refactor based on the review response. This may become less important in time as LLMs increase their token limit.

- **Give Examples:**
Provide expected inputs, data and outputs to improve accuracy quality.

- **Be Specific:**
Don’t be afraid to list exactly what you want, what you know, what is needed, and what not to include.

- **Ask it to Reflect:**
A technique called reflexion has been shown to increase GPT4’s accuracy. Basically ask it ‘Why were you wrong?’ or get it to reflect and review its own response.

## 🔗 A multi-prompt approach (prompt chaining)

can be used to update, refactor, and review a piece of code. A well-designed set of prompts is one where each has separated concerns and singular responsibilities.

### 1. Modernize and add best practices

by getting GPT-4 to re-write your code into the style you want. This step will generally result in coherent output, in the style you want, but may introduce errors, so we do it first.

Prompt:

>Review the following code and re-write it to modern es6 programming standards and formatting:
>
>[insert code here]

### 2. Review your code for logical errors and security concerns

Get recommendations to improve any logical or security concerns introduced. It’s important that we don’t ask for a refactor, just the reasoning behind wanting the refactor.

Prompt:

>Review your provided code 'tempFunction' for any logical or security concerns and provide a list of recommendations.

### 3. Validate the recommendations (reflexion)

Validate the provided recommendations. Reflexion is a powerful technique to improve the accuracy of the initial recommendations and try to eliminate any hallucinations. This is not always required but it is worth asking if you are unsure about any recommendations.

Prompt:

> Review your above recommendations. Tell me why you were wrong and if any recommendations were overlooked or incorrectly added?

### 4. Write the Code

Combine your reviews, recommendations and feedback to get GPT-4 to write your new function.

Prompt:

>Re-write the 'tempFunction' function based off your review and recommendations.

### 5. Create Tests

create some simple tests that we can run locally and validate the results

Prompt:

> Create two [ define technology ] tests for the above 'tempFunction' function. One that is expected to pass and one that is expected to fail.

## Direction / Advise / Questions

## Adding Documentation

Adding documentation requires creating clear and comprehensive explanations of a module’s purpose, design, and implementation.

Prompt 1#:

> I don't know how to code, but I want to understand how this works. Explain the following code to me in a way that a non-technical person can understand. Always use Markdown with nice formatting to make it easier to follow. Organize it by sections with headers. Include references to the code as markdown code blocks in each section. The code:
>
>[insert code here]

Prompt 2#:

>Please add comprehensive documentation for [file or module name], including clear and concise explanations of its purpose, design, and implementation. Consider including examples of how to use the module, as well as any relevant diagrams or flow charts to help illustrate its workings. Ensure that the documentation is easily accessible to other developers and is updated as the module evolves. Consider using documentation tools such as inline comments, markdown files, or a documentation generator to simplify the process.
>
>[insert code here]

<sup>[back to table of contents](#table-of-contents)</sup>

## Explain Code

Don't spend time trying to figure out how code works, just ask ChatGPT to explain it to you

Prompt:

> Context: I'm starting a new position as backend developer and I have to start to understand how some functions are working
>Technologies: [INSERT YOUR TECHNOLOGIES HERE]
>You have to: explain me the code line by line
>
>[INSERT YOUR CODE HERE]

<sup>[back to table of contents](#table-of-contents)</sup>

## Ask for alternatives

If you're not satisfied with your solution you can ask to ChatGPT to give you alternatives

Prompt:

> I'll provide you with a piece of code that I made and 
>I need you give me alternatives to do the same in other way:
>
>[INSERT YOUR CODE HERE]

<sup>[back to table of contents](#table-of-contents)</sup>

## Code Refactoring

### Refactor Code

Ask to ChatGPT to refactor your code

Prompt:
> I have a piece of code and I need you do a refactor of it:
>
>[INSERT YOUR CODE HERE]

Refactoring code is an essential process in software development that aims to improve the quality, readability, and maintainability of existing code without altering its functionality. Refactoring can enhance code efficiency, reduce errors, and make it easier to modify or extend in the future. With ChatGPT’s help, you can effectively refactor your code and achieve a better code structure.

<sup>[back to table of contents](#table-of-contents)</sup>

### Modernizing Old Code

By providing your old function to GPT-4 and asking it to refactor it to modern coding practices, you can quickly modernize your code.

Prompt:
> Refactor the following code to modern es6 programming standards:
>
>[INSERT YOUR CODE HERE]

<sup>[back to table of contents](#table-of-contents)</sup>

### Adding Coding Best Practices or Principles

If your organization or code base uses specific coding practices and styles that you want to maintain, you can provide instructions to GPT-4 on which particular coding practice or style you’d like it to focus on.

Prompt:
> Review the following code and refactor it to make it more DRY and adopt the SOLID programming principles.
>
>[INSERT YOUR CODE HERE]

<sup>[back to table of contents](#table-of-contents)</sup>

### Detecting and Fixing Errors

Sometimes we are unaware of the vulnerabilities or potential issues our code can create. Having GPT-4 review and address code issues can save you more than just time.

Prompt 1#:
> Review this code for errors and refactor to fix any issues:
>
>[INSERT YOUR CODE HERE]

Prompt 2#:

>I'm developing software in [INSERT YOUR TECHNOLOGIES HERE] and I need you help me to find and
fix all the errors in my code, following the best practices. I'll provide you my code
and you'll give me the code with all the corrections explained line by line 

<sup>[back to table of contents](#table-of-contents)</sup>

### Debug a React component

This process typically involves identifying the source of the error, understanding the issue, and implementing a solution to resolve the issue

Prompt:

> Please find and fix the bug in the [component name] component that is causing [describe the issue].
>
>[INSERT YOUR CODE HERE]

<sup>[back to table of contents](#table-of-contents)</sup>

### Create Unit Tests

Unit tests are automated tests that check the behavior of individual units of code in isolation. They help catch bugs early and make it easier to maintain the code.

Prompt 1#: 

> Please write unit tests for [file or module name] to ensure its proper functioning
>
>[insert code here]

Prompt 2#:
> Create 2 unit tests for the provided code. One for a successful condition and one for failure.

<sup>[back to table of contents](#table-of-contents)</sup>

### Transpiling Code

There are many reasons why you may need to convert code from one language to another. For example, you may have found a repository with code for one language that you need in another, you’re moving code bases, or maybe your boss read an article on the latest front-end framework and now you’re moving to a divisive new library.

Prompt:
> Rewrite the following code in Rust:
>
> [INSERT YOUR CODE HERE]

<sup>[back to table of contents](#table-of-contents)</sup>

### Responsive Design

Responsive design adapts a website to different screen sizes and devices, using flexible layouts, images, and CSS media queries. It aims to provide a good viewing experience for all users

Prompt:
> RPlease implement responsive design for the [component name] component to ensure that it looks and functions correctly on different screen sizes and devices. Consider using [responsive design technique or library] to achieve this.
>
>[insert code here]

<sup>[back to table of contents](#table-of-contents)</sup>

### Internationalization

Internationalization, also known as i18n, is the process of designing a software application to be able to support multiple languages and regional differences

Prompt:
> Please implement internationalization for the [component name] component to ensure that it can be used by users in multiple languages. Consider using [internationalization library or technique] to achieve this.

<sup>[back to table of contents](#table-of-contents)</sup>

### Add comments to code

If your code is self-explanatory but requires commenting, this can be a huge time-saver.

Prompt:
> Add comments to the following code:
>
> [INSERT YOUR CODE HERE]

<sup>[back to table of contents](#table-of-contents)</sup>

## Code Generation

### Create Functions

Provide context of your software and ask directly for creating functions you need for your software

Prompt:

> Context: I'm creating a software to manage projects
>
> Technologies: Go, PostgreSQL
>
> Description: It's a function that let me find users by its email or username.
>
> You have to: create the function for me

Also you can add in the description what you expect to receive from your function. If you already have an structure for the User, specify it, for example:

Prompt:

> Context: I'm creating a software to manage projects
>
> Technologies: Go, PostgreSQL
>
> Description: It's a function that let me find users by its email or username and returns the structure type "Member"
>
> You have to: create the function for me

<sup>[back to table of contents](#table-of-contents)</sup>

### Add Functionality

Prompt:

> I need a piece of code in [INSERT YOUR TECHNOLOGIES HERE] to implement [real-time communication]

<sup>[back to table of contents](#table-of-contents)</sup>

### Create Boilerplate Code

Starting new projects can be painful. While GPT-4 doesn’t know your business logic, it can be used to generate boilerplate code. This isn’t technically refactoring, but it’s amazing and can be part of the programming lifecycle process.

<details>
  <summary>Prompt:</summary>

```
Write me a boilerplate Node.js function that will take a variable of type User,
validate that the user has the right permissions, fetch an array of item type Posts
from a postgres database and return them. Leave comments for business logic.
```

</details>

<sup>[back to table of contents](#table-of-contents)</sup>

## 📚 Tools

- [ChatGPT](https://chat.openai.com/)
- ...

<details>
  <summary>Prompt:</summary>
  
  <br>

```
Write me a boilerplate Node.js function that will take a variable of type User,
validate that the user has the right permissions, fetch an array of item type
Posts from a postgres database and return them. Leave comments for business logic.
```

  ### Some Code
  ```js
  function logSomething(something) {
    console.log('Something', something);
  }
  ```
</details>