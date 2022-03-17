# Deploying plotly app on GCP
Pre-requisites: Google cloud Trial account, gcloud shell (command line interface)

- Step 1: Clone this repository
- Step 2: Go to the tut_1 folder on the command line interface (terminal/Powershell)
- Step 3: run ```pip3 install requirements.txt```
- Step 4: Run the following commands
```
gcloud builds submit --tag gcr.io/<ProjectID>/dash-youtube-example  --project=<ProjectID> .
```
The gcloud builds submit command:

  - compresses your application code, Dockerfile, and any other assets in the current directory as indicated by .;
  - uploads the files to a Cloud Storage bucket;
  - initiates a build using the uploaded files as input;
  - tags the image using the provided name
  - pushes the built image to Container Registry.


```
gcloud run deploy --image gcr.io/<ProjectID>/dash-youtube-example --platform managed  --project=<ProjectID> --allow-unauthenticated
```
