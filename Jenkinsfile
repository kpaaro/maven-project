pipeline {
    agent any
    stages{
        stage('Build'){
            steps {
                bat 'echo %PATH%'
                bat 'mvn clean package'
            }
            post {
                success {
                    echo 'Now Archiving...'
                    archiveArtifacts artifacts: '**/target/*.war'
                }
            }
        }
    }
}