# healthcare-services
Adding a service for tracking the status of enrollees in a health care program.
##Swagger Url: It is used for testing the rest Api's
##Junit5 Test cases also added.
http://localhost:8080/swagger-ui.html#

## Api's overview
Api 1:Api to add a new enrollee

Request:
Url: http://localhost:8080/enroll/addEnrollee
Body:
{
  "activationStatus": true,
  "dateOfBirth": "1992-04-14 12:15:22",
  "dependentDetails": [
    {
      "dependentDOB": "1992-04-14 12:15:22",
      "dependentName": "string"
    }
  ],
  "enrolleeName": "test1",
  "phoneNumber": "2343423"
}

Response:
Added new enrollee successfully

Api 2:Modify an existing enrollee

Request:
Url:http://localhost:8080/enroll/modifyEnrollee?enrolleId=1
Body:
{
  "activationStatus": true,
  "dateOfBirth": "1922-04-14 12:15:22",
  "dependentDetails": [
    {
      "dependentDOB": "1292-04-14 12:15:22",
      "dependentName": "wew"
    }
  ],
  "enrolleeName": "test123",
  "phoneNumber": "43534534"
}

Response:
Modified an existing enrollee successfully

Api 3: Remove an enrollee entirely

Request Url:
http://localhost:8080/enroll/removeEnrollee?enrolleId=1

Response:
Enrollee removed successfully

Api 4:Add dependents to an enrollee

Request Url:
http://localhost:8080/enroll/addDependents?enrolleId=4

Body:
[
  {
    "dependentDOB": "1922-04-14 12:15:22",
    "dependentName": "sd234"
  },
{
    "dependentDOB": "1932-04-14 12:15:22",
    "dependentName": "sd2324"
  }
]

Response:
Added dependents to an enrollee successfully

Api 5: Remove dependents from an enrollee
Request Url: 
http://localhost:8080/enroll/deleteDependents?enrolleId=4

Response:
Removed dependents of an enrollee successfully

Api 6:Modify existing dependents
Request Url: 
http://localhost:8080/enroll/modifyDependents?id=3
Body:
{
    "dependentDOB": "1922-04-14 12:15:22",
    "dependentName": "asdasd32"
  }
  
 Response:
 Modified existing dependents successfully


