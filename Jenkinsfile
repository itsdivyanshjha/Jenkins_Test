pipeline {
    agent any
    stages {
        stage('Prepare') {
            steps {
                echo 'Preparing environment'
                // Install dependencies if necessary
                sh 'pip install -r requirements.txt'
            }
        }
        stage('Execute Scripts') {
            parallel {
                stage('Script 1') {
                    steps {
                        echo 'Running script1.py'
                        sh 'python script1.py'
                    }
                }
                stage('Script 2') {
                    steps {
                        echo 'Running script2.py'
                        sh 'python script2.py'
                    }
                }
            }
        }
    }
}
