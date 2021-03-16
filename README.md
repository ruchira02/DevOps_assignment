# DevOps_assignment

Assignment : Dockerfile - Build image with loaded MySQL schema 

Steps to solve this Assignment

Step 1: Pull the latest code 
	  Open terminal & type following command
    
    git clone https://github.com/ruchira02/DevOps_assignment.git
         
Step 2: Go to cloned repo-directory and Build image
	
    cd DevOps_assignment
	  
    sudo docker build . -t assignment_2

Step 3: Start the container
    
    sudo docker run --name pucsd_assignment_2 -p 4040:4040 -d assignment_2

Step 4: Connect to MYSQL using a bash shell
	  
    sudo docker exec -it pucsd_assignment_2 /bin/bash

Step 5: It will take you to the root, then start MYSQL with username: pucsd and password: pucsd
    
    mysql -upucsd -ppucsd

Step 6: After successful connection with MYSQL we can see database: pucsdStudents & table: studentData
	
    Use pucsdStudents;
	  
    select * from studentData;
