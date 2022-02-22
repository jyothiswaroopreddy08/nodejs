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
                        bat 'bash ./jenkins/scripts/test.sh'
                    }
                }
                stage('Deliver') {
                            steps {
                                bat 'bash ./jenkins/scripts/deliver.sh'
                                input message: 'Finished using the web site? (Click "Proceed" to continue)'
                                bat 'bash ./jenkins/scripts/kill.sh'
                            }
                        }

    }
}