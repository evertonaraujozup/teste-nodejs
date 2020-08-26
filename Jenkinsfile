pipeline {
    agent any
    tools {nodejs "nodeenv"}
    stages {
        stage("Code Checkout from Jenkins") {
            steps {
                git branch: 'master',
                credentialsId: url:'https://github.com/evertonaraujozup/teste-nodejs.git'
            }
            stage ('Code Quality Check via SonarQube') {
                steps {
                    def scannerHome = tool 'sonarqube';
                    sh "${tool(sonarqube")/bin/sonar-scanner \
                    -Dsonar.projectKey=devops \
                    -Dsonar.projectKey=devops \
                    -Dsonar.sources=. \
                    -Dsonar.host.url=http:// \
                    -Dsonar.login=
                }
            }
        }
    }
    stage("Install Project Dependencies"){
        steps {
            nodejs(nodeJSInstallationName: 'nodenv') {
                sh "npm install"
            }
        }
    }
}