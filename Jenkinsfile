node('built-in')
{
    
    stage('Continuous_Download_loans') 
    {
    git branch: 'main', url: 'https://github.com/rajesh-jagtap/maven55.git'
    }
    stage('Continuous_Build_loans') 
    {
    sh 'mvn package '
    }
    
}
