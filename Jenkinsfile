pipeline {
    agent any 
    
    stages { 
        // run sonarqube test
        stage('Run Sonarqube') {
            environment {
                scannerHome = tool 'sonar';
            }
            steps {
              withSonarQubeEnv(credentialsId: 'sonarqube') {
                sh "${scannerHome}/bin/sonar-scanner"
              }
            }
        }
    }
}