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
                    def buildWrapperHome = tool 'sonarqube_build_wrapper_prd'
                    sonar_analyzer = "${buildWrapperHome}/build-wrapper-linux-x86-64 --out-dir ${WORKSPACE}/sonarqube_build_wrapper"

                    withSonarQubeEnv('sonar_cloud') {
                        sh """
                            printenv
                        """
                    }
            }
        }
    }
}
