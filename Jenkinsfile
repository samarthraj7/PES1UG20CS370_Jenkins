pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh 'g++ -o pes1ug20cs370-1 pes1ug20cs370-1.cpp'
            }
        }

        stage('Test') {
            steps {
                sh './pes1ug20cs370-1'
            }
        }

        stage('Deploy') {
            steps {
                echo 'deployed successfully'
            }
        }
    }

    post {
        always {
            script {
                if (currentBuild.result == 'FAILURE') {
                    echo 'pipeline failed'
                }
            }
        }
    }
}
