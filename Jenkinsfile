pipeline {
    agent any 
    
    tools {nodejs "node"}

    stages  {
        stage('Cloning Git'){
            steps {
                git 'https://github.com/evertonaraujozup/teste-nodejs'
          }
          
          stage ('Test') {
              steps {
                  sh 'node hello.js'
          }
        }
    }
}