pipeline {

  kubernetes {
        label podlabel
        yaml """
kind: Deployment
metadata:
  labels:
    app: web
  name: mynginx
spec:
  replicas: 1
  selector:
    matchLabels:
      app: web
  template:
    metadata:
      labels:
        app: web
    spec:
      containers:
      - image: nginx
        name: mynginx


---
apiVersion: v1
kind: Service
metadata:
  labels:
    app: web
  name: mynginx
spec:
  ports:
  - nodePort: 32223
    port: 80
    protocol: TCP
    targetPort: 80
  selector:
    app: web
  type: NodePort        
"""        

  stages {

    stage('Checkout Source') {
      steps {
        git url:'https://github.com/itdanya/skb-project.git', branch:'task-123'
      }
    }

    stage('Deploy App') {
      steps {
         echo 'done!'
    }
    }
  }
  }
}
