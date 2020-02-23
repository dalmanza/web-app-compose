# web-app

#Prerequisite
  1. For runing webapp you need docker-compose in your machine. d
  2. Any browser. However, I'd recomend Google Chrome Or Firefox.
  3. Git. it is necesary to pull the docker-compose file.

#How to start web-app?
  1. Clone this project in your local machine.
  2. Using yout terminal go to your docker-compose file was pulled.
  3. Type this in your terminal: #docker-compose up# you're going to see 
     all the logs generated by: web-app-be and web-app-fe 
     [this process will take some time until both images are downloaded from hub.docker]
  4. Once docker-compose has finished to download the images and run the application, you can,
     using your browser, ingress to the follwing url: http://localhost:4200


#What app-be has exposed?
  app-be has exposed a total of threes endpoints which will be described next:
    1. GET: /portfolio-information/{portfolio-id}
       This will return all information stored in portfolio table.
    2. PUT: /portfolio-information
       This endpoint is encharged of updating information of an specific portfolio.
       You'll need to provide and body [There is one body example in the section #Resources]
       This endpoint updates both 'description' and 'title' the other fields are not being updated
       to not affect others.
    3. GET: /twitter-time-line/{search}
       This endpoint will receive a string with the information to be looked for in twitter.


#Resources
  1. Body example:
      {
        "id": 2,
        "description": "The Mother of Dragons",
        "imageURL": "https://pbs.twimg.com/profile_images/1117967801652617216/i8PWXebo_400x400.jpg",
        "twitterUserName": "Daenerys",
        "title": "Daenerys Targaryen"
      }
    
