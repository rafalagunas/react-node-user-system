## Configuration

1. clone this repo with both submodules repos (front and back)

git clone --recurse-submodules https://github.com/rafalagunas/react-node-user-system.git

2. Enter to the folder containing docker-compose and both submodules (front and back)

cd user-system

3. build docker composer

docker-composer build

4. run docker composer

docker-composer up

4. That's it, you're now able to try the api using the following ports:

- http://localhost:8080 for api

### Available routes for api:

POST /user/create => create user
POST /user/admin => admin login
POST /user/login => login for normal users
GET /user/validate_token => validate a token included in the header as Bearer token
POST /user/add_information => update information

\*full examples included in the postman_collection.json

- http://localhost:3000 for frontend

### Available routes for frontend:

/ => register
/login => login
/update_profile => to update profile, username and password are required to be the same to update the information
/admin => administrator login, prints in the console.log and in a simple alert the users array from database containing all users

## Postman

1. postman_collection.json contains the needed requests to test the api

### Important notes:

- You will find in the **screenshots** folder specific files for every validation/use case

- To improve:

- Controllers abstraction
- Full unit testing to get a good % of coverage
- Finish CI integration using Circle CI for both repositories and the main one, for testing and deploying for every stage
- Postman documentation to complete
