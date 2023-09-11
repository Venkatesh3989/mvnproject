pipeline {
    agent any
    stages {
        stage('---clean---') {
            steps {
                sh "mvn clean"
            }
        }
        stage('--compile--') {
            steps {
                sh "mvn compile"
            }
        }
        stage('--test--') {
            steps {
                sh "mvn test"
            }
        }
        stage('--package--') {
            steps {
                sh "mvn package"
            }
        }
        stage('--install--') {
            steps {
                sh "mvn install"
            }
        }
        stage('deploy') {
            steps {
                sh "cp /var/lib/jenkins/workspace/mvnproject/target/myproj.war /var/lib/tomcat9/webapps/"
            }
        }

    }
}
