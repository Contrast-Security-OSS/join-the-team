# About the Code Challenges
Welcome to the Contrast Code Challenges project page. Code challenges are an important part of our recruiting and hiring process. Every engineer/developer, designer or technologist that works at Contrast, full-time or intern submits a code challenge as part of the process to join the team.

The code challenge is designed to give candidates the ability to showcase their skills in a low stress, extended time model rather than in a conference room as part of a technical interview. Be aware that each code challenge can take longer than a day to complete, hence we give you ample time to work it. We believe that technologists work best in the comfort of their own home, coffee shop or favorite place to code or design.

Most importantly we do the challenge for you. Anyone submitting a code challenge, owns their own code, whether they put it on GitHub or another site. Our theory is that you are putting time into the interview process. We want you to get something out of the effort. What better than something to add to your portfolio?

One last important item...please do not reference Contrast on your project as we do not want to introduce the possibility of someone plagiarizing your work. We rotate projects several times a year.

# Developer Projects
We offer two options to the developer project. The first project is designed for the full stack engineer who likes to design slick, web interfaces. The second project is more suited for the backend developer who still values interactivity with users of the application, but in a different modality.

You only have to complete one project. 

## Full Stack Web Application (UI and Service Layer Only Required)
If you have made it this far then you've learned enough to know that [Contrast](https://www.contrastsecurity.com/) is an application and cyber security platform. We think of security in terms of vulnerabilities, threats and attacks. 

As part of this project, we would like for you to build a simple, yet elegant application that visualizes a security intelligence data feed (vulnerabilities or threat intelligence data). We ask that your UI contains at least:

* Map if you are visualizing geo-location data that can zoom in/out
* Grid control (aka...a table of data) to present the data presented in the map
* Search of data to change the presentation in the map and grid.

It should be a clean UI written in one of the recommended JS frameworks below. You can write the service layer in the language of your choice.

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

For this project we are asking that you build the beginnings of a Node.js agent . The agent will simply have to be configured into the runtime of a
Express (or Hapi) application and perform some very basic instrumentation. We recommend that you look at existing APM technology like New Relic, 
AppDynamics or dynaTrace for inspiration. If you are familiar with an APM agent, then you will quickly learn how to solve a basic agent instrumentation effort.

**Project Requirements**

* Count how many string objects were created for a single page request or RESTful request
* Instrument the response to include a unique ID

We then want you to explore (2 out of 3) data points specifically:

* Time the request from start to finish.
* How much memory does a single page request take?
* How many assemblies/classes/methods were loaded (depends on language)?

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

We have a very specific project for Java agent engineer candidates. For any applicant wanting to work on the Contrast Java agent, this project is the 2018 required project.

The project for the Java Agent Software Engineer is to create a metric-gathering extension for a web application. This "extension" should gather metrics about requests and responses served by the application and the candidate is encouraged to design this extension such that it is decoupled from the web application.

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

* Your web application should store state in memory and not in a separate database.
* Your metric-gathering extension should be platform agnostic when possible.

Goals: We are interested in how you write well-structured, well-tested code that needs to interact with shared mutable state. Therefore we encourage you to implement your own metric-gathering rather than use any metric-gathering capability provided by your web application framework "out of the box". Our review's focus will be on the metric-gathering extension and not on the web application.

### .NET Instrumentation Engineer Project

We have a very specific project just for .NET agent engineers. For any applicant wanting to work on our .NET platform, this project is the 2018 required project.

Instrumenting .NET applications requires implementation of a profiler written in C++ which we consider too large for an interview project. Therefore, we ask that candidates interested in working on our .NET agent instead implement an [IHttpModule](https://docs.microsoft.com/en-us/dotnet/api/system.web.ihttpmodule). 

The following project requirements are listed below: 
* Add new content to HTML pages to display information gathered by your HttpModule.
* Measure the total time spent processing the request. 
* Measure the time spent by only the IHttpHandler for the request.
* Measure the size of the response body in bytes. Calculate the minimum, average, and maximum responses seen so far. 
* Provide a script to install your IHttpModule to all applications hosted on IIS.

In addition, please make sure to do the following:
* Integrate with a free CI Pipeline to compile, build, test and report in [AppVeyor CI](https://www.appveyor.com/) which is free for any Open Source project in GitHub
* Automated test coverage
* Make sure to write an amazing README in your GitHub project that explains what you built, why you built it, how to deploy it up and how to use it. Include the [AppVeyor build badge](https://www.appveyor.com/docs/status-badges/) in your README to show status.


# Site Reliability Engineering: The Cloud Operations...Performance and Reliability

At Contrast we like to play hard, work hard, and automate our Saas environment end to end. We made this project so you can showcase your skills and give us a better idea of your individual talents. 

Take a look at this [project here](https://github.com/Contrast-Security-OSS/ops-hire-project). You will need to clone the repo and send it our way when you are finished.


# UX/Designer Project: For the UX Engineer and Interaction Designer

Bad UX is everywhere. There are hundreds of touchpoints out there that could use a little UX love. We find ourselves frustrated by door handles, interfaces, iTunes, automated checkouts, road layouts...the list goes on. 

For this project, you have the opportunity to take a relatively well-known digital site or application with a less-than-stellar customer experience, create a critique of the app, and present some possible solutions with at least one polished high-fidelity mockup. Woo! You have free reign to touch on the information architecture (IA), useful additional features, workflows, terminology, interactions, visual design, etc. 

We want to see your understanding and application of UX principles by demonstrating your process from concept to final solution.

<a href="images/UX.png" title="UX"><img src="images/UX.png" alt="UX."></a>

Upon completion of the above, please send us your collection of artifacts and feel free to use a portfolio storage tool like Behance, [Invision](https://www.invisionapp.com), etc. if you'd like. Happy designing!

# UX/Docs Project: For the Digital Content Strategist
Our customer facing documentation is 100% open sourced on [Github](https://docs.contrastsecurity.com/). We have a strong belief that our documentation will get better with input and feedback from customers and members of the community, hence we've broken down barriers for the community to contribute to our content.

Our content has been built by members of our team to date. There hasn't been a single professional author for any of our documents. We know our documentation could be vastly improved. 

Candidates interested in becoming our first digital content strategist, we would like for you to do a couple of tasks designed to improve our OpenDocs, as we call it.

* Provide an editorial review of the [OpenDocs web site](https://docs.contrastsecurity.com). This can be a very free-form analysis of the site. It should be less than 1000 words. Make sure to include comments on the following:
    - Searchability of Content
    - Structure and Organization of Content
    - Use of Images and Visualizations
    - General Grammar and Content Value
* Make (3) recommendations or improvements that would immediately add value to our user community.
* Submit a writing sample. The writing sample could be completely unrelated to our content on OpenDocs. The writing sample should describe how a user of a web application accomplishes a particular task or set of tasks. It should include:
    - Overview of the task from the end-user's perspective.
    - Steps for the user to execute.
    - Appropriate visual aids
    - Tags for searchability and indexing
    - Please write the sample in [Markdown](https://en.wikipedia.org/wiki/Markdown)

