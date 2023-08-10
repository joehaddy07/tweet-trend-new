pipeline {
    agent {
        label 'Jenkins-Agent'
    }

environment (
    PATH = "/opt/maven/bin:$PATH"
)

    stages {
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
        // Add more stages as needed
    }
    // Post-build actions and other configurations
}
