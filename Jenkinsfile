node{
  stage('SCM Checkout'){
     git 'https://github.com/aggiramaiah/my-apps'
   }
   stage('Compile-package'){
   // Get Maven Hpme Path
   def mvnHome = tool name: 'maven-1', type: 'maven'
     sh "${mvnHome}/bin/mvn package"
   }
   stage('Email Notification'){
   mail bcc: '', body: '''Hi,
   Welcome to jenkins Job Notification
   Thabka
   Aggi''', cc: '', from: '', replyTo: '', subject: 'Jenkins Job', to: 'aggiramaiah@gmail.com'
   }

}
