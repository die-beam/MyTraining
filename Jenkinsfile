pipeline{
     //Directives
     agent any
     tools {
        maven 'maven'
     }

     stages {
        // Specify various stage with in stages

        // stage 1. Build
        stage ('Build'){
            steps {
                sh 'mvn clean install package'
            }
        }

        // stage 2. Testing
        stage ('Test'){
            steps {
                echo 'testing....'
            }
        }

        // Stage 3 publish artifact to Nexus
        stage ('Publish to Nexus')
            steps {
                nexusArtifactUploader artifacts: [[artifactId: 'VinayDevOpsLab', classifier: '', file: 'target/VinayDevOpsLab/0.0.10-SNAPSHOT.war', type: 'war']], credentialsId: '49035938-b85c-4702-bf61-7fd3ea0e8d24', groupId: 'com.vinaysdevopslab', nexusUrl: '172.20.10.252:8081', nexusVersion: 'nexus3', protocol: 'http', repository: 'MyLab-Snapshot', version: '0.0.11-SNAPSHOT'
            }

        // Stagge 3 Deploying
        stage ('Deply'){
            steps {
                echo 'deploying ....'
            }
        }
     }

}