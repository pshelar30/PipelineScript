pipeline {
    agent any

    stages {
        stage('git-checkout') {
            steps {
                echo 'Checking out from git repo';
                git branch: 'main', url: 'https://github.com/pshelar30/PipelineScript.git'
            }
        }
        stage('Build') {
            steps{
                echo "Building the checked out project";
                bat 'Build.bat'
            }
        }
        stage('Delpoy'){
            steps{
                echo "Deploying the project";
                bat 'Deploy.bat'
            }
        }
    }
}
