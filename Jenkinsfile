pipeline {
  agent any

  stages {
      stage('git version') {
            steps {
              sh "git version"    
            }
        }   

      stage('maven version') {
            steps {
              sh "mvn -v"
            }
        } 
      stage('docker version') {
            steps {
              sh "docker --version"
            }
        }    


      stage('kube version') {
            steps {
              withKubeConfig([credentialsId: 'kubeconfig']) {
              sh "kubectl version --short"
              }
            }
        }                    
    }
}