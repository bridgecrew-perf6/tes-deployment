pipeline {
  agent { label 'kubepod' }
  
  stages {
    stage('Checkout source') {
      steps {
        git url:'https://github.com/web-riset/tes-deployment.git', branch:'main'
      }
   }
    stage('Deploy App') {
      steps {
        script{
          kubernetesDeploy(configs: "nginx.yaml" , kubeconfigId: "mykubeconfig")
        }       
      }
    }
  }
}
