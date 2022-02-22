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
            bat 'D:\DevOps workspace\simple-node-js-react-npm-app-master\jenkins\scripts/test.sh'                    }
                }
    }
}