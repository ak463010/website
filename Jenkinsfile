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
                sh 'mkdir /var/www/html'
                sh 'cd /var/www/html'
                sh 'wget https://wordpress.org/latest.zip'
                
            }
        }
    }
}