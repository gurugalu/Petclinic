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
                git branch: 'feature2', url: 'https://github.com/jaiswaladi246/Petclinic.git'
            }
        }
        
        stage('package') {
            steps {
                sh "mvn clean package"
            }
        }
                
    }
}
