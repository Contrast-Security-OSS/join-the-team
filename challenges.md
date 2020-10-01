# About the Code Challenges
Welcome to the Contrast Code Challenges project page. Code challenges are an important part of our recruiting and hiring process. Most engineer/developer, designer or technologist that works at Contrast, full-time or intern submits a code challenge as part of the process to join the team. Some candidates prefer a technical interview and some prefer reviewing a past project. Our goal is to accommodate the candidate's preference.

The code challenge is designed to give candidates the ability to showcase their skills in a low stress, extended time model rather than in a conference room as part of a technical interview. Be aware that each code challenge can take longer than a day to complete, hence we give you ample time to work it. We believe that technologists work best in the comfort of their own home, coffee shop or favorite place to code or design.

Most importantly we do the challenge for you. Anyone submitting a code challenge, owns their own code, whether they put it on GitHub or another site. Our theory is that you are putting time into the interview process. We want you to get something out of the effort. What better than something to add to your portfolio?

One last important item...please do not reference Contrast on your project as we do not want to introduce the possibility of someone plagiarizing your work. We rotate projects several times a year.

# Developer Projects
We offer two options to the developer project. The first project is designed for the full stack engineer who likes to design slick, web interfaces. The second project is more suited for the backend developer who still values interactivity with users of the application, but in a different modality.

You only have to complete one project.

## Full Stack Web Application (UI and Service Layer Only)
If you have made it this far then you've learned enough to know that [Contrast](https://www.contrastsecurity.com/) is an application and cyber security platform. We think of security in terms of vulnerabilities, threats, and attacks.

As part of this project, we would like for you to build a simple, yet elegant application that visualizes a security intelligence data feed (vulnerabilities or threat intelligence data). We ask that your UI contains at least:

* Map if you are visualizing geo-location data that can zoom in/out
* Grid control (aka...a table of data) to present the data presented in the map
* Search of data to change the presentation in the map and grid.

It should be a clean UI written in one of the recommended JS frameworks below. The service layer should be written in Java.

Feel free to use any of the these JavaScript frameworks:
* Angular
* React
* Vue
* Meteor
* Ember

We recommend that you identify one or more data feeds from one of these three sources.

* Interesting [GitHub Project with Curated Threat Intelligence Feeds](https://github.com/hslatman/awesome-threat-intelligence)
* [National Vulnerability Database](https://nvd.nist.gov/vuln/data-feeds)
* Choose or recommend an alternate data set.

Additional requirements as part of our craftsmanship initiative:
* Make sure to write an amazing README in your GitHub project that explains what your built, why you built it, how to set it up and how to use it.
* Unit tests
* Integration tests of your service layer
* CI Pipeline to compile, build, test and report in [Travis CI](https://travis-ci.com/) which is free for any Open Source project in GitHub

## Node.js Agent Developer Project
Our agent technology is the heart and soul of our product. Agent engineers need to be highly proficient in the language they are supporting.
They must want to explore the internals of the language and the engine the language runs within. To really be successful you have to be willing
to "hack" the language you are working. Each of the languages below provides an interface to capture a bevy of instrumentation from your web application.

 **This project takes can take upwards of 8-10 hours**.

For this project we are asking that you build the beginnings of a Node.js agent. The agent will simply have to be configured into the runtime of an
Express, Hapi, or Koa application and perform some very basic instrumentation. We recommend that you look at existing APM technology like New Relic,
AppDynamics or Dynatrace for inspiration. If you are familiar with an APM agent, then you will quickly learn how to solve a basic agent instrumentation effort.

**Project Requirements**

* Count how many string objects were created for an API request.
* Instrument the response to include a unique ID

We then want you to explore (2 out of 3) data points specifically:

* Time the request from start to finish.
* How much memory does a single page request take?
* How many modules were loaded?

Provide an interface that instruments the application to answer the questions above (preferably both to an endpoint, console and log). Ideally, the interface is a flag or switch that can be turned on/off as part of the startup of the application.

Bonus: Show metrics on the page or a separate app/webpage

**Additional Requirements**

* Unit tests
* Make sure to write an amazing README in your GitHub project that explains what you built, why you built it, how to deploy it up and how to use it.
* CI Pipeline to compile, build, test and report in [Travis CI](https://travis-ci.com/) which is free for any Open Source project in GitHub
Include the [Travis build badge](https://travis-ci.com/) in your README to show status.

### Python Instrumentation Engineer Project

For this project we are asking that you build a minimalist version of an Application Performance Monitoring (APM) library for Django (or Flask or Pyramid). The middleware should get the time that the request enters the middleware, the time that it leaves the middleware, request path, the parameter list, the MD5 hash value of the rendered output, and the current thread and process ids. This should be appended to a CSV file. The location and name of the file should be configurable by the user of the library. To make it interesting the agent, optionally, should do its MD5 calculation in compiled C or Rust code.

**Getting Started**

1. Create a library that can be added to a Django project.
2. Add the library to an open source Django project and generate a performance metrics CSV file.

**Project Requirements**

* The Django (or Flask or Pyramid) middleware should generate a CSV file with the following fields:
  * Params: a semi-colon delimited list of GET parameter keys
  * MD5: the hashed value of the response body
  * Process ID: the process ID of the current request
  * Thread ID: the thread ID of the current request
* The filename and path of the generated CSV file should be configurable by the user of the library
* Optional: generate the MD5 hash in C or other compiled lanaguage (e.g. C++, Rust)
* Write unit tests.
* Write a README that explains what you built and how to add it to an application.

Goals: We are interested in how you write idiomatic and well-tested python code in a library that could be shared among many teams, particularly when some of the logic is implemented in not-python code. `virtualenv` is your friend if you want to check for both 2.7 and 3.x Python compatibility.

### Ruby Instrumentation Engineer Project

For this project we are asking that you build a minimalist version of an Application Performance Monitoring (APM) library for Ruby on Rails. The middleware should get the time that the request enters the middleware, the time that it leaves the middleware, request path, the parameter list, the MD5 hash value of the rendered output, and the current thread and process ids. This should be appended to a CSV file. The location and name of the file should be configurable by the user of the Gem. To make it interesting, the project should add itself to the hosting Ruby on Rails application using Railties *AND* the agent, optionally, should do its MD5 calculation in compiled C or Rust code.

**Getting Started**

1. Create a Gem that can be added to a Ruby on Rails project.
2. Add the Gem to an open source Ruby on Rails project (RedMine, Discourse, etc) and generate a performance metrics CSV file.

**Project Requirements**

* The Rack middleware should be implemented as a [Railtie](https://api.rubyonrails.org/classes/Rails/Railtie.html)
* The middleware should generate a CSV file with the following fields:
  * Request Time: the timestamp when the request enters the middleware
  * Response Time: the timestamp when the request leaves the middleware
  * Elapsed Time: the time betwen request and response
  * Path: the URI of the request
  * Params: a semi-colon delimited list of GET parameters
  * MD5: the hashed value of the response body
  * Process ID: the process ID of the current request
  * Thread ID: the thread ID of the current request
* The filename and path of the generated CSV file should be configurable by the user of the Gem
* Optional: generate the MD5 hash in C or Rust ([Helix](https://github.com/tildeio/helix) is an option).
* Write unit tests in RSpec and, optionally, add add it to Travis CI.
* Write a README that explains what you built and how to use it.

Goals: We are interested in how you write idiomatic and well-tested ruby code in a gem that could be shared among many Ruby on Rails projects particularly when some of the logic must be implemented in non-ruby code. `rvm` or `rbenv` is your friend if you want to test in multiple ruby versions.

### Java Instrumentation Engineer Project

We have a very specific project for Java agent engineer candidates. The project for the Java Agent Software Engineer is to create a metric-gathering extension for a web application. This "extension" should gather metrics about requests and responses served by the application and the candidate is encouraged to design this extension such that it is decoupled from the web application.

Note that to solve this problem, it is not necessary to create a javaagent. The goal of this project is to demonstrate an understanding of how a Java web framework handles the HTTP request and response lifecycle.

**Getting Started**

1. Create a small Java web application with a few test pages.
2. Implement a metric-gathering library in Java that satisfies the requirements below and extend your web application with it.

**Project Requirements**

* Request Time: measure time spent between when the application starts to process the request and the time when the application sends the response to the client.
* Response Sizes: measure the size of the HTTP response body in bytes.
* Metrics: Calculate minimum, average, and maximum for Request Time and Response Size.
* Identifier: Add a unique identifier to every response via an HTTP header.
* Implement a page that will display the metrics gathered by the extension. The display should include minimum, average, and maximum of both Request Time and Response Size.
* Bonus/Optional: Provide a front-end UI that allows users to look up historical request time/response size by unique identifier.
* Integrate with CI
* Write unit tests
* Write a README, project that explains what you built, why you built it, how to deploy it up and how to use it.
* Use a CI Pipeline to compile, build, test and report in Travis CI which is free for any Open Source project in GitHub Include the Travis build badgein your README to show status.

**Project Constraints**

* Your web application should store state in memory and not in a database running in an external process. This helps us get your project running.
* Your metric-gathering extension should manage its own state in-memory. More specifically, we want you to show us how to manage the metric-gathering state in thread-safe data structures vs how well you can use an in-memory database like HSQLDB.
* Prefer building your metric-gathering extension on widely adopted specifications vs specific technologies. For example, we would prefer to see a metric-gathering extension implemented as a servlet filter vs a Tomcat valve implementation.

Goals: We are interested in how you write well-structured, well-tested code that needs to interact with shared mutable state. Therefore we encourage you to implement your own metric-gathering rather than use any metric-gathering capability provided by your web application framework "out of the box". Our review's focus will be on the metric-gathering extension and not on the web application.



### .NET Instrumentation Engineer Project

We have a very specific project just for .NET agent engineers. We ask that candidates interested in working on our .NET agent to implement either a metrics gathering extension, either as an ASP.NET Core [Middleware](https://docs.microsoft.com/en-us/aspnet/core/fundamentals/middleware/) or an ASP.NET [IHttpModule](https://docs.microsoft.com/en-us/dotnet/api/system.web.ihttpmodule).

Your `Middleware` (or `IHttpModule`) extension should be designed so that it can be safely added to any ASP.NET Core (or ASP.NET) web application.

**Project Requirements:**

* Request Time Metric: Total time spent processing the current request.
* Response Size Metrics : Size of the response in bytes of the current request.  Also please calculate the Minimum, Maximum and Average response sizes seen so far.
* For HTML pages add the above Request Time and Response Time metrics to the response so they can be viewed directly on the page.
* Include unit and/or integration tests.
* Integrate with CI to compile, build, test your project.  You may use [AppVeyor CI](https://www.appveyor.com/) or [Azure DevOps](https://azure.microsoft.com/en-us/services/devops/) or another free CI Pipeline service of your choice.
* Include a small web application that demonstrates the behavior of your extension.  This web application is *not* the focus of the project and it needs to merely demonstrate metrics being added to its pages.  You should feel free to use the web application template projects provided by Visual Studio.
* Write a README in your GitHub project that explains what you built, why you built it, how to deploy it up and how to use it.  You can also outline any future improvements you would like to make to the project.

**Project Contstraints:**

* Your extension can safely handle multiple encodings and different types of pages.
* Your extension should store state in memory and not in a separate database.
* Your extension is thread-safe and can correctly handle multiple concurrent requests.
* Your extension uses server resources (i.e. memory and processor) efficiently.

**Bonus:**

* Include the AppVeyor or Azure DevOps build badge in your README to show status.
* Provide a way to see metrics for non-HTML pages

**Project Goals:**  We are interested in how you write well-structured, well-tested code that needs to safely interact and not adversely affect unknown third-party applications.  This is similar to the kind of work you would do as part of an agent team at Contrast.
Your extension needs to implement its own metric gathering rather than rely on any metric gathering capability provided by your web application framework or third party component.  Our review's focus will be on your extension and not on the web application.



# Cloud Engineering Project:

At Contrast we like to play hard, work hard, and automate our Saas environment end to end. We made this project so you can showcase your skills and give us a better idea of your individual talents.

Take a look at this [project here](https://github.com/Contrast-Security-OSS/infrastructure-hire-project). You will need to clone the repo and send it our way when you are finished.


# Integrations Developer

We have three projects to choose from if you're applying to be an integrations developer at Contrast.

Pick a project that appeals to you and follow the instructions. Commit often with quality commit messages so that we can see your thought process as the project progresses.

After submitting your project, you'll have a conversation with one of our engineers about your code, the decisions you made, things you liked, things you didn't, etc...

Thanks for looking!

### Add a Hook to a Cloud Foundry Buildpack

Clone the repository [here](https://github.com/Contrast-Security-OSS/project-nodejs-buildpack) and follow the instructions in the README.

### Write a Contrast Security Command Line Client

**Setup**

* Sign up for a [Contrast Security Community Edition](https://www.contrastsecurity.com/contrast-community-edition) account.
* Onboard a web application so it appears in your list of Applications in Contrast Security. [WebGoat](https://github.com/WebGoat/WebGoat) is a good sample Java project to onboard. We have others in our [Github](https://github.com/Contrast-Security-OSS) repository.
* Use WebGoat such that Vulnerabilities appear in your Vulnerabilities tab

**Project**

* In the language of your choice, write a command-line client that uses the [Contrast Security API](https://api.contrastsecurity.com/) to list vulnerabilites for an organization. (In the API, vulnerabilites are called Traces).
