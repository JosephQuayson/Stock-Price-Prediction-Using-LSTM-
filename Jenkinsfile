pipeline {
    agent { docker 'maven:3.9.0-eclipse-temurin-11' } 
    stages {
        stage('Example Build') {
            steps {
                sh 'mvn -B clean verify'
            }
        }
    }
}
