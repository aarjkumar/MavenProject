pipeline { 
    agent any 
    stages {
        stage('Build') { 
            steps {
                withMaven(maven : '/home/ubuntu/my-app'){
                        bat "mvn clean compile"
                }
            }
        }
        stage('Test'){
            steps {
                withMaven(maven : '/home/ubuntu/my-app'){
                        bat "mvn test"
                }

            }
        }
        stage('Deploy') {
            steps {
               withMaven(maven : '/home/ubuntu/my-app'){
                        bat "mvn deploy"
                }

            }
        }
    }
}
