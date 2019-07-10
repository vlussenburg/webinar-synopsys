# webinar-synopsys

# Manual setup steps (existing Jenkins)

1. Get access to [Seeker](https://seeker-vm.synopsys-alliances.com:8443/login)

# Spin up an AWS ECS cluster using (any) XL Deploy

1. Clone this repo
1. Install the latest [xl cli](https://docs.xebialabs.com/xl-platform/how-to/install-the-xl-cli.html)
1. Run `xl blueprint` and follow instruction to spin up a `aws/basic-ecs-cluster` and import into any XL Deploy
1. `xl apply -f xebialabs.yaml`, login to XL Deploy
1. Deploy your cluster to AWS
1. Run `xl apply -f ecr/ecr.yaml` and deploy the ecr in XL Deploy
1. Take note of the URI in `Infrastructure/webinar-synopsys/aws-webinar-synopsys/webinar-synopsys-ecr`
1. Install the ECS CLI and do `aws ecr get-login` and login to the ECR
1. Create a file `.env` in the root of your clone with `AMAZON_ECR=<uri>` you found above

# Deploy shit to Amazon

1. Run `docker-compose build` the docker containers should be built
1. `docker-compose push` to push to ECR
