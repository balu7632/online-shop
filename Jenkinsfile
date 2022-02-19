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
        sh 'docker push vardhanns/phpmysql_app'
        */
        //docker.withRegistry( 'https://registry.hub.docker.com', 'DockerHubPassword' ) {
             
             sh 'sudo docker login -u "upasanatestdocker" -p "Zephyr@17" docker.io'
             //sh 'sudo docker push upasanatestdocker/mysql'
             //sh 'sudo docker push upasanatestdocker/job1_web1.0'
             sh 'sudo docker push upasanatestdocker/job1_web2.0'
            // sh 'docker push upasanatestdocker/mysql'
          
    }
}
