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
            }
        }
    }
}

