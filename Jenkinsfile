node('built-in')
{
    
    stage('Continuous_Download_built_in') 
    {
    git branch: 'main', url: 'https://github.com/rajesh-jagtap/maven55.git'
    }
    stage('Continuous_Build_built_in') 
    {
    sh 'mvn package '
    }
    stage('Continuous_Deployement_built_in') 
    {
    sh 'scp /home/ubuntu/.jenkins/workspace/Scripted_Pipeline/webapp/target/webapp.war ubuntu@172.31.22.58:/var/lib/tomcat9/webapps/qaapp.war'
    }
    
    
    
}
