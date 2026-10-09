pipeline{
  agent any
  stages{
    stage(''' Stage 1 - Basic Setup '''){
      steps{
        sh '''
          apt update -y
          apt upgrade -y
          apt install sudo -y
          apt install docker.io docker-compose -y
          service docker start
          service docker status
          docker image build -t oklabs/myimage:t${BUILD_NUMBER} -f Dockerfile.myapp .
        '''
      }
    }
  }
  
}
