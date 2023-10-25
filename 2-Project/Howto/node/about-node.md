
### step 1
- jsut accept defult
- don't check fig

npm install express@4.10.1


### upgrade required 
if port is listenning 


Try changing the port from 3000 to something else.

I just ran into this issue when a coworker tried running an express app we've been building on a Windows machine for the first time, as opposed to an EC2 instance. I've been using a Mac during development.

> The issue seemed to be that 0.0.0.0:3000 was already mapped on company Windows machines. If you run netstat -an in a command prompt you may see it in use already.

### who's listening

netstat -an

