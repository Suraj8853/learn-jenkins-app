pipeline {
     agent {
        docker {
            image 'node:18'
            args '-u root:root'
        }
    }

    stages {
        stage('Build') {


            steps {
                sh '''
                    ls -la
                    node --version
                    npm --version
                    npm ci
                    npm run build
                    ls -la
                '''
            }
        }
    }
}