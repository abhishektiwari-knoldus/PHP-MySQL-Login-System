pipeline {
    agent any

    stages {
        stage('docker build') {
            steps {
                sh 'docker build . -t abhishek00007/lampp:${BUILD_NUMBER}'
                //sh 'docker run -p 8086:80 -d lamp/php1'
            }
            
        }
        stage('docker login'){
            steps{
                script{
                    withCredentials([string(credentialsId: 'dochub-pwd', variable: 'dockerhubpwd')]) {
                    sh 'docker login -u abhishek00007 -p ${dockerhubpwd}'
                    //sh 'docker tag lamp/php1 abhishek00007/lampp:${BUILD_NUMBER}'
                   // sh 'docker push abhishek00007/lampp:${BUILD_NUMBER}'
  
}

                }
            }
        }
        stage('docker image push')
        {
            steps
            {
                 sh 'docker push abhishek00007/lampp:${BUILD_NUMBER}'
            }
        }
    }
}
