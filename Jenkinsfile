// Powered by Infostretch 

timestamps {

node () {

	stage ('icicibank -dev - Checkout') {
 	 checkout([$class: 'GitSCM', branches: [[name: '*/master']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[credentialsId: 'a3cc0927-12e4-4932-8f53-fb3e92fe4e8b', url: 'https://github.com/lokeshsgithub/maven-web-application-warfile.git']]]) 
	}
	stage ('icicibank -dev - Build') {
 	
// Unable to convert a build step referring to "hudson.plugins.ws__cleanup.PreBuildCleanup". Please verify and convert manually if required.
// Unable to convert a build step referring to "hudson.plugins.timestamper.TimestamperBuildWrapper". Please verify and convert manually if required.		// Maven build step
	withMaven(maven: 'maven.3.8.6') { 
 			if(isUnix()) {
 				sh "mvn clean sonar:sonar deploy " 
			} else { 
 				bat "mvn clean sonar:sonar deploy " 
			} 
 		} 
	}
}
}