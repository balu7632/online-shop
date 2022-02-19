node{

    stage('SCM Checkout')
    {
        git 'https://github.com/balu7632/online-shop.git'
    }
    
    stage('Run Docker Compose File')
    {
        sh 'sudo docker-compose build'
        sh 'sudo docker-compose up -d'
    }
  stage('PUSH image to Docker Hub')
    {
      /* withCredentials([string(credentialsId: 'docker-pwd', variable: 'dockerhubpwd')]) 
        {
            sh "docker login -u balu7632 -p ${dockerhubpwd}"
        }
        sh 'docker push balu7632/phpmysql_app'
        */
        //docker.withRegistry( 'https://registry.hub.docker.com', 'dockerhubpwd' ) {
             
             sh 'sudo docker login -u "balu7632" -p "9010651040@reddes" docker.io'
             //sh 'sudo docker push balu7632/mysql'
             //sh 'sudo docker push balu7632/job1_web1.0'
             sh 'sudo docker push balu7632/job1_web2.0'
            // sh 'docker push balu7632/mysql'
          
    }
}
