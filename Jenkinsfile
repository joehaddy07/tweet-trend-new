pipeline {
    agent {
        label 'Jenkins-Agent'
    }

environment {
    PATH = "/opt/maven/bin:$PATH"
}

    stages {
        stage('Build'){
            steps {
                sh 'mvn clean deploy'
                
            }
        }
    }
}

stage('SonarQube analysis') {
    environment {
      scannerHome = tool 'joe-sonar-scannar'
    }
    steps{
    withSonarQubeEnv('joe-sonarqube-server') { // If you have configured more than one global server connection, you can specify its name
      sh "${scannerHome}/bin/sonar-scanner"
    }
    }
  }
