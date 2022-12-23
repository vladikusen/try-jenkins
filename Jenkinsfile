pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh 'echo "building"'
                sh 'chmod +x scripts/build.sh'
                sh 'scripts/build.sh'
                archiveArtifacts artifacts: 'bin/Debug/*', fingerprint: true
            }
        }
        stage('Test') {
            steps {
                sh 'echo "Runnning"'
                sh 'chmod +x scripts/run.sh'
                sh 'scripts/run.sh'
            }
        }
    }
}