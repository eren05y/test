pipeline {
    agent any

    stages {
        stage('clone') {
            steps {
                echo 'cloning'
                git branch: 'main', url: 'https://github.com/eren05y/test.git'
                mail bcc: '', body: 'Step 1: clone phase started', cc: '', from: '', replyTo: '', subject: 'Jenkins pipeline-2', to: 'eren051999@gmail.com'
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
                mail bcc: '', body: 'step 4: last phase is started', cc: '', from: '', replyTo: '', subject: 'Jenkins pipeline-2', to: 'eren051999@gmail.com'
            }
        }
    }
}
