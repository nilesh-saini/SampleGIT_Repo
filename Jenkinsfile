pipeline {
    agent any
    environment {
        EMAIL_RECIPIENTS = 'nilesh.saini@gmail.com'
        ZIP_NAME = "SOURCE_${BUILD_NUMBER}.zip"
    }

    stages {

        
        stage('Build') {
            steps {
              echo " build step"
                }
            }

        stage('Checkout Source') {
            steps {
                checkout scm
            }
        }

        
        stage('test') {
            steps {
              echo " test step"
                }
            }
        
        stage('List Git Files') {
            steps{
                echo "Listing all files and directories in workspace"
                sh '''
                    ls -lrt
                '''
            }
        }

        stage('deploy') {
            steps {
              echo " deploy step"
                }
            }

    }
}
