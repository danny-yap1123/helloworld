pipeline {
    agent any
    
    stages {
        stage('Hello World') {
            steps {
                script {
                  sh 'echo hello-world && sleep 10'
                  sh "echo ${env.Test}"
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
