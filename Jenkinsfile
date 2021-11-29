pipeline {
  agent any

  stages {
      stage('build artifact') {
            steps {
              sh "mvn clean package -DskipTests=true"  
              archive 'target/*.jar'

            }
        }   

      stage('unit test') {
            steps {
              sh "mvn test"
              archive 'target/*.jar'
            }
        } 
                  
    }
}