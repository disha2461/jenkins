pipeline {
    agent { node { label 'AGENT-1' } }

    stages {
        stage('Build') {
            steps {
                echo 'Building..'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
                error 'fails'
            }
        }
    }
    post { 
        always { 
            echo 'I will always wheater the job is success or not'
        }
        success{
            echo 'i will run always when the job is success'
        }
        failure{
            echo 'I will run when the job fails'
        }
    }
}