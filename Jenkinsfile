fb7538dc51b14db3bd52eb68da7ca7f2

pipeline {
    agent any
    tools {
        maven "M3"
    }
    
    stages {
        stage("Build") {
            steps {
                sh 'mvn clean compile'
            }
        }
        stage("Test") {
            steps {
                sh "mvn test"
            }
        }
        stage("Deploy") {
            steps {
                sh "mvn -Dmaven.compile.skip -Dmaven.compile.skip package"
            }
        }
    }
}
