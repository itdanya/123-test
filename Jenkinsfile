pipeline {

  agent any

  stages {

    stage('Checkout Source') {
      steps {
        git url:'https://github.com/itdanya/skb-project.git', branch:'task-123'
      }
    }

    stage('Deploy App') {
      steps {
        script {
          sh '/usr/bin/kubectl apply -f prob-nginx.yaml'
    }
    }
  }
  }
}
