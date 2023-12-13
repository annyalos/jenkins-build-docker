
node {

  
   def IMAGE="srv-web-ludo"
	
    stage('Clone') {
          checkout scm
    }

    stage('Build') {
          docker.build("$IMAGE",  '.')
    }

    stage('Run image') {
        docker.image('srv-web-ludo').withRun('--name srv_web-patrick' ) { c ->

        sh 'docker ps | grep srv_web-ludo'
	}

    }
}
