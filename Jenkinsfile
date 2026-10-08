pipeline {
    agent any

    stages {
        stage('Hello') {
            steps {
                echo 'Hello World - Webhook test1'
            }
        }
    }

    post {
        success {
            mail to: 'YOUR_EMAIL@gmail.com',
                 subject: "Jenkins Build Successful",
                 body: "The Jenkins build was successful."
        }

        failure {
            mail to: 'bhargav.marouthu@gmail.com',
                 subject: "Jenkins Build Failed",
                 body: "The Jenkins build has failed."
        }
    }
}
