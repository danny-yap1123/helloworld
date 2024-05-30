pipeline {
    agent any
    
    stages {
        stage('Hello World') {
            steps {
                script {
                  sh 'echo hello-world && echo dannywashere'
                  sh "echo Folder Environment Variable: ${env.TEST}"
                }
            }
        }
    }
    post {
        cleanup{
            deleteDir()
            dir("${env.WORKSPACE}@script") {
                //deleteDir()
            }
        }
    }
}
