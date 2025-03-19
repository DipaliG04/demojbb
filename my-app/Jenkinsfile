pipeline {
    agent any
    tools {
        maven "MAVEN"  // Match Jenkins Maven tool name
        jdk "JDK"      // Match Jenkins JDK tool name
    }
    stages {
        stage('Build') {
            steps {
                sh 'mvn -B clean package'  // Build the project
            }
        }
        stage('Test') {
            steps {
                sh 'mvn test'  // Run tests (if any)
            }
        }
        stage('Deploy') {
            steps {
                // Example: Deploy to Tomcat
                sh 'cp target/*.war /opt/tomcat/webapps/'
            }
        }
    }
}
