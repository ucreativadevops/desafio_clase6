pipeline{
    agent{ 'aws' }
    tools{
        nodejs 'nodejs14'
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

ssh-rsa AAAAB3NzaC1yc2EAAAADAQABAAABAQC1RqMtF54/IPQzgil76TvsyaAGX5eSI6GqLYQQvPoWEdbpxEJM9SJ+In2B/NiYuag4TiYwFiQcRfZaLWgmXlZkaPlU3FDSnD39kf4VWl7YgpZMUXm/iXCCqm+y1Zf67kjKhsLTWhmLuhq92Nehl/p6V75K+XzbFqEtxc+ZzBC1bCvVNg2EkLiOhrivPA1j4aWFIitZypWlziKPPeaHXjjQGiOmxRsTxGqWuluj9VNIN5i1IHIoZ9xliedIEzXxgj5gqt5Of/jHns5Ao3SHaOBYLOao95fq3hMmSqmhkwZOezLneT1ay78Dw0czpEN9K7LhQWuHLSufT2C2hEjFgPiz ec2-user@ip-172-31-25-229.ec2.internal
