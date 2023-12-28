pipieline{
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

        // Stagge 3 Deploying
        stage ('Deply'){
            steps {
                echo 'deploying ....'
            }
        }
     }

}