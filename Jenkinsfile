pipeline {
    agent any
    stages {
        stage('Preparation') {
          steps {
            // Get some code from a GitHub repository
            git 'https://github.com/evertonaraujozup/teste-nodejs.git'  
          }
        }
        stage('Install Dependencies') {
            steps {
                sh('npm install')
                sh('npm run bowerInstall')
            }
        }
        stage('Test') {
            steps {
                sh('npm install')
            }
        }
    }   
        stage('Sonar') {
            steps {
               bat(sonar:sonar -Dsonar.host.url=http:\/\/172.25.137.163 -Dsonar.login=admin -Dsonar.password=admin/)
            }
         
        }
    }
}