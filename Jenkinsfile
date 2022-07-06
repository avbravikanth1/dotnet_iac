---
pipeline {
    agent any
    stages {
        stage("SCM Checkout") {
            steps {
                git branch: 'main',
                    credentialsId: "raviGitAccess",            
                    url: 'https://github.com/avbravikanth1/dotnetApp.git'

                dir('secondRepo') {
                    git branch: 'main',
                    credentialsId: "raviGitAccess",
                    url: 'https://github.com/avbravikanth1/dotnet_iac.git'
                }
            }
        }
    }
}