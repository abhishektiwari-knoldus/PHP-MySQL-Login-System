pipeline {
    agent any

    stages {
        stage('docker build') {
<<<<<<< HEAD
            steps {             
=======
            steps {
>>>>>>> 5244a1ebf1283417767119d61664cdb13cf7af7f
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
