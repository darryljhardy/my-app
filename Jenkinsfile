pipeline { 
    agent any 
    stages {
        stage('Clone Repo and Clean') { 
            steps { 
                bat "mvn clean"
            }
        }
        stage('Test'){
            steps {
                bat "mvn test"
            }
        }
        stage('Deploy') {
            steps {
                bat "mvn package"
            }
        }
    }
}
