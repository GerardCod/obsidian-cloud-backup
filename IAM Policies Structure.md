#Security #IAM 

- Consists of
	-  Version:policylanguageversion,alwaysinclude“2012-10- 17”
	- Id:anidentifierforthepolicy(optional)
	- Statement:oneormoreindividualstatements(required)

- Statements consists of
	- Sid:anidentifierforthestatement(optional)
	- Effect:whetherthestatementallowsordeniesaccess (Allow, Deny)
	- Principal:account/user/roletowhichthispolicyappliedto
	- Action:listofactionsthispolicyallowsordenies
	- Resource:listofresourcestowhichtheactionsappliedto
	- Condition:conditionsforwhenthispolicyisineffect (optional)
	
![[Captura de pantalla 2024-03-13 a la(s) 12.40.15 a.m..png]]
