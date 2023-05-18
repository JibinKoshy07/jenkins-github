pipeline {
    agent any
    stages {

        stage('Checkout Codebase') {
            steps {
            checkout scm: [$class: 'GitSCM',
            userRemoteConfigs: [[credentialsId: 'Github_sshkey0',url: 'git@github.com:JibinKoshy07/jenkins-github.git', refspec: '+refs/heads/*:refs/remotes/origin/*']]

            }
        }
        stage('Build') {
            steps {
                sh 'pip install flask'

            }
        }
        // stage('Test') {
        //     steps {
        //         sh './a.out'
        //     }
        // }
        stage('Deploy') {
            steps {
                sh 'echo Done!'
            }
        }
    }
}