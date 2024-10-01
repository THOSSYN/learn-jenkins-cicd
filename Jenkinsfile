pipeline {
    agent any

    stages {
        stage('w/ Docker') {
            agent {
                docker {
                    image 'node: 18-alpine'
                }
            }
            steps {
                sh '''
                  ls -la
                  node --version
                  npm ci
                  npm run build
                  ls -la
                '''
            }
        }
    }
}