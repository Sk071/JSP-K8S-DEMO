Create kubernates cluster using kops

kops create cluster --name=jspdemo.k8s.local --state=s3://jspdemoproject --zones=us-east-1a --node-count=1 --node-size=t3.small --master-size=t3.medium --node-volume-size=8 --master-volume-size=8

************************************

Update kops cluster 

kops update cluster --name=jspdemo.k8s.local --state=s3://jspdemoproject --yes --admin

************************************

Verify cluster 

kops validate cluster --state=s3://jspdemoproject

************************************

Delete cluster

kops delete cluster --name=jspdemo.k8s.local --state=s3://jspdemoproject --yes
