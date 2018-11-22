pipeline {
  agent any
  tools{
    msbuild '/Library/Frameworks/Mono.framework/Versions/Current/Commands/msbuild'
  }
  stages {
      stage('Build') {
        steps {
          sh 'msbuild'
        }
      }
      stage('Test') {
        steps {
          echo "Testing"
        }
      }
      stage('Deliver') {
        steps {
          sh './jenkins/scripts/deliver.sh'
        }
      }
  }
}
