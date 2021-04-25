 pipeline {
    agent {label 'Volokhov-agent'}
    stages {
        stage('Get Sources') {
            steps {
                sh 'npm install'
            }
        }
        stage('Restore Dependencies') {
            steps {
                sh 'npm install'
            }
        }
        stage('Test') { 
            steps {
                sh 'npm run test' 
            }
        }
        stage('Package') { 
            steps {
                sh 'npm run build' 
            }
        }
        stage('Archive Artifacts') { 
            steps {
                archiveArtifacts '*.zip'
            }
        }
    }
}

