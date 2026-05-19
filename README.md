#DevOps Setup
Running the stack locally involves using the command: "docker compose up --build -d"

Port 80 is used due to it being the default http port, nginx routes requests coming through http://localhost to the frontend container, while requests to http://localhost/api/ping go to the backend for testing. 

Frontend has a webpage and ui to interact with and linked to backend while backend would be the logic and working code that returns things to display on frontend. Nginx is the service actually handling the webpage and the functioning within a browser, along with routing requests between either frontend or backend given which path is supplied after the ip address. 
