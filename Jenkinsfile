/* Requires the Docker Pipeline plugin */

env.WORKSPACE = pwd()
def version = readFile "${env.WORKSPACE}/version"

pipeline {
    agent { docker { image 'maven:3.8.7-eclipse-temurin-11' } }
    stages {
        stage('build') {
            steps {
                sh 'mvn --version'
                sh 'echo $version'
            }
        }
    }
}