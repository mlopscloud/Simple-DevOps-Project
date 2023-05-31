=================================
KUBERNETES NETWORKING
=================================
kind: Pod
apiVersion: v1
metadata:
  name: testpod
spec:
  containers:
    - name: c00
      image: ubuntu
      command: ["/bin/bash", "-c", "while true; do echo Learning NETWORKING; sleep 5 ; done"]
    - name: c01
      image: httpd
      ports:
       - containerPort: 80
