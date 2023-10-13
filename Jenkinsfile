pipeline {
    agent any

    stages {

        // stage('Git Checkout') {
        //     steps {
        //         git url: 'https://github.com/ak463010/website.git', branch: 'main'
        //     }
        // }

      

        stage('System update') {
            steps{

                sh 'sudo apt-get -y update'
            }
        }

        stage('Installing Apache2 server') {
            steps{
                sh 'sudo apt-get -y apache2'
            }
        }
        
        stage('Deploy') {
            steps {
                sh 'sudo rm -rf /var/www/html'
                sh 'sudo mkdir /var/www/html'
                sh 'sudo mv * /var/www/html/'
            }
        }

        stage('Cleanup') {
            steps {
                cleanWs()
            }
        }
    }
}