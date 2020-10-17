pipeline{
    agent any

    tools {
        maven 'maven_3.6.3'
        jdk 'jdk8'
    }

    stages{
        stage("verify"){
            steps{
                    sh 'mvn version'
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
