 pipeline {
    agent {label 'Volokhov-agent '}
    stages {
        stage('Get Sources') {
            steps {
                git '<Your_Repo_SSH_URL>'
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

