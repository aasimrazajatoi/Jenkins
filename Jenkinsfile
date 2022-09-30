pipeline {
    agent any
    tools {nodejs "NodeJS"}
    stages {
        stage ("source") {
            steps {
                sh 'git clone https://github.com/simonplend/example-app-nodejs-backend-react-frontend.git'
            }
        }
        
        stage ("install dependencies") {
            steps {
                sh 'cd example-app-nodejs-backend-react-frontend'
                sh 'npm install'
            }
        }
        stage ("build") {
            steps {
                sh 'npm run build'
            }
        }

        stage ("test") {
            steps {
                sh 'npm start'
            }
        }

        // stage ("deploy") {

        // }
    }
}
