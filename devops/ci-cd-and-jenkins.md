src: TechnicalGuftgu@YouTube

### What is CI/CD Pipeline?
CI/CD stands for continous integration and continous delivery/deployment.
It is a methodology of Software Development Lifecycle (SDLC).
It allows you to automate the process of deployment with early stage identification of errors or bugs.

```
Version Control -> Build -> Unit Test -> Deploy -> Auto Test -> Production Env Deploy -> Measure & Validate (QA)
    |                                                                                                    |
    <----------------------------------- Production Feedback ---------------------------------------------
```
Feedback is provided on every level.

### Things before CI/CD
- Developers had to push their code to vcs.
- The code is then integrated and built in order to spot the bugs.
- The the tester would test the code.

### After CI/CD
- The code directly goes from source code repo to CI server.
- Know the errors are spotted quickly as CI Server informs the developer if there is anything wrong.
- CI server contains all the procedure of build, test, and deploy stuff.

## What is CI (continous integration)?


## Jenkins
Jenkins is an open source automation server. It helps automate the parts of software development related to building, testing, and deploying, facilitating continuous integration and continuous delivery. It is a server-based system that runs in servlet containers such as Apache Tomcat. It supports version control tools, including AccuRev, CVS, Subversion, Git, Mercurial, Perforce, ClearCase and RTC, and can execute Apache Ant, Apache Maven and sbt based projects as well as arbitrary shell scripts and Windows batch commands.

- As Jenkins logo illustrates, Jenkins is kind of valet which serves or carries the necessary things to their next destinations.
- Jenkins is a continous integration tool.
- Alternatives: Bamboo, Buildbot.
- Jenkins is the only open source alternative.
- Jenkins is developed in Java, if you don't have Java installed on your system, you cannot run Jenkins.
- Like Java, it runs on every OS on port 8080.
- It was originally developed by Sun Microsystems in 2004 as project Hudson. Later, Oracle purchased Sun Microsystems and segregated Hudson & Jenkins. Jenkins is free while Hudson is an Entreprise edition (paid).
- Jenkins offers a huge community support and mammoth plug-in library.
- Higher compatibility, consistent UI.
- You can create own plugins for Jenkins.
- Jenkins follows the master slave architecture.

## What happens in a build process?
Compile -> Code Reveiw -> Unit Testing -> Integration Testing -> Packaging (jar)
