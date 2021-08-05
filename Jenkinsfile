pipeline {
    agent any

    stages {
        stage('clone') {
            steps {
                echo 'cloning'
                git branch: 'main', url: 'https://github.com/eren05y/test.git'
            }
        }
            steps {
                echo 'Building'
                sh 'go run main.go'
            }
        }
        stage('pack') {
            steps {
                echo 'packing'
                sh 'go build main.go'
            }
        }
        stage('test') {
            steps {
                echo 'testing'
                sh './main'
            }
        }
    }
}
