pipeline{

agent any

environment{
    version_name ="1.08"
}

stages{

stage("compile"){
steps
{
  bat "javac Test.java"
  bat 'echo "${version_name}"'
}
}

stage("run"){
steps{
  bat "java Test"
}
}
}

post{
   always{
   bat 'echo "always"'
   }
   
   success{
   bat 'echo "success"'
   }
   
   failure{
   bat 'echo "failure"'
   }
}

}