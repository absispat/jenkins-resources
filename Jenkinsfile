pipeline {
   agent any

   environment {
       NAME = "$testp"
       secret = credentials('passhere')

   }

   stages {
      stage('Hello') {
         steps {
            echo 'Hello World'
         }
      }
      stage('Build') {
         steps {
            echo 'Hello Build'
            sh 'echo "trying sh"'
            sh '''
                 echo "first line"
                 date
                 ls
                 cd jenkins
                 ls

                 echo $NAME
            '''
         }
      }
      stage('Deploy') {
         steps {
            sh '''
                 echo $NAME
                 NAME="hello"
                 echo $NAME > env_start.txt
                 echo $NAME
                 ls
            '''
         }
      }
      stage('Test') {
         steps {
            sh '''
                 NAME=`cat env_start.txt`
                 echo $NAME
                 echo "this is secret $secret"
            '''
         }
      }
   }
}
