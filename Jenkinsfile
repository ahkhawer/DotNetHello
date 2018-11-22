pipeline {
  agent any
  tools{
    MSBuild /Library/Frameworks/Mono.framework/Versions/Current/Commands/msbuild
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
