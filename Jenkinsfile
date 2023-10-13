pipeline {
    agent any

    stages {

        stage('System update') {
            steps{

                sh 'sudo apt-get -y update'
            }
        }

        stage('Installing Apache2 server') {
            steps{
                sh 'sudo apt-get install -y apache2'
            }
        }

        stage('Git wordpress') {
            steps {
                sh 'wget https://wordpress.org/latest.zip'
            }
        }

        stage('Unzip wordpress') {
            steps {
                sh 'wget https://wordpress.org/latest.zip'
            }
        }

        stage('Mv latest/* into /var/www/html/') {
            steps {
                sh 'sudo mv wordpress/* /var/www/html/'
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