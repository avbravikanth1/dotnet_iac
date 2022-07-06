pipeline {
    agent any
    stages {
        stage("SCM Checkout") {
            steps {
                git branch: 'master',
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
                sh "dotnet clean /var/lib/jenkins/workspace/ravi/dotnetApp/SampleWebApplication"                
                sh "dotnet build /var/lib/jenkins/workspace/ravi/dotnetApp/SampleWebApplication"               
            }
        }
    }
}