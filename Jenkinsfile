pipeline{
    agent any
    stages{
        stage ('Build') {
            steps {
                sh 'mvn clean package'
            }
            post {
                success {
                    echo "Archiving artifacts"
                    archiveArtifacts artifacts: '**target/*.war'
                }
            }
        }
        
    }
}