pipeline {
  agent { label 'kubepod' }
  
  stages {
    stage('Checkout source') {
      steps {
        git url:'https://github.com/web-riset/tes-deployment.git'
      }
    }
   }
    stage('Deploy App') {
      steps {
        kubernetesDeploy(configs: "nginx.yaml" , kubeconfigId: "mykubeconfig")
      }
    }
}
