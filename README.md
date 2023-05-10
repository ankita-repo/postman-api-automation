# postman-api-automation
Sample rest api testing using postman script

Prerequisite on your system:
1. Node installed
2. Npm install 
3. Install below package globally
    i. npm install -g newman
    ii. npm install -g json-server

Ref:
i. https://www.npmjs.com/package/newman 
ii. https://www.npmjs.com/package/json-server    

Steps to run: 

1. Run the rest api serice using below command
 json-server .\db.json

2. Run the postman automation
    newman run .\employee-rest-api-testing.json -e .\LOCAL_ENV.postman_environment.json -n 5

Some error occurred Error: listen EADDRINUSE: address already in use ::1:3000
To kill process working on existing node
    netstat -ano | findstr :<PORT>
    taskkill /PID <PID> /F
    Ref: https://stackoverflow.com/questions/39632667/how-do-i-kill-the-process-currently-using-a-port-on-localhost-in-windows

