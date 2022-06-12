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
                echo 'Ejecutando: npm run test'
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

      
        stage('Deploy Application') {
            steps {
                sh 'cp dist/clase6/* /var/www/html/'
            }
        }
    }
}
