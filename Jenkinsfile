pipeline {
     
 tools {
        nodejs "Nodejs" // Ensure NodeJS is configured in Global Tool Configuration
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