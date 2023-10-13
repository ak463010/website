pipeline {
    agent any

    stages {

        stage('Git Checkout') {
            steps {
                git url: 'https://github.com/ak463010/website.git', branch: 'main'
            }
        }

      

        
        
        stage('Deploy') {
            steps {
                sh 'ls'
                // sh 'sudo rm -rf /var/www/html'
                // sh 'sudo mkdir /var/www/html'
                // sh 'sudo mv website/* /var/www/html/'
            }
        }

        stage('Cleanup') {
            steps {
                echo 'sucess'
            }
        }
    }
}