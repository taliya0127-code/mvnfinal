pipeline 
{
  agent any
  stages
  {
   stage ('Build')
   {
    steps
    {
      bat 'mvn clean package'
    }
  }
   stage ('Test')
   {
    steps 
     {
      bat 'mvn test'
     }
   }
   stage ('Run application')
   {
    steps
    {
      bat 'java-jar mymaven-1.0-SNAPSHOT.jar'
    }
   }
 }
 post
{ 
  success
   {
     echo 'Build Success'
   }
   failure
   { 
     echo 'Failed'
   }
  }
 }
