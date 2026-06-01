pipeline {
    agent any
    stages ('start') {
            steps {
                echo "start"
            }
        }

    stage('Checkout Source') {
            steps {
                checkout scm
            }
        }

        stage('List Git Files') {
            steps {
                script {
                    echo "Listing all files and directories in workspace"

                    if (isUnix()) {
                        sh '''
                            echo "===== FILES AND FOLDERS ====="
                            find . -type f
                            echo ""
                            echo "===== DIRECTORY STRUCTURE ====="
                            find . -type d
                        '''
                    } else {
                        bat '''
                            echo ===== FILES AND FOLDERS =====
                            dir /s /b
                        '''
                    }
                }
            }
        }
}
