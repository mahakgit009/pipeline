pipeline{
    agent{
        label{
		    label 'built-in'
		}	
	}
	stages{
	    
		stage ('master'){
		        steps{
				    sh "yum install httpd -y"
					sh "service httpd start"
					sh "cp -r index.html /var/www/html"
					sh "chmod -R 777 /var/www/html/index.html"
					
				}
		}
		stage ('node-1'){
            
			agent{
              
			    label{
		            
					label "172.31.37.254"
		        }	
	        }
			
			steps{
			      sh "yum install httpd -y"
					sh "service httpd start"
					sh "cp -r index.html /var/www/html"
					sh "chmod -R 777 /var/www/html/index.html"
			}
    		
		}
		stage ('node-2'){
            
			agent{
              
			    label{
		             label "172.31.45.123"
		        }	
	        }
			steps{
			        sh "yum install httpd -y"
				    sh "service httpd start"
				 	sh "cp -r index.html /var/www/html"
					sh "chmod -R 777 /var/www/html/index.html"
			}
    		
		}
	}
}
