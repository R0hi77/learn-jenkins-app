pipeline {
    agent any

    stages {
        stage('Test with docker agent') {
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
    }
}