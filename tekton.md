 kubectl apply --filename https://storage.googleapis.com/tekton-releases/pipeline/previous/v0.26.0/release.yaml
 clear
 k get ns
 k get pods -n tekton-pipelines
 kubectl apply --filename https://storage.googleapis.com/tekton-releases/dashboard/latest/tekton-dashboard-release.yaml
 get pods -n tekton-pipelines
 kubectl apply --filename https://storage.googleapis.com/tekton-releases/pipeline/previous/v0.26.0/release.yaml
 kubectl get pods -n tekton-pipelines
 get svc tekton-dashboard -n tekton-pipelines
 
 The Tekton Dashboard Service is exposed on port 9097. So, set up a port forward for the tekton-dashboard Service on port 9097:

kubectl port-forward -n tekton-pipelines --address=0.0.0.0 service/tekton-dashboard 80:9097 > /dev/null 2>&1 &
