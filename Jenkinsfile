
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
                    cd /home/nuwan/Documents/work/sre/Jira/patching/jenkins-workspace
                    pwd
                    mkdir -p out
                    unzip axp-dep-6.0.0.SNAPSHOT -d out/
                    unzip patch-axp-dep-6.0.0.SNAPSHOT-001 -d out/
                    cp -R patch-axp-dep-6.0.0.SNAPSHOT-001 axp-dep-6.0.0.SNAPSHOT 
                """
            }
        }
    }
}


