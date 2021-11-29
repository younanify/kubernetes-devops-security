pipeline {
  agent any

  stages {
      stage('build artifact') {
            steps {
              sh "mv clean package -DskipTests=true"    
            }
        }   

      stage('unit test') {
            steps {
              sh "mvn test"
            }
        } 
                  
    }
}