pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                 sh 'g++ temp.cpp -o temp'
                 build job: 'PES1UG20CS074-1', wait: false
                 echo 'Build by CS074 successful'
            }
        }

        stage('Test') {
            steps {
               sh 'cat error.cpp'
                echo 'Test by CS074 successful'
            }
        }

        stage('Deploy') {
            steps {
               
                echo 'Deploy by CS074 successful'
            }
        }
    }

    post {
        failure {
            
                echo 'Pipeline Failed'
          
        }
    }
}
