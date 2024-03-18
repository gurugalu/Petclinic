pipeline {
    agent any

    tools {
        // Install the Maven version configured as "maven3" and add it to the path.
        maven "maven3"
    }

    stages {
        stage('Fetch Code') {
            steps {
                // Get some code from a GitHub repository
                git branch: 'feature1', url: 'https://github.com/jaiswaladi246/Petclinic.git'
            }
        }
        
        stage('package') {
            steps {
                sh "mvn clean package"
            }
        }
        stage('deploy to tomcat') {
            steps {
                sh "cp /home/guru/.jenkins/workspace/declartive/target/*.war /opt/apache-tomcat-9.0.65/webapps/"
            }
        }
        
    }
}

