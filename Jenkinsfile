node{
   stage('SCM Checkout'){
     git 'https://github.com/javahometech/my-app'
   }
   stage('Compile-Package'){
      // Get maven home path
      def mvnHome =  tool name: 'maven-3', type: 'maven'   
      sh "${mvnHome}/bin/mvn package"
   }
   stage('Email Notification'){
       mail bcc: '', body: 'this is a test email through jenkins', cc: '', from: '', replyTo: '', 
       subject: 'test email through jenkins', to: 'ogoit.svm@gmail.com'
   }
}


