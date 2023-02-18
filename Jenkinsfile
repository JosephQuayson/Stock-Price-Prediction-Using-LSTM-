pipeline{
    agent{ docker 'maven:3.9.0-amazoncorretto-8' } 
    stages{
        stage('Example Build') {
            steps{
                sh 'mvn --version'
            }
        }
    }
}
