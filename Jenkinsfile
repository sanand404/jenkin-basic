/* Requires the Docker Pipeline plugin */

pipeline {
    agent { docker { image 'maven:3.8.7-eclipse-temurin-11' } }
    stages {
        stage('build') {
            steps {
                script {
                    version = readFile "version"
                }
                sh 'mvn --version'
                sh 'echo version'
            }
        }
    }
}