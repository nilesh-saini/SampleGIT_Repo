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
                    echo "===== FILES AND FOLDERS ====="
                    ls -lrt
                '''
            }
        }

        stage('Create ZIP Archive') {
            steps {
                script {
                    sh '''
                        tar -czf src.zip src
                        ls -lrt
                        ls -lrt src.zip
                    '''
                }
            }
        }

        stage('deploy') {
            steps {
              echo " deploy step"
                }
            }

    }
}
