

# Frontend Coding Task


## Introduction

Imagine you own a rental business like Roadsurfer. You have a bunch of campervans and rental stations around the globe. Your customers pick up and return campervans at your stations. Your station personnel are kept busy handing over and processing the returned vans. 
To make your station staff’s lives easier, their work more efficient, and to improve transparency between all departments, you decide to create a calendar-like dashboard web-app, which based on the existing bookings displays all planned pickups (booking start date) and returns (booking end date) of campervans at every station.

For the sake of simplicity, let’s agree that a booking should be returned to the same station where it was picked up.

## Setup

 - Use a framework of your choice (Vue.js, Angular, React). If you are not sure which, choose vue.js
 - Please take care of some simple (or sophisticated - it is up to you ;) ) styling (recommended, but not required, would be to use tailwindcss)
 - Host your code in GitHub and publish your web-app on a GitHub Page https://pages.github.com/
 - In terms of the UX, the freedom is all yours: if the explanation below is not explicit enough, just come up with your own UX
 - Layout of your web-app should be designed keeping the “mobile first design” principle in mind.

## To do
- Create from scratch a reusable component “autocomplete”: a field with an autocomplete function
  - While the user types in the field, the remote API is queried to perform a search based on the text entered
  - After the user has clicked on one of the suggested results, the value is selected and an event to notify any interested handlers is triggered
- On a responsive grid create mobile and desktop views for the following page:
  - A week view (UX / UI is up to you)
    - Calendar-like week view (7 tiles, one for each weekday)
    - Pagination to switch weeks
    - Station selector: reuse your component “autocomplete”, for choosing a station (a station where the booking starts or ends). The source data of stations can be queried here: https://605c94c36d85de00170da8b4.mockapi.io/stations
    - On every day-tile, display bookings that start or end on that day at the selected station.
    - When a booking is clicked, a new view with booking details is opened (see “A booking detail view”)
    - **Optional**: A station employee can reschedule the pickup or return day of the booking by drag-and-dropping it (you can store the changes locally and emulate an API call - output the imaginary API call as text to the console)
  - A booking detail view (UX / UI is up to you)
    - Booking information can be retrieved here: https://605c94c36d85de00170da8b4.mockapi.io/stations/{station-id}bookings/{booking-id}
    - Display booking details:
      - Customer name
      - Booking Start Date
      - Booking End Date
      - Booking Duration
      - Pickup-Return Station Name
    - Action to return to the calendar view
- **Optional**: Introduce state management to your application (it is up to you to choose the level of complexity of the state management and in what part of the application you use it)
- **Please write unit tests for your code!**
