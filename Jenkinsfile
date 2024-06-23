pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git url: 'https://github.com/yourusername/simple-html-project.git', branch: 'master'
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
