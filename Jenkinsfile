pipeline {
    agent {
      label 'scheduler'
    }
    stages {
        stage ('Initialize') {
            steps {
                echo "Hello Oleksiy! Change 22"
            }
        }
        stage ('Build') {
            steps {
                sh 'pwd'
            }
        }
    }
}
