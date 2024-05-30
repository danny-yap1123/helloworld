pipeline {
    agent any
    
    stages {
        stage('Hello World') {
            steps {
                script {
                  sh 'echo hello-world && echo dannywashere'
                  sh "echo Folder Environment Variable: ${env.JOB_NAME}"
                  def jobPath = env.JOB_NAME.split('/')
                  def folderName = jobPath[0]
                  sh "echo ${folderName}"
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
