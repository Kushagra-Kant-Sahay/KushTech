pipeline {
    agent any
  
  stages {
    stage('Build’){

node {
// Checkout
git branch: ‘main’,url: ‘https://github.com/Kushagra-Kant-Sahay/KushTechonlogies.git';

// install required bundles
sh ‘bundle install’

// build and run tests with coverage
sh ‘bundle exec rake build spec’

// Archive the built artifacts
archive (includes: ‘pkg/*.gem’)

publishHTML([allowMissing: false, alwaysLinkToLastBuild: false, keepAll: false, reportDir: ‘coverage’, reportFiles: ‘index.html’, reportName: ‘Kush Technologies’, reportTitles: ‘Coverage Report’])
}
}
stage('Test') {
            steps {
               echo "testapp"
            }
            }
        stage('Deploy') {
            steps{
                echo "deployapp"
            }
        }
}

post {
                always
                {
                    mail body: 'Pipeline was triggered build tested and code has no error woohhlaahhh', from: 'trickygyan818@gmail.com', subject: 'Pipeline Triggered', to: 'diksha1999tripathi@gmail.com'
                }
            }
}
