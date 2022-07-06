pipeline {
    agent any
    stages {
        stage("SCM Checkout") {
            steps {
                git branch: 'main',
                    credentialsId: "raviGitAccess",            
                    url: 'https://github.com/avbravikanth1/dotnet-sample.git'

                dir('secondRepo') {
                    git branch: 'main',
                    credentialsId: "raviGitAccess",
                    url: 'https://github.com/avbravikanth1/dotnet_iac.git'
                }
            }            
        }
        stage('Build') {
            steps {
                sh "cd SampleWebApplication"
                sh "dotnet clean"                
                sh "dotnet build"               
            }
        }
    }
}