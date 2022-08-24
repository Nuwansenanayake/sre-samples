
// Jenkinsfile (Declarative Pipeline)

pipeline {
    agent any

    environment{
        env_workspace_path="/home/nuwan/Documents/work/sre/Jira/patching/jenkins-workspace"        
    }

    stages {
        stage('build') {
            
            steps {
                sh """
                    cd "${env_workspace_path}"
                    pwd
                    mkdir -p out
                    unzip axp-dep-6.0.0.SNAPSHOT -d out/
                    unzip patch-axp-dep-6.0.0.SNAPSHOT-001 -d out/
                    cd out
                    cp -R patch-axp-dep-6.0.0.SNAPSHOT-001/* axp-dep-6.0.0.SNAPSHOT 
                    zip axp-dep-6.0.0.SNAPSHOT-001.zip axp-dep-6.0.0.SNAPSHOT/* 
                """
            }
        }
    }
}


