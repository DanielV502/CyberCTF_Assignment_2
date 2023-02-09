# CyberCTF_Assignment_2

### 3. Challenge: basic-mod1 (Hard)

* The challenge requests the analysis of a weird message on the network.
* There was some instructions about getting the MOD of each part of the code we found on the downloaded message.
* The MOD37 of the message was uploaded on a Substitution Decoder Tool as the example of the mapped characters.

![R2_C3_1](https://user-images.githubusercontent.com/124681007/217738255-f79d87e4-cab9-4917-8453-0253d6aa2dc9.png)

* Now we can get the flag:

> The flag is: **“picoCTF{R0UND_N_R0UND_79C18FB3}”**

* This was kind of a manual process, we can automate it a bit of the process with some code:

		x=0
		flag="Flag: picoCTF{"
		List=["A","B","C","D","E","F","G","H","I","J","K","L","M","N","O","P","Q","R","S","T","U","V","W","X","Y","Z",0,1,2,3,4,5,6,7,8,9,"_"]
		List2=[54,396,131,198,225,258,87,258,128,211,57,235,114,258,144,220,39,175,330,338,297,288]
		List3=[]

		for listado in List2:
				List3.append(listado%37)

		for decoding in List3:
				flag=flag+str(List[decoding])

		print(flag+"}")

![R2_C3_2](https://user-images.githubusercontent.com/124681007/217740590-3cdca0ad-14b2-4fb1-b80a-702e93fbd3b7.png)

* This program in python will give us the flag in a more efficient way.
