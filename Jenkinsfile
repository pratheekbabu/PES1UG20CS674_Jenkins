pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                    sh "g++ hello.cpp -o outputfile"
                    build job: "PES1UG20CS674-1"
                 }
        }
        stage('Test') {
            steps {
                   sh "./outputfile"
          }
        }
    }
     post {
            success {
                
                   echo 'pipeline completed'
                }
         failure{
             echo 'Pipeline failed'
         }
        }
}
