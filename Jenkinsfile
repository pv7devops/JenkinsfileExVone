pipeline {
    agent any
    stages{
        stage('Build'){
            steps {
                sh 'mvn clean package'
            }
            post {
                success {
                    echo 'Archive artifiacts and get the output in Jar, war or EAR'
                    archiveArtifacts artifacts: '**/target/*.war'
                }
            }
        }
    }
}
