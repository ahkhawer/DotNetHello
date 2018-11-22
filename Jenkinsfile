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
          sh 'sudo $dotnet bin/Debug/netcoreapp2.1/DotNetHello.dll'
          //sh './jenkins/scripts/deliver.sh'
        }
      }
  }
}
