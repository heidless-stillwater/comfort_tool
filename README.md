# CBE Thermal Comfort Tool

https://github.com/CenterForTheBuiltEnvironment/comfort_tool.git

https://cloud.google.com/run/docs/quickstarts/build-and-deploy/deploy-python-service

## RUN/INSTALL
```
# local
gunicorn comfort:app --reload

# docker
docker build . -t comfort-tool

docker run --rm --name comfort-tool -e PORT=3000 -p 3000:3000 comfort-tool

# access docker shell
docker exec -it comfort-tool bash

# check exists
docker image ls

# gcloud

gcloud builds submit --tag gcr.io/pfolio-deploy-1/comfort-tool

gcloud run deploy --image gcr.io/pfolio-deploy-1/comfort-tool --platform managed --port=3000

```




A web interface for comfort model calculations and visualizations according to ASHRAE Standard-55, EN Standard 16798 and ISO Standard 7730. 

[Live deployment of the tool](http://comfort.cbe.berkeley.edu/).

[Official documentation](https://center-for-the-built-environment.gitbook.io/thermal-comfort-tool/)

[Contribute to the project](https://center-for-the-built-environment.gitbook.io/thermal-comfort-tool/contributing/contributing)

[How to deploy](https://cbe-berkeley.gitbook.io/thermal-comfort-tool/contributing/contributing#deploying)