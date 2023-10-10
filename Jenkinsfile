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
                sh 'sudo mkdir /var/www/html'
                sh 'sudo wget https://wordpress.org/latest.zip'
                sh 'sudo mv latest.zip /var/www/html'


                sh 'pwd'

                sh 'sudo apt install -y unzip'

                sh 'sudo unzip latest.zip'

            
                
            }
        }
    }
}