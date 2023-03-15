pipeline {
  agent any

  stages {
    stage('Build service-registry') {
      steps {
        bat 'cd service-registry && mvn clean package'
      }
    }

    stage('Build edge-service') {
      steps {
        bat 'cd edge-service && mvn clean package'
      }
    }

    stage('Build config-server') {
      steps {
        bat 'cd config-server && mvn clean package'
      }
    }

    stage('Build department-service-core'){
        steps {
            bat 'cd department-service-core && mvn clean package'
        }
    }

    stage('Build employee-service-core'){
        steps {
            bat 'cd employee-service-core && mvn clean package'
        }
    }

    stage('Run') {
      steps {
        bat 'java -jar service-registry/target/service-registry-0.0.1-SNAPSHOT.jar'
        bat 'java -jar edge-service/target/edge-service-0.0.1-SNAPSHOT.jar'
        bat 'java -jar config-server/target/config-server-0.0.1-SNAPSHOT.jar'
        bat 'java -jar department-service-core/target/department-service-core-0.0.1-SNAPSHOT.jar'
        bat 'java -jar employee-service-core/target/employee-service-core-0.0.1-SNAPSHOT.jar'
        // Add more commands here as needed for each project
      }
    }
  }
}