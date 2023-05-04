pipeline {
    agent any

    stages {
        stage('docker build') {
            steps {
                sh 'docker build . -t lamp/php1'
                sh 'docker run -p 8086:80 -d lamp/php1'
            }
            
        }
        stage('docker push'){
            steps{
                script{
                    withCredentials([string(credentialsId: 'dochub-pwd', variable: 'dockerhubpwd')]) {
                    sh 'docker login -u abhishek00007 -p ${dockerhubpwd}'
}

                }
            }
        }
    }
}
