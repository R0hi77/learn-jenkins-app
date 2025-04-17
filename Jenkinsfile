pipeline {
    agent any

    stages {
        stage('Test with docker agent') {
            agent {
                docker {
                    image 'node:18-alpine'
                }
            }
            steps {
                sh '''
                    npm --version
                '''
            }
        }
    }
}