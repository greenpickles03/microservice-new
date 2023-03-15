pipeline {
  agent any

  stages {
    stage('Build service-registry') {
      steps {
       dir("${WORKSPACE}\\service-registry"){
        bat 'mvn clean install -Dmaven.test.skip=true'
       }
      }
    }

    stage('Build edge-service') {
      steps {
        dir("${WORKSPACE}\\edge-service"){
            bat 'mvn clean install -Dmaven.test.skip=true'
        }
      }
    }

    stage('Build config-server') {
      steps {
        dir("${WORKSPACE}\\config-server"){
            bat 'mvn clean install -Dmaven.test.skip=true'
        }
      }
    }

    stage('Build department-service-core'){
        steps {
           dir("${WORKSPACE}\\department-service-core"){
               bat 'mvn clean install -Dmaven.test.skip=true'
           }
        }
    }

    stage('Build employee-service-core'){
        steps {
           dir("${WORKSPACE}\\employee-service-core"){
              bat 'mvn clean install -Dmaven.test.skip=true'
          }
        }
    }

    stage('Run') {
      steps {
        bat 'java -jar service-registry\\target\\service-registry-0.0.1-SNAPSHOT.jar'
        bat 'java -jar edge-service\\target\\edge-service-0.0.1-SNAPSHOT.jar'
        bat 'java -jar config-server\\target\\config-server-0.0.1-SNAPSHOT.jar'
        bat 'java -jar department-service-core\\target\\department-service-core-0.0.1-SNAPSHOT.jar'
        bat 'java -jar employee-service-core\\target\\employee-service-core-0.0.1-SNAPSHOT.jar'
        // Add more commands here as needed for each project
      }
    }
  }
}