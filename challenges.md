# About the Code Challenges
We have a couple of code challenges designed to give you the opportunity to showcase your skills. We love to see creativity, originality and simplicity of design. All of our projects involve some creativity, research, interest in data, automation and of course amazing instructions. Please make sure to write the most incredible and informative README.md files you can imagine.

There are tons of amazing open and free data sets to play with. Here are a few for inspiration:

* [Data.gov](https://www.data.gov/open-gov/)
* [NYC Open Data](https://nycopendata.socrata.com/)
* [Austin, TX Data](https://data.austintexas.gov/browse)
* [AWS Open Data](https://aws.amazon.com/public-data-sets/)
* [OpenData Baltimore](https://data.baltimorecity.gov/)
* [Open Data Sets on GitHub](http://www.kdnuggets.com/2015/04/awesome-public-datasets-github.html)
* [Firebase Data Sets](https://www.firebase.com/docs/open-data/)

# Project #1: For the Front-End Enthusiast and JavaScript Aficionados
We would like for you to pick a single data set or multiple temporal data sets that can be combined into a shareable data set for visualization purposes. Finding a perfect data set is not as important as how it is used.

You will need to create a single web page application that can be used to investigate your data set. The data can be reorganized and served however you like. We would like this web application to leverage a single web page framework, preferably AngularJS. You may use alternative SPA's like Ember or React. We recommend using a few different interactive visualizations that help to explore the data, but require at least one to explore the time dimension of the data. The application working with the data set must be capable of the following functional needs at a minimum:

* Ability to filter, search, and sort the data.
* Interact with the visualizations with input controls and/or cursor.
* At least one visualization that is time based and allows direct interaction to alter the date range and narrow the data set (think click and drag).
* Implement a simple front-end router with a few different views or components.

From a development perspective, we are looking for your code to:

* Handle client-side state.
* Cross-browser support (Chrome, FireFox, IE, etc.)
* Slow loading, long wait times, and other bad performance indications should be minimal.
* Proper error handling and data scrubbing.
* Responsive design should be considered.
* Your code should be DRY, maintainable, readable, and organized.
* Include automated tests where applicable.
* 100% automated: Should be simple as a clone and a single command to run.

Make sure to provide an amazing README that tells us how to setup your project. The ideal project will consist of cloning your GitHub repo and running a command or two.

# Project #2: For the Java Full Stack Engineers
The goal of this assignment is to build a small web application that will demonstrate programming skills in Java (preferrably Spring MVC), building RESTful services, the build process, as well as front-end frameworks (preferrably AngularJS). You need to demonstrate an understanding of ORM (preferrably Hibernate) for persistence purposes with MySQL as your data store. We also want to see some basic test automation (Unit and Integration).

We would like you to pick a minimum of two data sets from [OpenData Baltimore](https://data.baltimorecity.gov/) which can be combined into a single, shareable data set in MySQL. The data sets should be selected carefully so that they share a foreign key relationship or two. We ask that you design the schema and create automated scripts to easily bring the data into the database. This can be done via API calls to OpenData Baltimore, or simply package the data into a file as part of the Github project. 

We are looking for you to design an simple interactive web application that visualizes the data. We recommend you present the data in a few formats visually via the combination of charts and grid controls. The application working with the data set must be capable of the following functional needs:

* CRUD against the data (Create Read Update Delete): Provide a means for all (4) operations in the User Interface.
* Include a few complex database queries
* Filtering and sorting the data (via a grid control)
* Interactions with the UI visualization should change the data set in the grid control and vice versa.

From a development perspective, we are looking for:

* Your code should be DRY, maintainable and readable.
* Proper Code organization (Please no monolithic files).
* Organized relational data structure.
* Include automated tests.
* 100% automated: Should be simple as a clone and a few commands to run.

Make sure to provide an amazing README that tells us how to setup your project.

# Project #3: The Cloud Operations...Performance and Reliability

At Contrast we like to play hard, work hard, and automate our Saas environment end to end. We made this project so you can showcase your skills and give us a better idea of your individual talents. 

Take a look at this [project here](https://github.com/Contrast-Security-OSS/ops-hire-project). You will need to clone the repo and send it our way when you are finished.

# Project #4: Language Specialist (Agent Engineer)

Our agent technology is the heart and soul of our product. Agent engineers need to be highly proficient in the language they are supporting. They must want to explore the internals of the language and the engine the language runs within. To really be successful you have to be willing to "hack" the language you are working. Each of the languages below provides an interface to capture a bevy of instrumentation from your web application. 

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

Note: you only have to pick one language and that language should be the one that you are applying for

| Language | framework                       | Use of ORM                | Sample Web Application (Example)  |
|----------|---------------------------------|---------------------------|-----------------------------------|
| Java     | Spring                          | Hibernate                 | [WebGoat](https://github.com/WebGoat/WebGoat), [Sakai](https://sakaiproject.org/try-sakai) |
| .Net     | .Net Web API with SPA Interface | ADO.Net                   | [WebGoat](https://github.com/rapPayne/webgoat.net) |
| NodeJS   | ExpressJS                       | Sequelize                 | [NodeGoat](https://github.com/OWASP/NodeGoat), [Contrast Node App](https://github.com/Contrast-Security-OSS/NodeTestBench) |
| Ruby     | Rails                           | Active Record             | [RailsGoat](https://github.com/OWASP/railsgoat), [Canvas](https://github.com/instructure/canvas-lms) |
| Python   | Django or Flask                 | Django ORM or SQL Alchemy | [Sample LMS in Flask](https://github.com/adeora/Python-LMS), [Graphite](https://github.com/graphite-project/graphite-web) |

Make sure to provide an amazing README that tells us how to setup your project and turn on the instrumentation.

# Project #5: For the UX Engineer and Interaction Designer

Bad UX is everywhere. There are hundreds of touchpoints out there that could use a little UX love. We find ourselves frustrated by door handles, interfaces, iTunes, automated checkouts, road layouts...the list goes on. 

For this project, you have the opportunity to take a relatively well-known digital site or application with a less-than-stellar customer experience, create a critique of the app, and present some possible solutions with at least one polished high-fidelity mockup. Woo! You have free reign to touch on the information architecture (IA), useful additional features, workflows, terminology, interactions, visual design, etc. 

We want to see your understanding and application of UX principles by demonstrating your process from concept to final solution.

<a href="UX.png" title="UX"><img src="UX.png" alt="UX."></a>

Upon completion of the above, please send us your collection of artifacts and feel free to use a portfolio storage tool like Behance, [Invision](https://www.invisionapp.com), etc. if you'd like. Happy designing!

# Project #6: For the Digital Content Strategist
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
