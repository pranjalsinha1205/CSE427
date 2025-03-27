# CSE427
Cloud computing practical
----------------

| docker       |

----------------
| guest os     |

----------------
| hypervisor   | --------------------------> Container Model

----------------
| host os      |

----------------
| h/w          |

________________

this model is called the container model. why?
because they allow the application to be executed without depending on OS.

container is an isolated place where an app can run its code.
_______________

|             | 

| Application | --> container 

|_____________|

An image is responsible for running a docker file, if u dont have an image u wont be able to run it

Flag-> Flags in linux are also known as options and they play a very crucial role of modifying the behaviour of commands and they enable additional functionalities

# Commands
***13/03/25***
>> suo apt install docker.io
>> 
>> docker pull busybox // pulling an image called busybox
>> 
>> docker run -it busybox sh // loading the image, -it is a flag, it means interactive, sh means shell it is going to open the shell, busybox is an image name
>> 
>> exit // to return away from the busybox os and return back to ubuntu
>> 
>> docker ps // shows only running containers
>> docker ps -a // will give all the containers stopped running whatever
>>
>> //Building an image
>>
>> mkdir BuildingOne
>> 
>> cd BuildingOne
>> 
>> nano index.html
>> 
>> nano Dockerfile //configuration file required for docker to work
>> 
>> // inside the docker file, we are building our docker image
>>
>> docker build -t foldername .
>> 
>> docker build -t file .
>> 
>> docker run -d -p 8090:80 foldername
>> // now we get the webpage



busybox is a linux os

docker build, it needs a few things:-

i) folder

ii) configuration file

iii) content

Dockerfile

***Use the official Nginx image as the base***

FROM nginx:latest

***Copy file.html to the default Nginx HTML directory***

COPY index.html /usr/share/nginx/html/index.html

***Expose port 80 to allow access***

EXPOSE 80

***Start the Nginx server***

CMD ["nginx", "-g", "daemon off;"]
