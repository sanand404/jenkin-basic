/* Requires the Docker Pipeline plugin */

pipeline {
    agent { docker { image 'maven:3.8.7-eclipse-temurin-11' } }
    stages {
        stage('build') {
            steps {
                script {
                   def version = readFile "version"
                   env.version = version
                }
                sh 'pwd'
                sh 'ls'
                sh 'echo $version'
                sh 'mvn --version'
            }
        }
    }
}