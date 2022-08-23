pipeline {
    agent { dockerfile true }
    stages {
        stage('Get source') {
            steps {
                git(
                    url:'https://github.com/Faaline/BeopenIT_Test_Devops.git'               
                )

                bat "git log"
            }
        }
      
      stage('Front-end') {
            agent {
                docker { image 'node:16.13.1-alpine' }
            }
            steps {
                sh 'node --version'
            }
        }
    }
  
}
