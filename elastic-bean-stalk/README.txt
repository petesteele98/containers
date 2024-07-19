How to create a image and container then send to AWS

Create empty directory

CD to new directory
Create a Dockerfile - 
FROM nginx
ADD templates/index.html /usr/share/nginx/html
EXPOSE 80

Create an index.html file

To build and tag an image:

docker build -t ‘name of image’ .

To run the container:

docker run --name nginx -p 8080:80 ‘name of image’

Initialise Elastic Beanstalk:

eb init

Default region is 16 (eu-west-2)

Select app or create new

No to creating ssh

Create the app:

eb create 

Enter environment name 

Select application load balancer 

No to spot requests 