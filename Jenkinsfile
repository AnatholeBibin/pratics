pipeline{
  agent any
  stages {
      stage('Clone'){
        steps{
          sh "git clone https://github.com/AnatholeBibin/pratics.git"
      }
      }
      stage ('build'){
        steps{
        sh "cd pratics/ && docker build -t monimage_docker_pyth ."
      }
      }
      stage ('run')
        steps{
        sh "cd pratics/ && docker run -p 5000:5000 monimage_docker_pyth"
        }
      }
  }
}
