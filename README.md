# Tech Tailors selenoid

## Server info:

- Server name: `tt-dev-one`
- Server IP address: `138.201.50.78`

*Access to the server*

- In order to access the server, contact `ivojinovic` for account creation and credentials
- After you have been granted access, you can access the server using `ssh` command in the terminal on your local machine:

First: `ssh {username}@{server-ip-address}` and hit the `ENTER` key
Then: {password}, `ENTER` key

## Selenoid info:

- Selenoid port on server: `4444`
- Selenoid-UI port on server: `14444`
- Latest browser versions (updated 03.10.2022):
	- Chrome supported versions: `107.0`, `106.0`
	- Firefox supported versions: `106.0`, `105.0`
	- Opera supported versions: `91.0`, `90.0` 

*Access to the selenoid-ui from your local machine*

- In order to access the selenoid-ui from your local machine, you need to set up port-forwarding:
	- On your local machine, open the terminal and type:
	First: `ssh -N -L {PORT_YOU_WANT_TO_USE}:127.0.0.1:{SELENOID-UI_PORT_ON_SERVER} {username}@{server-ip-address}` and hit the `ENTER` key
	Then: {password}, `ENTER` key
- Now open in your browser: `localhost:{PORT_YOU_WANT_TO_USE}` - port you attached in the first terminal command

## Selenoid maintenance and updating:

- Selenoid project: https://gitlab.techtailors.rs/tech-tailors/devops/deploy/selenoid-deployment

### Deployment steps:

- Clone project on your machine
- Make the changes you want
- Commit - Push - Merge
- Go to the project on GitLab
- Go to the CI/CD -> Pipelines:
	- If you want to deploy the latest selenoid changes, run `deploy-selenoid` job
	- If you want to stop selenoid, run `stop-selenoid` job

> Ready to go! HAPPY TESTING!