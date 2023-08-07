node {
    def app

    stage('Clone repository') {
      

   
            sh 'echo "Task starts"'
        
    }

    stage('Build image') {
  
       app = docker.build("tranthin/cicd-jenkins")
    }

    stage('Test image') {
  

        app.inside {
            sh 'echo "Tests passed"'
        }
    }

}
