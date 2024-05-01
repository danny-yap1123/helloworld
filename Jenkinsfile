pipeline {
    agent any
    
    stages {
        stage('Sonatype Scan') {
            steps {
                script {
                  sh './nexus-iq-cli -a "${user}:${pass}" -i Java-Sample1 -s "https://nexusiq.nssg.jhdomain.com/" -t "build" . '
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
