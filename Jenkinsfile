pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh 'mvn clean package'
            }
            post {
                success {
                    echo '开始存储.33..'
                    archiveArtifacts artifacts: '**/target/*.war'
                }
            }
        }
    }
}
