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

        stage('Installing unzip') {
            steps{
                sh 'sudo apt-get install -y unzip'
            }
        }

        stage('Installing php') {
            steps{
                sh 'sudo apt-get install -y php7.4'
            }
        }

        stage('Installing php extentions') {
            steps{
                sh 'sudo apt-get install -y php7.4 php7.4-common php7.4-opcache php7.4-mcrypt php7.4-cli php7.4-gd php7.4-curl php7.4-mysql'
            }
        }

        stage('Installing mysql server') {
            steps{
                sh 'sudo apt-get install -y mysql-server'
            }
        }

        stage('Download wordpress') {
            steps {
                sh 'wget https://wordpress.org/latest.zip'
            }
        }

        stage('Unzip wordpress') {
            steps {
                sh 'unzip latest.zip'
            }
        }

        stage('Deploy') {
            steps {
                sh 'sudo rm -rf /var/www/html'
                sh 'sudo mkdir /var/www/html'
                sh 'sudo mv wordpress/* /var/www/html/'
            }
        }

    

        stage('Cleanup') {
            steps {
                cleanWs()
            }
        }
    }
}