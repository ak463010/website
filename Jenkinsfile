pipeline {
    agent any

    stages {


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