## Kubernetes example hello-app

This repository includes Kubernetes example with deployment and LoadBalancer service.
* hello-app deployed by using yaml-file with deployment/replicas:3
	* hello-app image: gcr.io/google-samples/hello-app:2.0
	* yaml file name for deployment: `hello_app_deployment.yaml`
* Expose the service and test it with the curl request: curl http://<ip address of exposed service>:8080
	* LoadBalancer service used
	* yaml file name for LoadBalancer service : `hello_app_serviceLB.yaml`
* In order to test with curl another test-container/pod created
	* yaml file name for test continer/pod : `hello_app_test.yaml`
	* curlimages/curl:7.78.0 image is used which includes curl inside
	* command `curl http://helloapp:8080` is used
