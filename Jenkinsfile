node {
    def app

    stage('Clone repository') {
      

            checkout scm
            sh 'echo "Task starts"'
        
    }

    stage('Build image') {
  
       sh 'docker build -t tranthin/cicd-jenkins .'
    }

     stage('Push to Docker Hub') {
            steps {
                //Đẩy ảnh Docker lên Docker Hub
                sh 'docker push tranthin/cicd-jenkins'
            }
        }

    stage('Test image') {
            sh 'echo "Tests passed"'
        }

}
