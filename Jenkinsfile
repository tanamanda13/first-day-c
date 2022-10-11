pipeline {
    agent any

    stages {
        stage('compile') {
            steps {
                sh 'apt update && apt install gcc -y'
                sh 'apt install make -y'
                sh 'make -f Makefile'
            }
        }
        stage('archive') {
            steps {
                archiveArtifacts "HelloWorld"
                // script {
                //     if (fileExists('HelloWorld')) {
                //         archiveArtifacts "${WORKSPACE}"
                //     }
                // }
            }
        }
    }
}
