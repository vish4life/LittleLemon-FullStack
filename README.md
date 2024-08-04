# LittleLemon - Web application
Little Lemon is a personal web application developed using Django Rest framework which allows customers to make reservations and also check existing reservations list.
## Tech Stack
* Python
* Django
* Django Rest Framework
* HTML
* CSS
* Javascript (Vanilla)

## Project Requirement
Building the fullstack web application for a imaginary restaurant* "`Little Lemon`"

### The Web application should consist of the following
* Complete functioning web application
    * Header
        * Home
        * About
        * Menu
        * Book
        * Reservations
    * Footer
## Project Structure
* Project folder: LittleLemonProject
    * urls.py
    * settings.py
> `Note: above mentioned are the part of those files which had changes included as part of the project`
* Project App: LittleLemonApp
    * urls.py
    * settings.py
    * views.py
    * models.py
    * templates
    * static
> `Note: above mentioned are the part of those files which had changes included as part of the app`

## Functional Design
* `Header` and `Footer` should get displayed on all the pages of the application
> ### Header
> > Header page consists of the following components
> > * Home page:
> > * * Displays the Hero section with current offers and deals
> > * * Displays thumbnail of Signature dish with information related to restaurant's Menu with a navigation link
> > * * Displays thumbnail of a dish's image which provides an option to book table
> > * * Displays the restaurant's working hours
> > * About page:
> > * * Displays the restaurants origin and speciality
> > * Menu page:
> > * * Displays the Menu items available in the restaurant
> > * Book Page:
> > * * Allows user to enter/select the following for making a reservation
> > * *  * Name
> > * *  * Reservation Date
> > * *  * Reservation Slot
> > * *  * Reserve Button
> > * * On submitting the submission information should get displayed on the right pane under Bookings for section
> > * Reservations page:
> > * * Displays the json data of all the reservations from the system
> > * * Displays the map for the restaurant
> ### Footer
> > Footer page consists of the following components
> > * Little Lemon's Logo
> > * Copy right information
> > * * Displays thumbnail of Signature dish with information related to restaurant's Menu with a navigation link
> > * * Displays thumbnail of a dish's image which provides an option to book table
> > * * Displays the restaurant's working hours

# Technical Design
### Libraries
> Python V3.12.3

> > Pipenv (virtual environment)

> >  Djoser V 2.2.3

> >  Django V5.0.7
> >   * Djangorestframework V3.15.2

> >  mysqlclient V 2.2.4

### Database:
> MySQL

## Code Flow:
### Processing Logic:
* Following outlines the code and functionality of web application

<table>
  <tr>
    <td><h2>Configuration</h2></td>
    <td><h2>Details</h2></td>
    <td><h2>Screenshot</h2></td>
  </tr>
  <tr>
    <td>1</td>
    <td>Is the app added to the installed apps list in the settings file?</td>
    <td>Configuration updated in settings.py file</td>
    <td><img src = "https://github.com/vish4life/LittleLemon-Backend/blob/main/Snapshots_Usecase/01_user_creation_ins_res.JPG"/></td>
  </tr>
  <tr>
    <td>2</td>
    <td>Is the database configuration updated inside the settings file?</td>
    <td>Configuration updated in settings.py file</td>
    <td><img src = "https://github.com/vish4life/LittleLemon-Backend/blob/main/Snapshots_Usecase/01_user_creation_ins_res.JPG"/></td>
  </tr>
  <tr>
    <td>3</td>
    <td>Were migrations performed?</td>
    <td>Yes migrations are performed and database has the tables</td>
    <td><img src = "https://github.com/vish4life/LittleLemon-Backend/blob/main/Snapshots_Usecase/01_user_creation_ins_res.JPG"/></td>
  </tr>
  <tr>
    <td>4</td>
    <td>Are there three fields in the booking form: First name, Reservation date and Reservation slot?</td>
    <td>Booking form shows three fields as mentioned</td>
    <td><img src = "https://github.com/vish4life/LittleLemon-Backend/blob/main/Snapshots_Usecase/01_user_creation_ins_res.JPG"/></td>
  </tr>
  <tr>
    <td>5</td>
    <td>Does a date selector open up when you click on the reservation date field on the booking form?</td>
    <td>Yes date selector allows to pick date and by default shows today's date</td>
    <td><img src = "https://github.com/vish4life/LittleLemon-Backend/blob/main/Snapshots_Usecase/01_user_creation_ins_res.JPG"/></td>
  </tr>
  <tr>
    <td>6</td>
    <td>Are all the bookings available as JSON data on the reservations page?</td>
    <td>Yes Json data / HTML reposonse both are received based on the response method set in views.py</td>
    <td><img src = "https://github.com/vish4life/LittleLemon-Backend/blob/main/Snapshots_Usecase/01_user_creation_ins_res.JPG"/></td>
  </tr>
  <tr>
    <td>7</td>
    <td>Is duplicate booking prohibited on a specific date if the time is already booked?</td>
    <td>No duplicate bookings will be allowed, once the slot is filled it gets disabled for that day</td>
    <td><img src = "https://github.com/vish4life/LittleLemon-Backend/blob/main/Snapshots_Usecase/01_user_creation_ins_res.JPG"/></td>
  </tr>
  <tr>
    <td>8</td>
    <td>Does changing the date refresh the booking data?</td>
    <td>Yes the booking information gets updated immediately</td>
    <td><img src = "https://github.com/vish4life/LittleLemon-Backend/blob/main/Snapshots_Usecase/01_user_creation_ins_res.JPG"/></td>
  </tr>
  <tr>
    <td>9</td>
    <td>Is a duplicate booking on a specific date and time unavailable if the slot is already booked?</td>
    <td>Yes, once the slot is filled it gets disabled for that day</td>
    <td><img src = "https://github.com/vish4life/LittleLemon-Backend/blob/main/Snapshots_Usecase/01_user_creation_ins_res.JPG"/></td>
  </tr>
  <tr>
    <td>10</td>
    <td>Can you display bookings for a specific date using the API?</td>
    <td>Yes, the API endpoint with date will result in the booking details available for that day</td>
    <td><img src = "https://github.com/vish4life/LittleLemon-Backend/blob/main/Snapshots_Usecase/01_user_creation_ins_res.JPG"/></td>
  </tr>
  <tr>
    <td>11</td>
    <td>If there is no booking, does a No Booking message show for that date?</td>
    <td>Yes no bookings will be displayed</td>
    <td><img src = "https://github.com/vish4life/LittleLemon-Backend/blob/main/Snapshots_Usecase/01_user_creation_ins_res.JPG"/></td>
  </tr>
  <tr>
    <td>12</td>
    <td>Was fetch API used to retrieve data from the API?</td>
    <td>Yes the data is retrieved using fetch api</td>
    <td><img src = "https://github.com/vish4life/LittleLemon-Backend/blob/main/Snapshots_Usecase/01_user_creation_ins_res.JPG"/></td>
  </tr>
  <tr>
    <td>13</td>
    <td>Is the current date automatically selected when you open the booking form?</td>
    <td>Yes default date will be current / todays date</td>
    <td><img src = "https://github.com/vish4life/LittleLemon-Backend/blob/main/Snapshots_Usecase/01_user_creation_ins_res.JPG"/></td>
  </tr> 
</table>

`Note 01: Project name: LittleLemonProject and App name: LittleLemonApp`
`Note 02: Templates provided as the base code needs enhancement to correctly function`
