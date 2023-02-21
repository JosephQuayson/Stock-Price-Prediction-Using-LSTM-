pipelineJob('example') {
    description('This is dsl examples')

    triggers {
        cron('* * * * *')
    }
    logRotator {
        numToKeep(5)
        artifactNumToKeep(1)
    }
     definition {
        cpsScm {
            scm {
                git {
                    remote {
                    url ('https://github.com/JosephQuayson/Stock-Price-Prediction-Using-LSTM-.git')
                  }
                  branch('main')
               }
            }
            scriptPath("Jenkinsfile")
        }
    }
}
