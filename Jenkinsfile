/* Requires the Docker Pipeline plugin */

def version = load "version"

pipeline {
    agent { docker { image 'maven:3.8.7-eclipse-temurin-11' } }
    stages {
        stage('build') {
            steps {
                sh 'mvn --version'
                sh 'echo version'
            }
        }
    }
}