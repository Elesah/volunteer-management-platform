
# Functional requirements 
This platform will help manage the activities of volunteers working with institutionalised children. 

- Successful signup/login with the various roles from the organization (volunteers working directly with children, centre coordinators, city coordinators, country coordinators and TBD)
- Successful deletion of account for users
- Successful export of user information
  
- **Volunteers** working directly with children should be able to do the following: 
  - add the following information about themselves : name, availability, email, phone, number, type of help they can provide, facebook (optional), description                 (optional), their volunteering contract (optional)
  - add an entry for every visit/hangout they have with the children which will contain: centre name/place, time of the activity, length of the activity, names of             children, their age, other volunteers involved,, description of the event, additional important information (optional)
  - be able to edit an entry for up to a month of submitting
  - see history of their activities (as well as activities in which they had been tagged)
    - see hours they've spent volunteering (week/month/year TBD)
  - see all the acitivities history for peers volunteers
  - see hours spent volunteering at their centre(s) (for that month/week/year TBD)
      
- **Centre coordinators** should be able to do everything regular volunteers can do, and a couple of other specific activities:
      - add regular volunteers to their centre    
      - confirm accounts for regular volunteers assigned to their centre(s)
      - edit availability for regular volunteers assigned to their centre(s)
      - remove volunteers from their centres
      - see hours spent volunteering for every regular volunteers assigned to their centre(s) (for that month/week/year TBD)
      - mark a volunteer as non-active 

- **City coordinators** should be able to do everything centre coordinators do and a couple of other specific activities:
     - confirm accounts for centre coordinators
     - add an existing account as a centre coordinator (there can be max of two centre coordinators)
     - remove volunteers as centre coordinators
     - mark centre coordinators as non-active
 
- **Country coordinators** should be able to do everything city coordinators do and a couple of other specific activities:
     - confirm accounts for city coordinators
     - add an existing account as a city coordinator (there can be max of two city coordinators)
     - remove volunteers as city coordinators
     - mark city coordinators as non-active
     - remove a country coordinators
     - mark other country coordinators as non-active
 
- **Admins** should be able to do everything country coordinators do and a couple of other specific activities:
    - assign country coordinators
 

# Technical details

## Features

* [Clean architecture](https://blog.cleancoder.com/uncle-bob/2012/08/13/the-clean-architecture.html) structure
* Symfony 5
* docker-compose configuration with separate fpm container
* Performance improvements for dev: separate cache and logs volumes, vendor folder excluded from mounting

## Running

* Use docker-compose 
* Access [http://localhost:5000/](http://localhost:5000/)


## // todo:

* ~~github~~
* production: separate image targets
* production: make cache-warmup with root user instead of having cache folder www-data writable.
* entire deployment pipeline
* production: not depend on .env file
* install phpunit-speedtrap
* figure out a way for easy composer commands since no longer mounting /vendor folder
