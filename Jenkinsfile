pipeline{
    agent any
    stages{
        stage('Build'){
            steps{
                sh 'g++ -o hello hello.cpp'
            }
        }
        stage('Test'){
            steps{
                sh './hello'
            }
        }
        stage('Deploy'){
            steps{
                echo "Deploying..."
            }
        }
    }
    post{
        failure{
            echo "Pipeline Failed"
        }
    }
}
