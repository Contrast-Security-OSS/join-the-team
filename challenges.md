# About the Code Challenges
Welcome to the Contrast Code Challenges project page. Code challenges are an important part of our recruiting and hiring process. Every engineer/developer, designer or technologist that works at Contrast, full-time or intern submits a code challenge as part of the process to join the team.

The code challenge is designed to give candidates the ability to showcase their skills in a low stress, extended time model rather than in a conference room as part of a technical interview. While we give you ample time, each code challenge is designed to take no more than 4 to 8 hours. We believe that technologists work best in the comfort of their own home, coffee shop or favorite place to code or design.

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

## Language Agent Developer Project 
Our agent technology is the heart and soul of our product. Agent engineers need to be highly proficient in the language they are supporting. They must want to explore the internals of the language and the engine the language runs within. To really be successful you have to be willing to "hack" the language you are working. Each of the languages below provides an interface to capture a bevy of instrumentation from your web application. 

 **This project takes can take upwards of 8-10 hours**. 

For this project we are asking that you build the beginnings of a language based agent. The agent will simply have to be configured into the runtime of a web application and perform some very basic instrumentation. We often recommend that you look at existing APM technology like New Relic, AppDynamics or dynaTrace for inspiration. If you are familiar with an APM agent, then you will quickly learn how to solve a basic agent instrumentation effort.

You have the option of finding an Open Source web application leveraging one of the language frameworks below depending on which team you are applying. There are lots of open source web applications to choose from. All that we ask is that you choose one that can easily be setup and configured. Alternatively, if you don't really like any of the applications on GitHub, feel free to write your own based on the requirements from Project #2 for the Full Stack Engineer position. 

All projects need to count: 

* How many string objects were created for a single page request or RESTful request?
* Instrument the response to include a unique id

We then want you to explore (2 out of 3) data points specifically:

* Time the request from start to finish.
* How much memory does a single page request take?
* How many assemblies/classes/methods were loaded (depends on language)?

Provide an interface that instruments the application to answer the questions above (preferably both to an endpoint, console and log). Ideally, the interface is a flag or switch that can be turned on/off as part of the startup of the application. 

Bonus: Show metrics on the page or a separate app/webpage

Note: you only have to pick one language and that language should be the one that you are applying for. See below for further instructions for .NET. 

| Language | framework                       | Use of ORM                | Sample Web Application (Example)  |
|----------|---------------------------------|---------------------------|-----------------------------------|
| Java     | Spring                          | Hibernate                 | [WebGoat](https://github.com/WebGoat/WebGoat), [Sakai](https://sakaiproject.org/try-sakai) |
| NodeJS   | ExpressJS                       | Sequelize                 | [NodeGoat](https://github.com/OWASP/NodeGoat), [Contrast Node App](https://github.com/Contrast-Security-OSS/NodeTestBench) |
| Ruby     | Rails                           | Active Record             | [RailsGoat](https://github.com/OWASP/railsgoat), [Canvas](https://github.com/instructure/canvas-lms) |
| Python   | Django or Flask                 | Django ORM or SQL Alchemy | [Sample LMS in Flask](https://github.com/adeora/Python-LMS), [Graphite](https://github.com/graphite-project/graphite-web) |

Make sure to provide an amazing README that tells us how to setup your project and turn on the instrumentation.

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

<a href="UX.png" title="UX"><img src="UX.png" alt="UX."></a>

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


