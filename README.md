# plotly_gcp
Deploying plotly on gcp

Run the following command 

```
gcloud builds submit --tag gcr.io/<ProjectID>/dash-youtube-example  --project=<ProjectID>

```
```
gcloud run deploy --image gcr.io/<ProjectID>/dash-youtube-example --platform managed  --project=<ProjectID> --allow-unauthenticated
```