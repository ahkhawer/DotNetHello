pipeline {
  agent any
  stages {
      stage('Build') {
        steps {
          sh '/Library/Frameworks/Mono.framework/Versions/Current/Commands/msbuild'
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
