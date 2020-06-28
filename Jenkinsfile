pipeline {

  kubernetes {
        label podlabel
        yaml """
        
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
