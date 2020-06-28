pipeline {


  agent { label 'kubepod' }


  stages {


    stage('Checkout Source') {
      steps {
        git url:'https://github.com/itdanya/skb-project.git', branch:'task-123'
      }
    }


    stage('Deploy App') {
      steps {
        script {
          kubernetesDeploy(configs: "nginx.yaml", kubeconfigId: "476119d3-e9b0-458f-a331-bedc428d8503")
        }
      }
    }


  }


}
