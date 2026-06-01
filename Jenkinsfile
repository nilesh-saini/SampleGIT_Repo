pipeline {
    agent any
    environment {
        EMAIL_RECIPIENTS = 'nilesh.saini@gmail.com'
        ZIP_NAME = "SOURCE_${BUILD_NUMBER}.zip"
    }

    stages {

        stage('Build Start Notification') {
            steps {
                script {
                    emailext(
                        subject: "Jenkins Build Started: ${env.JOB_NAME} #${env.BUILD_NUMBER}",
                        body: """
                            Build has started.

                            Job Name: ${env.JOB_NAME}
                            Build Number: ${env.BUILD_NUMBER}
                            Build URL: ${env.BUILD_URL}

                            Triggered by: ${currentBuild.getBuildCauses()}
                        """,
                        to: "${EMAIL_RECIPIENTS}"
                    )
                }
            }
        }
        stage('Build') {
            steps {
              echo " build step"
                }
            }
              stage('test') {
            steps {
              echo " test step"
                }
            }

              stage('deploy') {
            steps {
              echo " deploy step"
                }
            }

    }
}
