pipeline{
    agent any

    stages{
        stage("verify"){
            steps{
                withMaven('maven_3.6.3') {
                    sh 'mvn version'
                }
            }
        }
    }
    post{
        always{
            echo "========always========"
        }
        success{
            echo "========pipeline executed successfully ========"
        }
        failure{
            echo "========pipeline execution failed========"
        }
    }
}
