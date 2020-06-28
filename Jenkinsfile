pipeline {


  agent { label 'kubepod' }


  stages {


    stage('Checkout Source') {
      steps {
        git url:'https://github.com/itdanya/skb-project.git', branch:'task-123'
      }
    }


    stage('Deploy App') {
      sh script: nginx.yaml
    }

  }


}
