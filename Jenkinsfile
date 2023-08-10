pipeline {
    agent (
        label 'Jenkins-Agent'
            
            
        
        )

    stages {
        stage('Clone-code') {
            steps {
                echo git branch: 'main', url: 'https://github.com/joehaddy07/tweet-trend-new.git'
            }
        }
    }
}

environment(
    PATH = "/opt/maven/bin:$PATH"
)
stage('Build') {
            steps {
                sh 'mvn clean package'
            }
        }
        
        stage('Test') {
            steps {
                sh 'mvn test'
            }
        }
