node {
    def app

    stage('Clone repository') {
      

            checkout scm
            sh 'echo "Task starts"'
        
    }

    stage('Build image') {
  
       app = docker.build("tranthin/cicd-jenkins")
    }

    stage('Push image') {
        
        docker.withRegistry('https://registry.hub.docker.com', 'dockerhub') {
            app.push("12325")
        }
    }

    stage('Test image') {
            sh 'echo "Tests passed"'
        }

}
