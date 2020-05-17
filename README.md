
# Work Day Scheduler 

# Synopsis
This is a simple calendar application that allows the user to save events for hours 9 - 6 pm of the day. This app will run in the browser and feature dynamically updated HTML and CSS powered by jQuery.

# User Story

AS AN employee with a busy schedule
I WANT to add important events to a daily planner
SO THAT I can manage my time effectively


# Screenshot 
<img width="799" alt="Screen Shot 2020-05-17 at 1 06 53 PM" src="https://user-images.githubusercontent.com/56641651/82154955-5edb1880-983f-11ea-85a0-02b7552b7103.png">

# Acceptance Criteria 
The project fulfills the below acceptance criteria: 

* GIVEN I am using a daily planner to create a schedule
* WHEN I open the planner
* THEN the current day is displayed at the top of the calendar
* WHEN I scroll down
* THEN I am presented with timeblocks for standard business hours
* WHEN I view the timeblocks for that day
* THEN each timeblock is color coded to indicate whether it is in the past, present, or future
* WHEN I click into a timeblock
* THEN I can enter an event
* WHEN I click the save button for that timeblock
* THEN the text for that event is saved in local storage
* WHEN I refresh the page
* THEN the saved events persist

# Sample Code

```
$(document).ready(function(){
  // create a var to call the id 
  var currentDateEl = $("#currentDay");
  // create a var to detect the current date
  var curDate = moment().format('MMMM Do YYYY');
  currentDateEl.text(curDate);
});
// function to save input from text area 
$(".saveBtn").click(function(){
  // var to target the text area for each specific time block
  var textValue=$(this.parentNode.children[1]).val();
  // code to save the text area items in local storage 
  localStorage.setItem($(this).attr("id"),textValue);
});

```


  
 # Installation
To use this portfolio, log into your GitHub account (if you don’t have a GitHub user profile, create one at https://github.com/join) and open this link in your browser: https://github.com/natashagils/Homework5-Scheduler. Then click on the "Fork" button at the top right corner and wait until the repo is forked. 



