pipeline {
    agent any

    stages {
        stage('docker build') {
            steps {
                sh 'docker build . -t lamp/php1'
                sh 'docker run -p 8086:80 -d lamp/php1'
            }
        }
    }
}
