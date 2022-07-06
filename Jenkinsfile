pipeline {
    agent anypipeline {
    agent any

    stages {
        stage("SCM Checkout") {
            steps {
                git branch: 'master',
                    credentialsId: "raviGitAccess",            
                    url: 'https://github.com/avbravikanth1/my-react-app.git'

                dir('secondRepo') {
                    git branch: 'main',
                    credentialsId: "raviGitAccess",
                    url: 'https://github.com/avbravikanth1/dotnet_iac.git'
                }
            }
        }
    }
}