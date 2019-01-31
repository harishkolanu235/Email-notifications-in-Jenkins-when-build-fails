node
{
	try{
      stage('CheckoutCode')
      {
          git 'https://github.com/harishkolanu235/MavenProjectRepository'
      }
       stage('Build code')
      {
        sh 'mvn clean packages'
      }
      
	} catch (err) {
	    emailext body: "Cought Error: ${err}", subject: 'Build failed', to: 'harishk2305@gmail.com'
	  }
    
    
}
