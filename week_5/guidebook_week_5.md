**Full-Stack Developer Path | Virtual Lab Activity | Week 5 | Back-end | Mar 2021**

# Digital Future Leaders Program

### Let's build a backend system using [NestJS](https://nestjs.com/) for our "CRM System For People" app


In the previous activity, we built a basic but functional front-end application for a project called "CRM System For People". And we have built it in a way so that it can be easily integrated with a backend system, In other words, minimizing hard coding.

Notice that we started with a basic website in the first week, then we looked into some useful open sources packages that we can use to build a full stack application.

The main programming language we are relying on is [Node.js](https://nodejs.org/en/)

The reason why we chose NestJS instead of Express.js is due to the following reasons:
- It uses TypeScript by default, just like Angular, meaning you'll be able to find bugs early
- It has a powerful CLI that helps in writing boilerplate code
- It has almost everything we need to build a backend system for the business requirement we have
- It uses the same structure as Angular
- And it is based on Express.js 😎

### Learning Objectives

By the end of this activity you will learn the following:

- Learn how to install NestJS CLI
- Learn how to use NestJS documentation guide
- Learn how to use NestJS CLI to add a resource
- Use TypeORM to define our objects (Case, Organization, User)
- Use Swagger to provide documentation for our API
- Use the API explorer provided by Swagger
- Use express session with redis to store user sessions
- Setup user authentication and authorization