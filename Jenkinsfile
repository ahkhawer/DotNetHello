pipeline {
  agent any
  stages {
      stage('Build') {
        steps {
          sh '${msbuild}'
        }
      }
      stage('Test') {
        steps {
          echo "Testing"
        }
      }
      stage('Deliver') {
        steps {
          sh 'dotnet bin/Debug/netcoreapp2.1/DotNetHello.dll'
          //sh './jenkins/scripts/deliver.sh'
        }
      }
  }
}
