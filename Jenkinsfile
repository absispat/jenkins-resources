pipeline {
   agent any

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

                 echo $testp
            '''
         }
      }
      stage('Deploy') {
         steps {
            sh '''
                 echo $testp
                 testp="hello"
            '''
         }
      }
      stage('Test') {
         steps {
            sh '''
                 echo $testp
            '''
         }
      }
   }
}
