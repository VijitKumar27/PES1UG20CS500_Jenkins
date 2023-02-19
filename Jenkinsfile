pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh 'g++ working.cpp -o working'
                 build job: 'PES1UG20CS498-1', wait: false
                 echo 'Build successful'
            }
        }

        stage('Test') {
            steps {
                sh 'cat working.cpp'
                echo 'Test successful'
            }
        }

        stage('Deploy') {
            steps {
               
                echo 'Deploy successful'
            }
        }
    }

    post {
        failure {
            
                echo 'Pipeline Failed'
          
        }
    }
}
