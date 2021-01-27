pipeline {

  agent any
  stages {

    stage('Checkout Source') {
      steps {
        git url:'https://github.com/sureshemail4courses/K8sDeploy.git', branch:'main'
      }
    }

    stage('Deploy App') {
      steps {
        script {
          sh 'sudo kubectl apply -f nginx.yml'
        }
      }
    }

  }

}
