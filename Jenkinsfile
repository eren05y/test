pipeline {
    agent any

    stages {
        stage('build') {
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
