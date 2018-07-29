# CLASS04 - FINAL PROJECT

Main repository for the final project for Class 04

![amaHeadlineLogo](./images/ama-headline-logo.png)

## Work Agreement

[https://github.com/dpfernandes/class04-final-project/blob/master/WorkingAgreement.md](https://github.com/dpfernandes/class04-final-project/blob/master/WorkingAgreement.md)

“Working agreements are guidelines that define how groups want to work together, and what they want in the working environment and from each other to feel safe and free to learn, explore and discover.”_

Read the agreement and live up to it. Your project and team work has to have rules so you develop and communicate in the same way and follow up on each others work! **A finished project is only a sucesss if you did it together and learned together.**

Feel free to review the points and contribute/pull request with new ones.

Note that the project is split into two sub-projects. One for the [client](/client) and one for the [server](server). Further documentation in these folders.

![Archiv für die Musik Afrikas - Universität Mainz](./images/ama1.png)

## Work stories

### First iteration

##### 1A: When I want to find a specific music I want to be able to search for specific music title

##### 1B: When I want to find a specific artist I want to be able to search for specific artist - be aware that there are albums that have more than one artist;

##### 1C: When I want to find a music from a specific year I want to be able to search for specific year

###### Build an UI using the mockup below as a guideline for:

      > A List View story of what you can search on the DB - use storybook and build the components
      for the view;

      > A Search View - use storybook and build the components for the view. Use the data on the
      JSON file to demo;

![mockupSearchView](./images/mockupSearchView.png)

      > Search Result View for the Artist with the info about the about Albums that are related to him/her;

![mockupSearchResult](./images/mockupSearchResult.png)

      > Detail View for the Album with the info it's info, list of the titles with a Player for each
       one of them;

![mockupDetailView](./images/mockupDetailView.png)

      > A Sort Search results based on Alphabetic order by Artist or by song Title and by Chronologic order.
      This component should show up in every list result view.

###### Build a Database Diagram based on the JSON file. Use the example below:

![dbDiagram](./images/dbDiagram.png)

###### Please check the JSON file in

[database-24fdbd.json](./database-24fdbd.json)

###### Implement Elastic Search using Isaac Project as an example and Ahmed’s endpoint

[https://github.com/katsisaac50/myreactivesearch](https://github.com/katsisaac50/myreactivesearch)

###### Make a Sitemap with the different Pages using the example below

![sitemapExample](./images/sitemapExample.png)

###### Make a diagram of the API endpoints using the example below

![apiEndPoints](./images/apiEndpoints.png)

You can use AMA Instagram to get some images and add some real content to your project.
Check AMA Instagram here: [https://www.instagram.com/reboot.africa](https://www.instagram.com/reboot.africa)

### Second iteration

- Work on the data model and import it in MySQL
  - Use Knex.js to create the data model and the migrations
  - [Optional] We found that using docker to start the MySQL instance simplifies it a bit (the ports format: external:internal external meaning exposed in localhost)
    - `docker run --rm -e MYSQL_ROOT_PASSWORD=password -d -p 3306:3306 mysql:8.0.11 --default-authentication-plugin=mysql_native_password`
- Data structure
  - [TODO] Write about some of our record/field choices
  - [TODO: Get latest] Data model
    - ![Data Model](./images/dataModel.png)
- [WIP] Use AWS to host the music files
- [WIP] Use Discogs api to get more data
- [Needs Design] Create static pages: Contact, About, FAQ (if needed)

### Third iteration

TBD

## Process

We suggest the following process for working on the project:

1. Understand the product. Why is it necessary? What does it do and how does it do it?
2. Decide on what your architecture will look like. This is mostly given, since all classes have been focusing on a single type of architecture, but make sure you understand what you are building and why you are building it.
3. Get a simple "hello world" style of prototype running utilizing the entire stack (i.e. have the React application query the API that will return a string of text fetched from the database). Don't try to implement the actual application yet. Make sure that functionality such as connecting to the database is
4. Break the UI into a component hierarchy.
5. Design a data-model for your database that will allow you to store and query the data you need.
6. Build a migration script that will allow you to easily set up any tables you need in your database and fill it with test data.
7. Build a static version of the UI. Don't worry about functionality yet. If you discover discrepancies in your component break-down as you build, update the breakdown.
8. Start thinking about what components should be stateful. Add container components as needed.
9. Start wiring up all of the functionality, fetching the data from the API and implementing real functionality as opposed to having just static components.
10. Plan development so you can stop developing any new features in the last 10-15% of the project (4-6 days). Use this time as a "feature freeze" period, where you focus on "hardening" the product by testing and fixing bugs.

## Working with GIT and handing in iterations

We expect to see running code at a regular frequency, so the product has been broken up into iterations. You are expected to finish approximately one iteration per week. We expect to see each iteration as a _pull request_ on github so we can give you feedback directly in code.

To hand in and get feedback on your iterations you must follow this process for working with git and github:

- _One_ member in each group must make a fork of the [original repository](https://github.com/HackYourFuture-CPH). A fork means that you are making a copy of the repository on your own github profile.
- The member who has made that fork must go to settings and add his team members and the mentors as collaborators
- Whenever you start working on an iteration make a new branch from the master branch and name it accordingly (ì.e. `iteration-1`)
- It is recommended that each team member make a branch off of the `iteration-1` branch and name it based on the work he or she is going to be doing (i.e. `work-story-1a-api-endpoints` if you are going to be working on API endpoints for the work story 1A)
- When you have managed to make the new code work on your local computer, commit your work to your personal branch and push it to github.
- In the github interface find your personal branch and make a pull request towards the `iteration-1` branch. Share the link with your team member(s) and ask for feedback.
- All team members should read through pull requests from other members and do as much as they can in terms of asking questions and researching in order to understand what other members have done. The team members should perform a review and either approve or request changes to the code before it can be merged.
- Once the other team members have reviewed the pull request, go to the github interface and merge the pull request.
- Once you have an iteration ready and need feedback from the mentors, make sure all work is merged to the `iteration-1` branch and then create a pull request towards the `master` branch. Post the pull request link in the main Slack channel.

To get feedback before a sunday session, pull requests must be created saturday at midnight the latest.

If you are worried that only one member will have the project on his or her github, there is no need. People can see any contributions you make to open source repositories whether it is on your profile or not. After the project is finished we recommend that the remaining team members fork the finished repository from their teammate, to make it easier to showcase the project on their account.
