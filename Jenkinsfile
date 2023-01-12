/* Requires the Docker Pipeline plugin */

pipeline {
    agent { docker { name: 'asible', image 'maven:3.8.7-eclipse-temurin-11' } }
    stages {
        stage('build') {
            container('ansible') {
                script {
                   def version = readFile(file: "version")
                   echo version
                }
                sh 'mvn --version'
            }
        }
    }
}