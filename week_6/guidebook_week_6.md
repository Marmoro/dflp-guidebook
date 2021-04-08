**Full-Stack Developer Path | Virtual Lab Activity | Week 6 | Back-end Continued | Apr 2021**

# Digital Future Leaders Program

### Continuation of the previous activity

Exercise files here: https://github.com/Marmoro/crmforpeople-app.git

#### Cloning the back-end application
```bash
$ git clone https://github.com/Marmoro/crmforpeople-app.git
```

In this week, we will continue working on the previous activity to make it ready for integration. And to reach this state, there are a couple of things we have to do.

But before that, let's refresh our mind and reflect back into what we have been working with so far.

In the early days, we built a simple website using HTML, CSS and JS, and the codebase did not have complex functions, only simple ones. Because the goal was not to demonstrate the capability of these tools, but to know how to build something useful. Then we moved few levels up and started with Angular to build a web application and then with NestJS we started to build the back-end application for it.

In between these tools, there are other important topics that maybe we didn't get deep into yet such as:
- [TypeScript](https://www.typescriptlang.org/docs/handbook/intro.html)
- [SCSS](https://sass-lang.com/guide)
- [NodeJS](https://nodejs.org/dist/latest-v14.x/docs/api/synopsis.html)
- [Redis Database](https://redis.io/topics/introduction)
- [MySQL Database](https://www.w3schools.com/sql/)
- [Docker](https://docs.docker.com/get-started/overview/) and [Docker Compose](https://docs.docker.com/compose/)
- Libraries used in our front-end and back-end applications
  - [Angular Material](https://material.angular.io/)
  - [Angular Flex Layout](https://tburleson-layouts-demos.firebaseapp.com/#/docs)
  - [Observables & RxJS](https://angular.io/guide/observables)
  - [TypeORM](https://typeorm.io/)
  - [Express Session](https://www.npmjs.com/package/express-session)
  - [PassportJS](http://www.passportjs.org/docs/downloads/html/)

We are giving you a fast-track by showing you how to building something useful with these tools and then explain how everything works and makes sense. And today's learning objectives are:

- Use Docker and Docker Compose to run MySQL & Redis locally as containers
- Use express session with redis to store user sessions
- Setup user authentication and authorization using PassportJS and NestJS Guards feature
- Create database by connecting to the MySQL container's shell and using mysql command
- Refactor existing entities (Case, Organization, User)
- Create One-Time Password authentication for users
- Fix bugs that exists in the exercise files 👾
- Create a build of the application using npm