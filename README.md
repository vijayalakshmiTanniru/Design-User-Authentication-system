# Design-User-Authentication-system
Covid-19 India Portal
Given two files app.js and a database file covid19IndiaPortal.db consisting of three tables state, district and user.

Write APIs to perform operations on the tables state, district only after authentication of the user.

The columns of the tables are given below,

State Table

Columns	Type
state_id	INTEGER
state_name	TEXT
population	INTEGER
District Table

Columns	Type
district_id	INTEGER
district_name	TEXT
state_id	INTEGER
cases	INTEGER
cured	INTEGER
active	INTEGER
deaths	INTEGER
You can use your previous code if required.

Sample Valid User Credentials
API 1
Path: /login/
Method: POST
Request

Scenario 1

Description:

If an unregistered user tries to login

Response
Status code
400
Body
Invalid user

Scenario 2

Description:

If the user provides an incorrect password

Response
Status code
400
Body
Invalid password

Scenario 3

Description:

Successful login of the user

Response

Return the JWT Token

Authentication with Token
Scenario 1

Description:

If the token is not provided by the user or an invalid token

Response
Status code
401
Body
Invalid JWT Token

Scenario 2
After successful verification of token proceed to next middleware or handler

API 2
Path: /states/
Method: GET
Description:
Returns a list of all states in the state table

Response
API 3
Path: /states/:stateId/
Method: GET
Description:
Returns a state based on the state ID

Response
API 4
Path: /districts/
Method: POST
Description:
Create a district in the district table, district_id is auto-incremented

Request
Response
API 5
Path: /districts/:districtId/
Method: GET
Description:
Returns a district based on the district ID

Response
API 6
Path: /districts/:districtId/
Method: DELETE
Description:
Deletes a district from the district table based on the district ID

Response
API 7
Path: /districts/:districtId/
Method: PUT
Description:
Updates the details of a specific district based on the district ID

Request
Response
API 8
Path: /states/:stateId/stats/
Method: GET
Description:
Returns the statistics of total cases, cured, active, deaths of a specific state based on state ID

Response

Use npm install to install the packages.

Export the express instance using the default export syntax.

Use Common JS module syntax.
