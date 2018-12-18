node('master') 
{
    stage('ContinuousDownload')
    {
       git 'https://github.com/selenium-saikrishna/maven.git'
    }
    stage('ContinuousBuild')
    {
       sh 'mvn package'
    }
    stage('ContinuousDeployment')
    {
	 sh 'scp /var/lib/jenkins/workspace/dev/webapp/target/webapp.war ubuntu@172.31.9.132:/var/lib/tomcat7/webapps/qaenv2.war'
    }   
}
