pipeline{
    agent any 
    environment{
        script_options = "--clean 30" 
        Docker_pass = credentials('docker-password')
    }
    stages{
        stage('clone'){
            agent{
                docker{
                    image 'maven'
                }
            }

            environment{
                        script_options = "--clean 30"
            }   
            steps{
                sh 'mvn --version'
                sh 'echo $script_options'
            }
            
        }
        stage('build'){
            agent {
                docker {
                    image 'node'
                }
            }
            steps{
                sh 'node --version'
                sh 'printenv'
            }
        }
        stage('docker login'){
            steps{
                sh "docker login -u josephquay -p $Docker_pass "
                }
        }
    }

    post{
        always{
            cleanWs()
        }
        success{
            sh "echo Success"
        }
    }

}
