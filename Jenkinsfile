pipeline {
    agent {
        label 'any'
    }

    stages {
        stage('Install Dependencies') {
            steps {
                sh 'npm install'
            }
        }

        stage('Unit Test') {
            steps {
                sh 'npm run test'
            }
        }

        stage('Sonnar Scanner') {
            steps {
                sh 'npm run sonar'
            }
        }
        stage('Build Application') {
            steps {
                sh 'npm run build'
                sh 'ls -l'
            }
        }
       
        stage('Initiate Web Server') {
            steps {
                sh 'service nginx start'
            }
        }
      
        stage('Deploy Application') {
            steps {
                sh 'cp /var/www/html/'
            }
        }
    }
}
