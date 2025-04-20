pipeline {
    agent any

    stages {
        stage('Build') {
            agent {
                docker {
                    image 'node:18-slim'
                    reuseNode true
                }
            }
            steps {
                sh'''
                    npm ci
                    npm run build
                    ls -la
                '''
            }
        }
        stage('Test'){
            steps{
                sh'''
                    test -f build/index.html
                '''
            }

        }
    }
}