pipeline {
  agent any
  tools{
    MSBuild 'MSBuild_Default'
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
