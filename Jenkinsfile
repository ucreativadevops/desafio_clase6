pipeline{
    agent any
    stages{
        stage('Build infraestructure'){
            steps{
                echo 'install npm'
                sh 'npm install'
            }
        }
        stage('Unit tests'){
            steps{
                echo 'Running lint tests'
                sh 'npm run lint'
                echo 'Running unit tests'
                sh 'npm run test'
            }
        }
        stage('SonarQube setup'){
            steps{
                echo 'Running sonarqube setup'
            }
        }
        stage('Build project'){
            echo 'Compiling the Angular project'
            sh 'npm run build'
        }
        stage('Deployment'){
            steps{
                echo 'Deployment'
            }
        }
    }
}