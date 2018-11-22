pipeline {
  agent any
  stages {
      stage('Build') {
        steps {
          sh '/usr/local/share/dotnet/dotnet msbuild'
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
