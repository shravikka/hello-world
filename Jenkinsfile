pipeline {
    agent { docker { image 'node:6.3' } }
    stages {
        stage('build') {
            steps {
                sh 'echo "Hello world"'
                sh '''
                    echo "Multiline scripts"
                    ls -lah
                '''
                sh 'echo "Fail!"; exit 1'
            }
        }
    }
    post {
        always {
            echo "Build is starting"
        }
        success {
            echo "Build is successful"
        }
        failure {
            echo "Build failed"
        }
        changed {
            echo "Build state is changed"
        }
    }
}

