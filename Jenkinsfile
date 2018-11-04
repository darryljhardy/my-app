pipeline { 
    agent any 
    stages {
        stage('Clone Repo and Clean') { 
            steps { 
                bat "rmdir my-app /s /q"
                bat "git clone https://github.com/darryljhardy/my-app.git"
                bat "mvn clean -f my-app"
            }
        }
        stage('Test'){
            steps {
                bat "mvn test -f my-app"
            }
        }
        stage('Deploy') {
            steps {
                bat "mvn package -f my-app"
            }
        }
    }
}
