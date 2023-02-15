pipeline{
    agent any
    stages {
        stage('Build'){

            steps{
                sh 'g++ -o fresh fresh.cpp'
                echo 'Build stage successful'
            }
        }
        stage('Test'){
            steps{
                sh './fresh'
                echo 'Test stage successful'
            }
        }
        // stage('Deploy'){
        //     steps{
        //         sh 'mvn deploy'
        //         echo 'Deployment successful'
        //     }
        // }
    }
    post{
        failure{
            echo 'Pipeline failed'
        }
    }
}