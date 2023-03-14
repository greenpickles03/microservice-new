pipeline {
  agent any

  stages {
    stage('Build service-registry') {
      steps {
        sh 'mvn clean package'
      }
    }

    stage('Build edge-service') {
      steps {
        sh 'mvn clean package'
      }
    }

    stage('Build config-server') {
      steps {
        sh 'mvn clean package'
      }
    }

    stage('Build department-service-core'){
        steps {
            sh 'mvn clean package'
        }
    }

    stage('Build employee-service-core'){
        steps {
            sh 'mvn clean package'
        }
    }

    stage('Run') {
      steps {
//         sh 'java -jar service-registry/target/service-registry-0.0.1-SNAPSHOT.jar'
        sh 'java -jar D:/Development file/remote/microservice/service-registry/target/service-registry-0.0.1-SNAPSHOT.jar'
        sh 'java -jar edge-service/target/edge-service-0.0.1-SNAPSHOT.jar'
        sh 'java -jar config-server/target/config-server-0.0.1-SNAPSHOT.jar'
        sh 'java -jar department-service-core/target/department-service-core-0.0.1-SNAPSHOT.jar'
        sh 'java -jar employee-service-core/target/employee-service-core-0.0.1-SNAPSHOT.jar'
        // Add more commands here as needed for each project
      }
    }
  }
}
