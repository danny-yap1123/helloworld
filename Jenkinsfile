pipeline {
    agent any
    
    stages {
        stage('Sonatype Scan') {
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
