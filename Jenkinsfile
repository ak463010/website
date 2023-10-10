pipeline {
    agent any

    stages {
        stage('Updating Packages') {
            steps {
                echo 'Updating..'
                sh 'sudo apt-get -y update'
            }
        }
        stage('Installing Packages') {
            steps {
                echo 'Installing apache2..'
                sh 'sudo apt-get -y install apache2'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
                sh 'sudo rm -rf /var/www/html'
                sh 'sudo git clone https://github.com/ak463010/website.git /var/www/html'
            }
        }
    }
}