  pipeline {
    agent any
    tools {
        jdk 'JDK 21'   // must match your JDK name in Jenkins Global Tool Config
    }

    stages {
        stage('Checkout') {
    steps {
        git branch: 'master', url: 'https://github.com/jay1698/maven-project.git', credentialsId: 'GitID'
    }
        }

        stage('Compile Java') {
            steps {
                script {
                    if (isUnix()) {
                        sh 'javac jay.java'
                    } else {
                        bat 'javac src\\main\\java\\gg\\jay.java'
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
                        bat 'java -cp out gg.jay'
                    }
                }
            }
        }
    }
}
