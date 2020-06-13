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
                 testp="hello"
                 echo $testp
            '''
         }
      }
      stage('Deploy') {
         steps {

                 echo $testp
            '''
         }
   }
}
