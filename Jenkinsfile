pipeline {
    agent any
    tools {
        jdk 'JDK 21'   // must match your JDK name in Jenkins Global Tool Config
    }

    stages {
        stage('Checkout') {
            steps {
                // Pull code from your GitHub repo
                git branch: 'main', url: 'https://github.com/jay1698/maven-project.git'
            }
        }

        stage('Compile Java') {
            steps {
                script {
                    if (isUnix()) {
                        sh 'javac jay.java'
                    } else {
                        bat 'javac jay.java'
                    }
                }
            }
        }

        stage('Run Java') {
            steps {
                script {
                    if (isUnix()) {
                        sh 'java jay'
                    } else {
                        bat 'java jay'
                    }
                }
            }
        }
    }
}
