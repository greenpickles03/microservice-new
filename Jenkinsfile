pipeline {
  agent any

  stages {
    stage('Build') {
      steps {
        sh 'mvn package'
      }
    }

    stage('Build') {
      steps {
        sh 'mvn package'
      }
    }

    stage('Build') {
      steps {
        sh 'mvn package'
      }
    }

    stage('Build'){
        steps {
            sh 'mvn package'
        }
    }

    stage('Build'){
        steps {
            sh 'mvn package'
        }
    }

    stage('Run') {
      steps {
        sh 'java -jar service-registry/target/service-registry-0.0.1-SNAPSHOT.jar'
        sh 'java -jar edge-service/target/edge-service-0.0.1-SNAPSHOT.jar'
        sh 'java -jar config-server/target/config-server-0.0.1-SNAPSHOT.jar'
        sh 'java -jar department-service-core/target/department-service-core-0.0.1-SNAPSHOT.jar'
        sh 'java -jar employee-service-core/target/employee-service-core-0.0.1-SNAPSHOT.jar'
        // Add more commands here as needed for each project
      }
    }
  }
}
