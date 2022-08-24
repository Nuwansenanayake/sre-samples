
// Jenkinsfile (Declarative Pipeline)

pipeline {
    agent any
    stages {
        stage('build') {
            
            steps {
                sh 'mvn --version'
                sh 'ls'
                sh 'cd /home/nuwan/Documents/work/sre/Jira/patching' 
                sh 'mkdir -p /home/nuwan/Documents/work/sre/Jira/patching/jenkins/test'
                sh """
                    cd /home/nuwan/Documents/work/sre/Jira/patching
                    mkdir -p jenkins/test2
                """
                sh """
                    cd ../../jenkins-workspace
                    ls
                    mkdir -p out
                """
            }
        }
    }
}


