
// Jenkinsfile (Declarative Pipeline)

pipeline {
    agent any

    environment{
        env_workspace_path="/home/nuwan/Documents/work/sre/Jira/patching/jenkins-workspace"     
        env_pack_name="axp-dep-6.0.0.SNAPSHOT"
        env_patch_name="patch-axp-dep-6.0.0.SNAPSHOT-001"
        env_newpack_name="axp-dep-6.0.0.SNAPSHOT-001.zip"   
    }

    stages {
        stage('Merge Patch to Release Pack') {
            
            steps {
                sh """
                    cd "${env_workspace_path}"
                    
                    rm -r -f out/

                    mkdir -p out
                    unzip "${env_pack_name}" -d out/
                    unzip "${env_patch_name}" -d out/
                    cd out/
                    cp -R "${env_patch_name}"/* "${env_pack_name}" 
                    ## zip -rq "${env_newpack_name}" "${env_pack_name}"/* 
                """


            }
        }
        stage('post test'){
            steps{
                sh "pwd"
            }    
        }
    }
}


