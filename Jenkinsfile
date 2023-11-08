pipeline {
    agent any
    stages {
        stage('maven build') {
            steps {
                sh "mvn clean"
                sh "mvn compile"
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
