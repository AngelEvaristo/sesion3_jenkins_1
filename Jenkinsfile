pipeline {
    agent any

    environment {
        DN_VERSION= "9.0"
    }

    stages {
        // stage ('Clonar desde github') {
        //     steps {
        //         checkout scmGit(branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[credentialsId: 'AngelEvaristo', url: 'https://github.com/AngelEvaristo/sesion3_jenkins_1.git']])
        //     }
        // }

        stage ('Restaurar dependencias') {
            steps {
                script {
                    bat 'dotnet restore'
                }
            }
        }

        stage ('Compilacion') {
            steps {
                script {
                    bat 'dotnet build --configuration Release'
                }
            }
        }

    }

}