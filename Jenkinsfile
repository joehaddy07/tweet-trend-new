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
                sh 'mvn install'
                sh 'mvn -Dmaven.surefire.debug test'
            }
        }
    }
}
