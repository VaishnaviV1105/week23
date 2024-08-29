pipeline {

  agent { label 'kubepod' }

  stages {

    stage('Checkout Source') {
      steps {
        git url:'https://github.com/VaishnaviV1105/week23.git', branch:'main'
      }
    }

    stage('Deploy App') {
      steps {
        script {
          kubernetesDeploy(configs: "pod.yaml", kubeconfigId: "mykubeconfig")
        }
      }
    }

  }

}

}