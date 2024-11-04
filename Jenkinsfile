fb7538dc51b14db3bd52eb68da7ca7f2

pipeline {
    agent any
    tools {
        maven "M3"
    }
    
    stages {
        stage("Checkout") {
            steps {
                git branch: "main", url: "https://github.com/codeyjoseph/lbg-hello-world-maven.git"
            }
        }
        stage("Compile") {
            steps {
                sh 'mvn clean compile'
            }
        }
        stage("Test") {
            steps {
                sh "mvn -Dmaven.compile.skip test"
            }
        }
        stage("Package") {
            steps {
                sh "mvn -Dmaven.compile.skip -Dmaven.compile.skip package"
            }
        }
    }
}
