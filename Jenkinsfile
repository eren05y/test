pipeline {
    agent any

    stages {
        stage('clone') {
            steps {
                echo 'cloning'
                git branch: 'main', url: 'https://github.com/eren05y/test.git'
            }
        }
        stage('build') {
            steps {
                echo 'Building'
                sh '/usr/local/go/bin/go run main.go'
            }
        }
        stage('pack') {
            steps {
                echo 'packing'
                sh '/usr/local/go/bin/go build main.go'
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
