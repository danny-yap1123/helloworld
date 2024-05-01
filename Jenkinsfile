pipeline {
    agent any
    
    stages {
        stage('Hello World') {
            steps {
                script {
                  sh 'echo hello-world && sleep 10'
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
