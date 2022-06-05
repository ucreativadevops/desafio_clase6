pipeline{
    agent any
    tools{
        nodejs 'nodejs17'
    }
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
            steps{
            echo 'Compiling the Angular project'
            sh 'npm run build'
            echo "reviewing that the directory exists"
            sh 'ls -a'
            }
        }
        stage('Deployment'){
            steps{
                echo 'Deployment'
            }
        }
    }
}

