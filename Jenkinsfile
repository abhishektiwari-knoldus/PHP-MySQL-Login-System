pipeline {
    agent any

    stages {
        stage('docker build') {
            steps {
                sh 'docker rm -f $(docker container ls | awk '{print $NF}'|awk 'FNR == 2 {print}')'
                sh 'docker build . -t lamp/php1'
                sh 'docker run -p 8086:80 -d lamp/php1'
            }
        }
    }
}
