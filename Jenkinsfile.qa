pipeline{
    agent any
  
    stages{
        
        stage('git clone')
        {
           steps{
               echo "git https://github.com/Ashutosh558/Exponent-Maven-Web-app-DevOps.git"
           } 
        }
        stage('maven build')
        {
            steps{
                echo "mvn clean package"
            }
        }
        stage('deploy on tomcat')
        {
            steps{
                echo "deploy adapters: [tomcat9(credentialsId: '8f6b5249-ab7c-4b2e-a0dc-2eb421288c68', path: '', url: 'http://15.206.189.166:9000/')], contextPath: 'my-app', war: '**/*.war"
            }
        }
    }
}
