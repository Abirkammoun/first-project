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
	    stage("Supprimer le contenu du dossier target") {
            steps {
                script {
                    //this step attempts to clean the files and directories generated by Maven during its build
                    bat "mvn clean"
                }
            }
        }
        stage ("Creation du livrable"){
			steps{
				bat "mvn package -DskipTests=true"
			}
		}
        
        	
    }
}


        
