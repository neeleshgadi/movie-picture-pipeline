# Movie Picture Pipeline — Execution Evidence

Repository: https://github.com/neeleshgadi/movie-picture-pipeline  
Pull request: https://github.com/neeleshgadi/movie-picture-pipeline/pull/1

## Successful GitHub Actions runs

- [Frontend Continuous Integration](https://github.com/neeleshgadi/movie-picture-pipeline/actions/runs/34602265373)
- [Backend Continuous Integration](https://github.com/neeleshgadi/movie-picture-pipeline/actions/runs/34602265275)
- [Backend Continuous Deployment](https://github.com/neeleshgadi/movie-picture-pipeline/actions/runs/34610512576)
- [Frontend Continuous Deployment](https://github.com/neeleshgadi/movie-picture-pipeline/actions/runs/34612946543)

## Deployed application evidence

- Frontend LoadBalancer: http://a0604af14c57e473b903108b5de1bdea-1180824653.us-east-1.elb.amazonaws.com
- Backend `/movies`: http://a4c179e5d038a4a39b16789be22ce310-976900741.us-east-1.elb.amazonaws.com/movies

The frontend displays:

- Top Gun: Maverick
- Sonic the Hedgehog
- A Quiet Place

The backend `/movies` response contains the same three movies.

## Kubernetes and ECR verification

- EKS cluster: `cluster` in `us-east-1`
- Frontend deployment: `1/1` available
- Backend deployment: `1/1` available
- Frontend image: `329249488922.dkr.ecr.us-east-1.amazonaws.com/frontend:76ab7ad76dc551d483e889e4e987c53ddde5a5db`
- Backend image: `329249488922.dkr.ecr.us-east-1.amazonaws.com/backend:01c6da9cef8d751c11747cf853b91c57968d32f4`

The corresponding `kubectl get all`, deployment descriptions, and ECR image details were verified after deployment. AWS credentials are stored only as GitHub Actions secrets and are not included here.
