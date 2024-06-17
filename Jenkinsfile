pipeline {
     agent any
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
                  npm install -g serve
               serve -s build -l 4000 &
                '''
            }
        }
    }
}