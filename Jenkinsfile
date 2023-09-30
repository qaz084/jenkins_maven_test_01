/*Jenkinsfile (Declarative Pipeline)*/
/* Requires the Docker Pipeline plugin */
pipeline {
    agent { docker { image 'maven:3.9.4-eclipse-temurin-17-alpine' } }
    stages {
        stage('build') {
            steps {
                bat 'mvn --version'
            }
        }
         post {
        always {
                timeout(time: 1, unit: 'MINUTES') {
                    echo 'This will always run'
                }
          
        }
    }
}
