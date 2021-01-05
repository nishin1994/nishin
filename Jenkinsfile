pipeline {
    agent none
    stages{
        stage('Build') {
            agent { label 'master' }
            steps {
                bat """
                echo $params.BRANCH
                echo 'Build Started'
                //call Make build
                echo 'Build Finished'
                """
                }
        }
        stage('Flash') {
            steps {
                echo 'Flash'
            }
        }
        stage('Pytest') {
            agent { label 'master' }
            steps {
                bat """
                echo 'Pytest Started'
                //call Make pytest
                echo 'Pytest Finished'
                """
            }
        }
        stage('Coverity') {
            steps {
                echo 'Coverity'
            }
        }
    }
}
