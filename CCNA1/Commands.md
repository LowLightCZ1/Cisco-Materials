### ___Basic device commands___
- __Commands__
	__enable__ - access to privileged EXEC mode
	__disable__ - return to user EXEC mode
	__configure terminal__ - access to global configuration mode
	__exit__ -  return to privileged EXEC mode
	__line (console 0)__ - enter the line subconfiguration mode
	__end or Ctrl+Z__ - from any subconfiguration mode to the privileged EXEC mode
- __Device Name__
	 - _Rules_:
		 - Starts with a latter
		 - Contain no spaces
		 - End with a letter or digit
		 - Use only letters, digits and dashes
		 - Less than 64 characters in length
	Switch# `configure terminal`
	Switch(config)# `hostname Sw-Floor-1`
	Sw-Floor-1(config)#
	- `no hostname` - return default prompt
- __Passwords Guide__ 
	- Default password
		Sw-Floor-1(config)# `line console 0`
		Sw-Floor-1(config-line)# `password "cisco"`
		Sw-Floor-1(config-line)# `login`
		Sw-Floor-1(config-line)# `end`
	- Secret password
		Sw-Floor-1(config)# `enable secret class`
		Sw-Floor-1(config)# `exit`
	- Encrypt password
		Sw-Floor-1(config)# `service password-encryptio`
		Sw-Floor-1(config)# `end`
	- _Banner motd(Motho of today)_ - `banner motd #Authorized Access Only#`
- 