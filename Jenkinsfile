pipeline {
    agent any
    stages {

        stage('Echoing') {
            steps {
                sh '''
                pwd
                echo "Hi Destiny"
                echo "I am enjoying groovy"
                echo "Groovy Baby"
                echo "Inside shell block"
                '''
            }
        }

        stage('Run Script') {
            // This runs a script
            steps {
                sh 'sh ./run.sh'
            }
        }
    }
    post {
        always {
            archiveArtifacts '*.zip'
        }
    }
}