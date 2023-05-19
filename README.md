# Intulse Technical Interview (Part 2)

The purpose of this co-working project is to see how you work in a modern Angular environment and familiarize us with your personal development style.  This is a free-form project and there is not a specific expected solution. 

You are encouraged to:
1. Ask questions
2. Search the internet
3. Discuss technical choices

## Estimated Time
We expect the project to take anywhere between `30` to `60` minutes.

## Prerequisites
You will need to have completed [Part 1](https://github.com/intulse/interview) of Intulse's technical interview.

## Tools
- Visual Studio Code
- Node.js 18+

## Required Technology
- [Angular 13+](https://angular.io/)

## Objectives

- [ ] Create a new Workspace in an empty folder using Visual Studio Code
- [ ] Create a new Angular project using the Angular CLI inside Visual Studio Code
- [ ] Create a new file in your Angular project named `demo-data.interface.ts` and in it code an interface named `DemoData` to match the data returned from the endpoint you created Part 1 of the interview project `/demo/call-summary`
- [ ] Edit the Typescript portion of the root component in your new Angular application:
  - [ ] Add a reference to your `DemoData` interface type
  - [ ] Add a public property named `demoData` of type `DemoData` which is `null` by default
  - [ ] Add a public property named `loading` of type `boolean` which is `true` by default
  - [ ] On initialization of the component make an HTTP GET request to the endpoint you created in part 1 of this technical interview (e.g. `http://localhost:12345/demo/call-summary`) such that the returned data is of type `DemoData`
  - [ ] When the call completes
    - [ ] Set the `demoData` property equal to the the returned data
    - [ ] Set the `loading` property to `false`
- [ ] Edit the HTML portion of the root component in your new Angular application:
  - [ ] Create a DIV that only displays when the component property `loading` is `true` with the content "Loading..."
  - [ ] Create a DIV that only displays when the component property `loading` is `false` with the following content inside
    - [ ] A table with headers for `Hour`, `Calls`, `Total Duration`, `Avg. Duration`
    - [ ] The table should have one row for each entry in `demoData.hours`
    - [ ] The table should have a footer row which displays values in `demoData.totalCalls`, `demoData.totalDurationInSeconds`, and `demoData.avgDurationInSeconds` in the corresponding columns
- [ ] Run your project using `npm start`
- [ ] Make certain your Part 1 project is running
- [ ] Open a browser and browse to Angular application where should see a simple screen with a loading indicator which changes to a table displaying the demo data

## Bonus

- [ ] Build an injectable `DemoApi` class to wrap the HTTP client
- [ ] Use dependency injection to inject the DemoApi into the root app component and use it to make the HTTP GET request
