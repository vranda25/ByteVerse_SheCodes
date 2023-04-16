# Udaan
Taking women to new heights

This is a platform created for women artisans to showcase their skills and get employment opportunities. Clients can view the profiles of these women artisans and book them for the services they provide. This project is built using React.js for the frontend and Django for the backend.

## Installation 
This is backend of our project. Frontend can be found at https://github.com/HetviSoni/Udaan-frontend

To run this on your local machine://
Clone the repository//
Move to the project directory//
cd udaan//
Install required modeules: pip install -r requirements.txt//

*Uses simple Jwt Authentication. After registration and Login all APIs require Authentication.//

The backend is also deployed on pythonanywhere. Access the APIs using//
http://udaan.pythonanywhere.com/


## Usage
Women artisans can create a profile and showcase their skills.//
Clients can view the profiles of these women artisans.//
Clients can book an appointment for the services they provide.//
Women artisans can manage their bookings through their profile.//

## Features
User authentication for women artisans and clients.//
Profile creation and management for women artisans.//
Booking management for clients and artisans.//
Booking search and management for clients.//

## Technologies Used
React.js//
Django Rest Framework//
HTML//
CSS//
SCSS//
JavaScript//

## Contributing
If you want to contribute to this project, please follow the below steps://

Fork this repository.//
Clone the forked repository.//
Create a new branch with a descriptive name.//
Make your changes and commit them.//
Push your changes to your forked repository.//
Create a pull request.//


## API endpoints
Register  :  Sign up as either Customer or Business
http://udaan.pythonanywhere.com/api/accounts/register/            
        

Login  :  Login using email and password
http://udaan.pythonanywhere.com/api/accounts/login/

*Uses simple Jwt Authentication. All views requires Authentication.


Business/Profile :  Business can make profile (POST) and see profile (GET)
http://udaan.pythonanywhere.com/api/business/profile/


Business/Skills  : Business can add skills (POST) and see whole profile i.e., profile details+email+all skills (GET)
http://udaan.pythonanywhere.com/api/business/skills/


Business/profile/all  : can see all business profiles(profile+email+only names of skills) (GET)
http://udaan.pythonanywhere.com/api/business/profil/all/


Business/skills/all  : can see all skills of all businesses (only skills with user id ig) (GET)
http://udaan.pythonanywhere.com/api/business/skills/all/


Business/skills/particular  : can see all skills of a particular business (only skills) user id must be provided (GET) (jiske skills dekhne hai uska user id do response me saare skills in detail milenge)
http://udaan.pythonanywhere.com/api/business/skills/particular/


Business/status  : Business can see all services/bookings for her along with status(pending, accepted but not completed, complete) (GET)
http://udaan.pythonanywhere.com/api/business/status/


service/post  : Customer can post a service/book a skill, skill id must be provided (jis skill ke liye booking krni h uss skill ki id dena padegi)(POST), can view list of all his services/booking (GET)
http://udaan.pythonanywhere.com/api/service/post/


service/status  :  Business can change status of a service, service id and status must be provided by default status is pending(POST) (business ko service accept krna h to “status” : “2” n decline krna h to “status” :  “3”)
http://udaan.pythonanywhere.com/api/service/status/

“1” : pending
“2” : accept
“3” : decline


service/completed  : Customer can check is_completed for his/her bookings only if service status is “accepted” (bina business ke accept kiye service complete kese ho skti h ) and increases job_completed for a particular business
, service id must be provided (POST) (jo service complete ho gai h usse customer is_completed kr skta h)
http://udaan.pythonanywhere.com/api/service/completed/


service/rating  : Customer can give rating to a service that is completed, service id must be provided (POST), anyone can view rating provided for a particular service,service id must be provided (GET)
http://udaan.pythonanywhere.com/api/service/rating/


service/rating/all  : all ratings of a particular business, user id must be provided (GET)
http://udaan.pythonanywhere.com/api/service/rating/all/


Business/history/all  : list of all services completed by a particular business, user id must be provided (GET), gives customer_name, skill_name, rating of services
http://udaan.pythonanywhere.com/api/service/history/all/


