pipeline {

    agent any
    
    stages {
        stage("run frontend"){
            steps {
                echo 'executing the frontend...'
                nodejs('Node-10.17')
                sh 'yarn install'
            }
            }
        }
        
    stage("run backend"){
            steps {
                echo 'executing the backend...'
                withGradle(){
                    sh './gradlew -v'
                }
            }
        }
        
    stage("deploy"){
            steps {
                echo 'deployed the application...'
            }
        }
    }
}
