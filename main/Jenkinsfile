pipeline{
    agent any
    stages {
        stage('Build'){
            steps{
                sh 'g++ -o PES2UG20CS400-1 fresh.cpp'
//                 sh 'make Makefile'
                echo 'Build stage successful'
            }
        }
        stage('Test'){
            steps{
                sh './PES2UG20CS400-1'
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
