pipeline {
    agent any
    stages {
        stage('maven clean') {
            steps {
                sh "mvn clean"
            }
        }
        stage('maven compile'){
            steps{
                sh "mvn compile"
            }
        }
        stage('maven test-package'){
            steps{
                sh "mvn test"
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
               echo "sh cp /var/lib/jenkins/workspace/mvnproject/target/myproj.war /var/lib/tomcat9/webapps/"
            }
        }

    }
}
