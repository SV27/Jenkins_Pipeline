pipeline{
    agent any

    tools {
        maven 'maven_3.6.3'
        jdk 'jdk8'
    }

    stages{
        stage("clean"){
            steps{
                sh 'mvn clean'
            }
        }

        stage("compile") {
            steps {
                sh 'mvn compile'
            }
        }

        stage("test") {
            steps {
                sh 'mvn test'
            }
        }

        stage("package") {
            steps {
                sh 'mvn package'
            }
        }
    }

    post{
        always{
            cleanWs()
        }
        success{
            echo "========pipeline executed successfully ========"
        }
        failure{
            echo "========pipeline execution failed========"
        }
    }
}
