pipeline {
    agent any
  
  stages {
    stage('Build') {

        steps {

            echo "build"
              }
            }
stage('Test') {
            steps {
               echo "Webapp Tested"
            }
            }
        stage('Deploy') {
            steps{
                echo "Webapp Deployed"
            }
        }
}

post {
                always
                {
                    mail body: 'Pipeline was triggered build tested and code has no error woohhlaahhh', from: 'trickygyan818@gmail.com', subject: 'Pipeline Triggered', to: 'kksahay04@gmail.com'
                }
            }
}
