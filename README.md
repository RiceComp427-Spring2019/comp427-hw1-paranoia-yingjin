# <img src="http://www.rice.edu/_images/rice-logo.jpg" width=180> Comp427, Spring 2018, Homework 1
## Rational Paranoia
The homework specifications, as well as the corresponding course slide decks,
can be found on the [Comp427 Piazza](https://piazza.com/class/jqifhp864b37ju).
This assignment is due **Thursday, January 17 at 6 p.m.**

You will do this homework by editing the _README.md_ file. It's in
[MarkDown format](https://guides.github.com/features/mastering-markdown/)
and will be rendered to beautiful HTML when you visit your GitHub repo.

## Student Information
Please also edit _README.md_ and replace your instructor's name and NetID with your own:

_Student name_: Ying Jin

_Student NetID_: yj4

Your NetID is typically your initials and a numeric digit. That's
what we need here.

_If you contacted us in advance and we approved a late submission,
please cut-and-paste the text from that email here._

## Problem 1
- Scenario: {Documents}

As head of IT for an international law firm, you are responsible for a document management system; 
some documents stored there are about sensitive legal, financial, or political matters.


- Assumptions:
  - The employees who works in the law firm are all properly trained and know the rules of
  	keeping sensitive information private. They are not allowed to copy the sensitive files
  	onto a removable devices and take them back home, or in the car which expose more potential 
  	threats to having the files being stolen.
  - The authentication of the file system is by ip address and username + password. 
  	employees have to login to the private network to access the file system.
  - The file management system keeps an employee database with proper access control information
  	and detailed logs of the file access history.
  
- Assets:
  - The sensitive information that stored in some of the files.
  	Since these files might includes 
  	client financial, legal or political information, they should be kept private
  	and categorized at different security level, only authorized personnel could 
  	gain the access of appropriate level of files.  
  	
  - All the files that are stored inside the file management system.
  	All the files should be kept safe; 
  	These files are essential documents for the law firm to perform it's daily tasks, 
  	and successfully run its business. They should be checksum checked frequently to make
  	sure its integrity. 
	  
  - The physical server that host the file system. 
  	The physical server should be kept in an appropriate environment that suitable 
  	for hardware to sustain. To prevent from potential loss, the file system should be
  	versioned, backed up, and keep backup in a different geographical location.
  
  - Availablility of the files. 
  	Some of files maybe time sensitive. If for any reason the 
  	files become unavailable for a period of time, it might cause damage of the reputation
  	of the firm, or loss of the case, etc.

- Threats:
  - The hackers might want to hack into the system and steal sensitive information.
  	For example, the financial information could be used to attack one's bank account and 
  	steal money; The political information might be used to by 
  	someone to attack one's campaign; The legal information might be used by the other 
  	party to win the case, etc. 
  - An enemy may just want to damage the files to ruin the law firm from doing its business.
  - The hardware failure of the file systems may affect the integrity and/or the availability
  	of the files.
  - The software bugs might have impact on security of the system and/or the integrity
  	of the files
  - The natural disasters like fire, flood, and earthquake etc. may destroy the physical
  	file system servers.
  - The network might be attacked by DOS or other internet intrusions and affect the 
  	availabilities of the files system. 
  - The employee's computer might get compromised and being used by attackers to gain
  	illegal access to the file system
  - The files might be altered or dropped by accident of authorized users or by 
  	malicious attackers. 
  
- Countermeasures:
  - For files contain sensitive information, they should be encrypted or make it
  	password protected. It means better security, but there are extra cost for 
  	encryption and un-encryption, and people may forgot the password, etc.
  - For files with super sensitive information, it might be a good idea not to put them in a
  	digital form, but make a hard copy and keep them in a safe. However, the availability
  	of the file will be very limited and if anything happens to the hard copy, it's hard to
  	recover.
  - Ideally we should maintain at least two backups. 
  	One of the backups should be kept in a different geographical location. However, not 
  	mention the cost, considering how sensitive files are, the security of the 
  	backup system is a big concern too. 
  	- Keep a local backup of the files on the hard disks 
  	  and save them in a safe provides a fast way to recover the files when the integrity or 
  	  availability of the file system are compromised. Even though keeping a separate hard 
  	  copy is very labor intensive (depends on how long you sync the files), and it might 
  	  not survive from nature disasters, it worths
  	  the effort if the availability of the files are on the very top of the priority.
  	- In case of the files are being altered or dropped by accident of authorized users or by 
  	  malicious attackers, a direct backup copy or a versioned copy should be available to 
  	  recover the file to its most recent state.
  	- More frequent backup and keeping them for a longer period of time, means a better 
  	  recovery when they are needed. Of course to do so taking more storage and more network 
  	  transactions to make the backup. It requires more bandwidth, costs more money for 
  	  storage and rises some security concern too during the transport.
  - The OS and software run on the file system should be patched/upgraded consistently, 
  	especially when there are security concerns about the software. This will add extra cost
  	for the maintenance time, potential other bugs, or the software upgraded not compatible 
  	to another, etc. A recovery plan should be in place if such a patch or upgrade failed. 
  	Mitigate between how often these tasks should be executed and keep the system at most secure
  	state should be considered.
  - The hardware should be actively maintained or immediately repaired, e.g. replace failed 
  	disks or damaged network cables, etc. Keep a redundancy, using RAID or other new 
  	technologies to mitigate potential hardware failure.
  - To protect the availability of the file system in case of network attacks like DoS, the
    extra layer of security, like firewalls and proxy servers are needed. Some mitigation 
    services might perform better on detecting and fighting the DoS attack but they can be
    very expensive.

  	 
## Problem 2
- Scenario: {TSA}

As head of the TSA, you set the rules for screening passengers at airport checkpoints.

- Assumptions:
  - The purpose of the screening is to find out if the passengers are carrying weapons, explosives or
  	life threatening devices that could be used to hijack the plane, perform the terrorist attack or
  	wound/death of the other passengers. Any other illegal items are carried with passengers might
  	be reported to the police, but excluded from screening procedure policy. 
  - Assume that the TSA system is networked with some other databases that provide the 
  	information to help them identify potential high risk passengers
  	so that those passengers will be screened with more cautious.
  - Assume all the staff working on the screening are properly trained to follow the rules
  	
- Assets:
  - The safety of everyone in the airport - airport employees, the passagers, etc. Airports are known 
  	target for terrorists to attack since it's crowdedness. Keeping it a safe environment is
  	very critical.
  - The airplane and the passengers on the plane. The hijackers might want to on hold of the plane
  	to take them to different destinations, take passengers as hostage for ransoms, or like in 9/11,
  	perform terrorist attack to cause more death and damages.
  - The image or data that collected on the screening devices are considered private.
  	They should be protected from being hacked or misused.
  - The properties of the passangers. The screening procedure or devices should not cause the
  	damage of passenger's properties. 
  - The health of the passengers. The screening procedure or devices should not cause the
  	damage of passengers health. If the passenger's physical condition are not appropriate to 
  	take certain screening, they may request a pat down.
  - Keep the normal operation of the aviation system (availability) with volume of the passengers 
  	growing. To address that, we need to increase the checkpoint performances, screening process 
  	has to effectively and efficiently detect threats, reduce false alarms and facilitate 
  	the flow of legitimate passengers and trades.
  - The screening equipment. These high technology equipment might become the target of the 
  	attackers trying to compromise - having it not working or not working properly.
  
- Threats:
  - The attackers might take false or forged documentation to avoid being identified
  	as who they are. 
  - The attackers might take guns, other weapons like sharp metals, explosives, the 
  	harmful chemicals in gel or liquid forms, etc.  Both passengers and their carry on 
  	baggages should be screened for these known threats/technologies.
  - The attackers might use a new weapon or technology that our current screening system
  	is not capable to detect.   
  - Human errors. With already large volume of the passengers each day, and it is still
    growing, the screening process involving humans are facing more challenges. The staff can 
    get tired and become less alert, probability of missing the threats would increase.
  - Automation system limitations. The algorithm implemented for automation the screening 
  	or threat detection might not be perfect to detect all the threats.
  - Hackers could attack the computer system and get hold of the images that are
  	taking during the screening. These images might be used to attack the passengers. Or 
  	the attackers could hack in and compromise the automation process.
  - The volume of the passengers. With large number of passengers to screen, the waiting time
  	might take too long to have the operations run normally.
  
- Countermeasures:
  - With number of passengers we have to scan each day, we would like to minimize the overall
  	waiting time, increase the efficiency of the screening process, but still effectively
  	catch the potential threats. We might ask this question, "Do we have to screen everyone
  	with great details?" probably not. Here is some solutions to balance the quantities vs 
  	qualities -
  	- Having people pre-check themselves. If people could identify themselves as very 
  	  low-risk individuals by having their background pre-checked, they could go through
  	  a checkpoint with less security screened. However, doing so
  	  is risky. People with clean background is not necessarily criminal free. Another risk is
  	  the attackers might be able to forge himself/herself as a pre-check person. Using a 
  	  strong authentication system to help us identify the false or forged documents is important.
  	- Discover the high-risk people. This can be done by matching the travelers with criminal 
  	  database and having these people screened with more cautious. 
  	- Improve the performance of the screening process
  	Though pre-check is risky, it helps us to leverage the resources, focusing on the medium/high risk
  	individuals and improve the overall traveler experiences. 
  	   
  - Replacing some screening process with automation systems could help us reduce human errors and
  	improve the performance. But the automations systems have it's own limitations. It might
  	disfunction, get hacked, or containing bugs.
  - Stay on top of the new technology. Periodically re-visit and re-assess of the current
  	screening technology, equipment and process, update/upgrade/replace them with new equipment and 
  	design new process to increase the capability of finding new threats and improve the 
  	performance of the screening. However, they are not only very expensive, the amount of 
  	time to implement them are very challenge too.
  - Screening records. The images and data are taken during the screening process could be
    valuable resources. They can be used to feed big data analysis, machine self-learning, etc.
    as a result, it can improve the threat analysis algorithm or image qualities.
  	However, these information are privacy of the passengers. Wether Keeping them in a safe storage 
  	for research only or deleting them after the safety check-in is a challenge question. 
  - Be ready for the new threats. We try our best to detect the known threats. However, the 
    enemy might find the new weapons or technologies that could by-pass the checkpoint and
  	being used to perform the attacks. Having the staff and the resources ready to quickly 
  	response to those new threats information and deploy the new technology to defense it 
  	are challenge but necessary.


## Problem 3
- Scenario: I am a security consultant working with companies that develop software that run 
	on IoT (Internet of Things) devices.
- Assumptions:
  - IoT industrial have a standardized API protocols and all menufactures would follow
  	the API
  - Home-use IoT and Commercial-use IoT have some security overlaps. However, in the following
  	threat modeling, it only consider the security for the IoT that being used in consumer's home.
  - There are possibility that the out of the box IoT production has been compromised on board. 
  	We assume that is not the case in the following model.
  - All the devices, including TVs, cars, light bulb or the HVAC system, we assume they are all internet
  	connected things here.
- Assets:
  - The availability of the IoT devices. It is essential for the consumers to have the 
  	functioning devices which are also accessable from consumer's phone or other controlling interface.
  - The data - either the photos/videos taking using cameras, or the data collected from 
  	the devices like thermometers, ovens, cars, TVs, etc. We need to make sure these data's integrity,
  	they are from the known devices and be authentic. 
  - Confidentiality. All the data collected from IoT devices are considered private.
  	Since all data need to be transferred over the network. They should be encrypted to 
  	protect its integrity and confidentiality. 
  - Consumer's safety. If the devices were taking over by the attackers, like security
  	cameras, the cars, or the HVAC systems, not only it would expose the privacy of the consumer, 
  	it could be life threatening to them too. 
  
- Threats:
  - The attackers can deploy the DoS attack to the devices and make them not available.
  - All IoT devices have some computing powers, as they have the ability to connect to the internet,
  	recieving/sending signals, messages or even audio/video, etc. The attacker could compromise the
  	chip and use it to facilitate DDos attack.
  - Lack or weak encryption of transport. With limited computing power, implement sophisticated encryption
  	algorithm could take long time to compute. Without encryption or with weak encryption, when 
  	the consumer exposed themself in an insecure network, any user of that network could view the data
  	or decrypt it if a weak encryption used.  
  - Weak password for account of the device, mobile apps or data storage (e.g. cloud) service account.
  	The consumer might not change the password or using weak password after connecting the 
  	devices to their network. Or using the weak password for the mobile apps, or cloud services.
  	That gives the hacker a good opportunity to hack into the system and gain control of the devices or 
  	the data.
  - Insecure network connections. The consumer might not secure their network properly or 
  	communicate to the devices over a public network connection which has no secure setup. This could 
  	result the devices being compromised, put data integrity in danger, and expose devices 
  	to Dos attack.
  - Security concern with the software or firmware on the IoT devices. The device may contain
  	hard coded credentials, security holes, etc.
  
- Countermeasures:
  - Firmware and software update/upgrade. The devices should have ability to get firmware/software 
  	upgraded for new features or security update. Of course the process has to be safe guarded 
  	with strong authentications and the updating process should be encrypted so that the files
  	won't be compromised during the transport. However, this is also expose the possibility for 
  	the attackers to hack in the devices via weak link of the security and update the devices 
  	for their own usage.
  - Authentication - User name and password. The device management UI should require the user to 
  	change the password when they first time setup the device and force a strong password. It requires
  	a secure "forget password" interface if the user forget their password. Even better if
  	the username can be changed too. However, adding that layer could introduce other security concerns,
  	like they have to provide more sensitive data to retrieve the username in case it is forgotten.
  - Encryption. Ideally, using a strong encryption is very important to protect the data integrity and 
  	confidentiality. However, adding that kind of computing power to a device like a light bulb probably
  	would make it cost too much to sell. 
  - Maintenance. It is easier for a device manufacture to design a backend interface to access the devices
  	for maintenance that they don't want the end user do. Like some special configuration that a consumer
  	would not understand how to do it and might accidentally set it up wrong. However, this back door 
  	might give the attacker a way of hack the device and taken over the devices.
  - For IoT devices, there is little human involvement for the devices to work. Most of the time, you can simple 
  	ask Alexa to turn on or off the light, or a google home to talk to your devices. It is hard to
  	discover if the devices are being comprised and taken over by someone and leaking data to them.
  	Some intelligent behavior analysis might be able to help for detecting such attack. How it could differentiate
  	the legitimate behavior vs. wrong doing is challenge. 


