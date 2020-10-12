pipeline {
    agent any
    tools{
        maven 'local maven'
    }

    stages {
        stage('Build') {
            steps {
                sh 'mvn clean package'
            }
            post {
                success {
                    echo '开始存储.....'
                    archiveArtifacts artifacts: '**/target/*.war'
                }
            }
        }
    }
}
