pipeline {
    agent any
    
    tools {nodejs "NODE_JS"}
    
    stages {
        stage('Build') {
            steps {
                bat 'npm install'
            }
        }
        stage('Test') {
            steps {
               sh './jenkins/scripts/test.sh'                    }
                }
    }
}