pipeline {
    agent any

    stages {

        stage('Git Checkout') {
            steps {
                git url: 'https://github.com/ak463010/website.git', branch: 'main'
            }
        }

        stage('System Update and Upgrade') {
            steps {
                sh 'sudo apt-get -y update'
            }
            steps {
                sh 'sudo apt-get -y upgrade'
            }
        }

        
        
        stage('Deploy') {
            steps {
                sh 'sudo rm -rf /var/www/html'
                sh 'sudo mkdir /var/www/html'
                sh 'sudo mv website/* /var/www/html/'
            }
        }

        stage('Cleanup') {
            steps {
                echo 'sucess'
            }
        }
    }
}