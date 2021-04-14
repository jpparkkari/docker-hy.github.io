# [Course material](https://jpparkkari-coursepage.herokuapp.com)

## DevOps with Docker course exercise 3.1

This Docker app runs the course web pages.
Image is also submitted to docker hub with name jpparkkari/coursepage

There is docker-compose.yml with Watchtower, which pulls the latest docker hub image, if the app is started with docker-compose up.

Github Actions pipeline first updates the Docker hub image and then also pushes container to Heroku. 
There maybe would have been alternative ways to do the Heroku deployment:
1. run watchtower in Heroku, so it would automatically pull the latest image. That just wasn't the purpose of this exercise.
2. connect the Heroku app to Github repo, so it would pull the latest version from there. Also that wasn't in line with the exercise idea in my opinion. That also might need bit more testing and restricts from committing straight to main branch.
3. skip updating the docker hub image and push the image just to heroku. Most possible from these three, but I wanted to have some consistency. Without the docker hub, watchtower wouldn't work, and that might still be used later in this part of course. Or maybe I need to come back to it later.



