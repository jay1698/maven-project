pipeline {
    agent any
    tools {
        jdk 'JDK 11'  // Name of the JDK installation in Jenkins
    }

    stages {
        stage('Check JDK Version') {
            steps {
                script {
                    // Checking the JDK version
                    def javaVersion = sh(script: 'java -version', returnStdout: true).trim()
                    echo "JDK Version: ${javaVersion}"
                }
            }
        }
    }
}
