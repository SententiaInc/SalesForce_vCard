# SalesForce_vCard
Salesforce can be updated to allow your users to share vCards for Free!

A visualforce page can be configured to export contact data that can be forwarded onto vendors and customers to facilitate easy communication!


![alt text](https://github.com/SententiaInc/Salesforce_vCard/blob/master/Cover.PNG "Vanilla Javascript SOQL JSON Example")

YouTube Tutorial: <br/> 

<a href="http://www.youtube.com/watch?feature=player_embedded&v=8vu1sgmxLew
" target="_blank"><img src="http://img.youtube.com/vi/8vu1sgmxLew/0.jpg" 
alt="Tutorial" width="240" height="180" border="10" /></a>


Visualforce Page Code Sample includes content type tag example that exports different file types 
Apex contenttype attribute example: 
`contenttype="text/vcard; charset=iso-8859-1 #export.vcf"`

VCard 4.0 format adapted from: https://en.wikipedia.org/wiki/VCard

You will need to enhance the code to include fields that you want to include

Example: 

If you want to pre-populate a contact name you must edit the following line to include

`N:Gump;Forest;;Mr.;`

To: 

`N:Gump;{!contact.FirstName};;Mr.;`

Note, you may also want to use the visualforce substitute function to wrap this for characters that may cause issues.

Additionally you need to create a contact custom detail page button and add it to the page layout of the contact record. 

Display in New Window (URL): 

`/apex/testVcard?id={!Contact.Id}`

![alt text](https://github.com/SententiaInc/Salesforce_vCard/blob/master/buttonCode.PNG "Vanilla Javascript SOQL JSON Example")


