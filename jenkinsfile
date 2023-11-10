pipeline {
    agent any

    stages {
   //     stage('Checkout') {
     //       steps {
                // Checkout source code from your version control system (e.g., Git)
     //           checkout scm
        //    }
        }

        stage('Build') {
            steps {
                // Build the Maven project
                script {
                    sh "${MAVEN_HOME}/bin/mvn clean package"
                }
            }
        }

        stage('Test') {
            steps {
                // Run tests (modify as per your testing framework)
                script {
                    sh "${MAVEN_HOME}/bin/mvn test"
                }
            }
        }

        stage('Deploy') {
            steps {
                // Deploy your application (modify as per your deployment process)
                script {
                    // Example: Deploy to a Tomcat server
                    sh "cp target/your-app.war /path/to/tomcat/webapps/"
                }
            }
        }
    }

    post {
        success {
            // Notify on success if needed
            echo "Build and deployment successful!"
        }
        failure {
            // Notify on failure if needed
            echo "Build or deployment failed!"
        }
    }
}
