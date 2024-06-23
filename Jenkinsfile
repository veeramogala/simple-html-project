pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git credentialsId: 'github-pat', url: 'https://github.com/veeramogala/simple-html-project.git', branch: 'main'
            }
        }
        stage('Build') {
            steps {
                echo 'Building...'
            }
        }
        stage('Deploy') {
            steps {
                // Assuming the web server serves files from /var/www/html
                sh 'cp -r * /var/www/html/'
            }
        }
    }
}
