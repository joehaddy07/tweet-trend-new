pipeline {
    agent (
        node (
            label 'Jenkins-Agent'
            
            )
        
        )

    stages {
        stage('Clone-code') {
            steps {
                echo git branch: 'main', url: 'https://github.com/joehaddy07/tweet-trend-new.git'
            }
        }
    }
}
