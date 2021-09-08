pipeline {
    agent any

    stages {
        stage('verify branch') {
            steps {
                echo '$GIT_BRANCH'
            }
        }
      stage('Docker build') {
            steps {
               sh 'docker images -a'
               sh '''
               cd azure-vote/
               docker images -a
               docker build -t jenkins-pipeline .
               cd ..
                ''' 
            }
        }  
    }
}
