# aws-serverless-open-telemetry
Reviewing and using open telemetry


To run this you need to do it within Docker since the libraries need to compile in Linux:
```
docker build -t serverless-otel .

docker run --rm --name otel -it -e AWS_ACCESS_KEY_ID=##accesskey## -e AWS_SECRET_ACCESS_KEY=##secretkey## serverless-otel bash
```

The second command connects to the server.  Once you are there, deploy the application by running `npm run deploy`.  When the application is successfully deployed, then you could run the command `sls invoke -f hello` multiple times so that the counter gets executed.