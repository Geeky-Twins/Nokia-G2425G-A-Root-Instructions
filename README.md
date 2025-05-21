# Nokia-G2425G-A-Root-Instructions

										
				1. take backup from ONT

				2. install python -> pip install pycryptodome
										
				3. download and save script from https://gist.github.com/rajkosto/e2b2455d457cc2be82dbb5c85e22d708 as nokia_tool.py
				
				4. open command prompt
						
				python nokia_tool.py -d OYdLWUVDdKQTPaCIeTqniA==
				
				python nokia_tool.py -u config.cfg
				
				5. Search for in the xml file
				
				a. TelnetSshAccount -> true, ONTUSER, mybigpassword
				IMPORTANT!!!!!
							If your password line looks like this:
							<Password ml="64" rw="RW" t="string" v="mybigpassword" ealgo="ab"></Password>
							then please change it to 
							<Password ml="64" rw="RW" t="string" v="mybigpassword"></Password>
							
				b. LimitAccount_ONTUSER -> false
				
				6. encrypt and rename config.cfg
				
				7. telnet 192.168.1.1
				
				ritool dump
				
				ritool set OperatorID ALCL
				
				8. Hard Reset
				
				9. 192.168.1.254
				
				Username:AdminGPON
				Password:ALC#FGU
				
				10. For locking back, use ritool set OperatorID BRTI after enabling telnet and then hard reset
								
								
