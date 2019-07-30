# webinar-synopsys

# Manual setup steps (existing Jenkins)

1. Get access to [Seeker](https://seeker-vm.synopsys-alliances.com:8443/login)

# One time setup

1. Add `ADMIN_PASSWORD`, `XLD_LICENSE` and `XLR_LICENCE` (the licenses base64 encoded) variables in a `.env` file in the same folder as the `docker-compose.yml`, like so:
```
ADMIN_PASSWORD=

XLR_LICENSE=

XLD_LICENSE=
```
1. Add to the `secrets.xlvals` in the `xlr` folder, adding the secret values obviously: 
```
xld_password =

jira_username =
jira_password =

blackduck_password =

seeker_token =

snow_password =
```

1. Install Docker and do open up the TCP port [see here](https://redtalks.live/2017/05/26/redtalks-18-enabling-the-docker-tcp-api-in-aws/)

# Deploy shit to Amazon

1. `git clone https://github.com/xebialabs-external/webinar-synopsys.git`
1. Run `docker-compose build` the docker containers should be built

1. `docker-compose up -d` 


```

The filters to surface would be, 
“Severity (enumeration)“, 
“Seeker Verified (true/false)“, 
Important: Version (free form text)


Nice to have: Checkers (multi selection list), date/time range 
```
