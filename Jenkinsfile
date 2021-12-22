pipeline {
    agent any

    stages {
        stage('Compile') {
            steps {
                echo 'test pipeline'
                git branch: '${branch}', url: 'https://github.com/pawlakadrian/Jenkins.git'
                bat 'mvn clean compile'
                echo 'wszystko ok'
            }
        }
        stage('Test') {
            steps {
                bat 'mvn clean test'
                echo 'tests completed!'
            }
        }
    }
}
