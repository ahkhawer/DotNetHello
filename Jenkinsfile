pipeline {
  agent any
  stages {
      stage('Build') {
        steps {
          sh '/usr/local/share/dotnet msbuild'
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
