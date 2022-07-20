node('built-in')
{
    
    stage('Continuous_Download') 
    {
    git branch: 'main', url: 'https://github.com/rajesh-jagtap/maven55.git'
    }
    stage('Continuous_Build') 
    {
    sh 'mvn package '
    }
    stage('Continuous_Deployement') 
    {
    sh 'scp /home/ubuntu/.jenkins/workspace/Scripted_Pipeline/webapp/target/webapp.war ubuntu@172.31.22.58:/var/lib/tomcat9/webapps/qaapp.war'
    }
    stage('Continuous_Testing') 
    {
    git branch: 'main', url: 'https://github.com/rajesh-jagtap/testing55.git'
    sh ' java -jar /home/ubuntu/.jenkins/workspace/Scripted_Pipeline/testing.jar'
    }
    stage('Continuous_Delivery') 
    {
    input message: 'Wait for the approval of Delivery Manager', submitter: 'meena'
    sh 'scp /home/ubuntu/.jenkins/workspace/Scripted_Pipeline/webapp/target/webapp.war ubuntu@172.31.29.221:/var/lib/tomcat9/webapps/prodpp.war'
    }
    
    
    
}
