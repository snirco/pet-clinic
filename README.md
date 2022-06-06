# pet-clinic

In order to run this pipeline you will need the following:
1. Jenkins installed
2. plugins: docker, docker-pipeline, github.
3. create a new pipeline, use the configuration as seen in the following screenshot

![image](https://user-images.githubusercontent.com/25568324/172248645-14725770-4f58-4a60-aeb6-447eee65aef7.png)

set script path to 'Jenkinsfile'
run 'build now' inside Jenkins UI.

Some work done on this:
As mentioned, it really was 100% new to me unfortunately..
I had to learn all the syntax, configurations and setup needed to get started which definitely took many hours.
I obviously didn't manage to complete the assignment but I did learn a lot working on it which was fun (and frustrating sometimes).
I'm now more familiar with CI/CD pipelines, working with containerized images etc.

I think the next piece would have been figuring out the correct way to package the docker image, base it on the corrent base image and have it pushed to either dockerhub or this repo.

I didn't get to touch on the bonus part unfotunatelly.
