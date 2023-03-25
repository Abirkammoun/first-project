pipeline {

    agent any
   // triggers {
     // cron('*/4 * * * *')

//    } 

    stages {
    //   stage ('GIT') {
     //       steps {
      //         echo "Getting Project from Git"; 
       //        git branch:"Haifa", url : "https://github.com/achrafchourabi/TimesheetWaves.git"; 
       //     }
        //}

       stage("Verification du version Maven") {
           steps {
                bat "mvn -version"
              
            }
        }
	
        	
    }
}