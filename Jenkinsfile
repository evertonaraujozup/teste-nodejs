pipeline {
  agent any
    
  tools {nodejs "node"}
    
  stages {
        
    stage('Cloning Git') {
      steps {
        git 'https://github.com/evertonaraujozup/teste-nodejs.git'
      }
    }
    stage('Test') {
      steps {
          node 'hello.js'
      }
    }      
  }
}