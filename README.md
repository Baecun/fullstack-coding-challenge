# Unbabel Fullstack Challenge

Hey :smile:

Welcome to our Fullstack Challenge repository. This README will guide you on how to participate in this challenge.

In case you are doing this to apply for our open positions for a Fullstack Developer make sure you first check the available jobs at [https://unbabel.com/jobs](https://unbabel.com/jobs)

Please fork this repo before you start working on the challenge. We will evaluate the code on the fork.

**FYI:** Please understand that this challenge is not decisive if you are applying to work at [Unbabel](https://unbabel.com/jobs). There are no right and wrong answers. This is just an opportunity for us both to work together and get to know each other in a more technical way.

## Challenge

We're going to build a very simple translation web app based on the Unbabel API.

You can find more info about the api at [https://developers.unbabel.com](https://developers.unbabel.com)

1) Request an API Key to your hiring manager or point of contact for the hiring process at Unbabel so you can use the API for this tutorial.  
2) Build a basic web app with a simple input field that takes an English (EN) input translates it to Spanish (ES).  
3) When a new translation is requested it should add to a list below the input field (showing one of three status: requested, pending or translated) - (note: always request human translation)   
4) The list should be dynamically ordered by the size of the translated messages   

#### Requirements
* Use Flask web framework
* Use Bootstrap
* Use PostgreSQL
* Create a scalable application. 
* Only use Unbabel's Translation API on sandbox mode
* Have tests


#### Notes
* Page load time shouldnt exceed 1 second


#### Resources
* Unbabel's API: http://developers.unbabel.com/
------------------
## Implementation:

### Features:
- Basic translation functionality as requested
- Inpect any translation individually
- Authentication module along with registration


### Views:
- Login
- Registration
- Translate
- Translation

### Services:
- authentication_service
- translation_service
- database_connection


### Database:
PostgreSQL instance hosted on ElephantSQL.com

#### Model:
- User
    - id (PK)
    - username
    - email
    - password_hash
    - translations (FK)
- Translation
    - id (PK)
    - source_language_id (FK)
    - targert_language_id (FK)
    - callback_url
    - text
    - request_date
    - status
    - translated_text
    - user_id
- Language
    - id
    - short_name
    - full_name


##### Things that would have been interesting to implement:
‘Guest Mode’ with temporary translation requests
Implementing the Database seed method using a file containing the languages
Customized error page
Customized 404 code page


## Running the application:
Since the database is hosted online, there’s no need to set it up manually. All you need to run the app is to execute the command: `python runserver.py` from the project’s main directory.

### Unit tests:
Test coverage is fairly small, but since most methods inside the services are CRUD related, they end up being very similar to each other.
To run unit test, run the following command inside the project directory:
`python -m unittest`

## Test Login information:
For convinience's sake, I created a default user, so that registration isn't absolutely necessary in order to access the application.
###### email: unbabel-fullstack-challenge@unbabel.com
###### password: Unbabel-Fu11st4ck-Dev
