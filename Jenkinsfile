pipeline {

  agent { label 'deploy' }
  stages {

    stage('Checkout Source') {
      steps {
        git url:'https://github.com/sureshemail4courses/K8sDeploy.git', branch:'main'
      }
    }

    stage('Deploy App') {
      steps {
        script {
          kubernetesDeploy(configs: "nginx.yml", kubeconfigId: "mykubeconfig")
        }
      }
    }

  }

}
