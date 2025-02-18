pipeline {
    agent any 
    
    stages { 
        // run sonarqube test
        stage('Run Sonarqube') {
            environment {
                scannerHome = tool 'sonar';
            }
            steps {
              withSonarQubeEnv(credentialsId: 'sonarqube',  installationName: 'sonar') {
                sh "${scannerHome}/bin/sonar-scanner"
              }
            }
        }
    }
}