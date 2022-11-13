# Learning-CloudRun
# Requirement
- Docker
- [gcloud-sdk](https://cloud.google.com/sdk/docs/install-sdk)

# Setup
- Build

```bash
$ docker build -t learning-cloudrun:latest .
```

- Start

```bash
$ docker run -p 3000:3000 learning-cloudrun:latest
```

# Deploy to CloudRun

- gcloud login

```bash
$ gcloud auth login
```

- Submit a build image to GCR

```bash
$ gcloud builds submit --project PROJECT_ID --tag gcr.io/PROJECT_ID/learning-cloudrun
```

- Deploy

```bash
$ gcloud run deploy --image gcr.io/PROJECT_ID/learning-cloudrun --platform managed
```
