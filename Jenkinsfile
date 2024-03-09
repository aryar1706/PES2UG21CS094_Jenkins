pipeline{
  agent any
  stages{
       // stage('Clone repository'){
          //steps{
            //checkout([$class:'GitSCM',
                     //branches: [[name:'*/main']],
                     //userRemoteConfigs:[[url:'https://github.com/aryar1706/Jenkins.git']]])
        //  }
        //}
    stage('Build'){
      steps{
        build 'PES2UG21CS094-1'
        sh 'g++ main.cpp -o output'
      }
    }
    stage('Test'){
      steps{
        sh './output'
      }
    }
    stage('Deploy'){
      steps{
        sh './non_existing_command'
        echo 'deploy'
      }
    }
  }
  post{
    failure{
      error 'Pipeline failed'
    }
  }
}
