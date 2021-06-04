# Infrastructure Monitoring

>>>
**Note:**

This is an an example which defined about the customization of grafana and help in creation of CI/CD of grafana.
>>>

## Overview

This project is a dockerized method to configure grafana at any place either on Cloud or On-prem. 
 

### Detailing about repo :
- It contains a Dockerfile for grafana.
- `dashboard` folder contains dashboard json which help in initializing Grafana with preconfigured dashboards. More json can be also added here to configure more and more dashbaord.
- `provisioning` folder contains information about the datasource to grafana.
- Changes like prometheus endpoint can be made in `datasources/all.yml` .

### Process to run the project.
- Docker client should be install on local system
- Run command from root folder `docker build -t <images_name> .` to build an image using dockerfile.
- Run command `docker run -itd -p 3000:3000 <image_name>` to make container working.
- Browse `http://localhost:3000` to access grafana.
- Use default credentails `admin/admin` to login.


### Limitations.
- It is only for POC purpose so credentails would not be persistance.


