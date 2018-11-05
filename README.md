# SalesForce_vCard
Salesforce can allow users in your org to share vCards for Free!


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

Note, you may also want to use the visualforce substitute function to wrap this. 

Additionally you need to create a contact vustom detail page button and add it to the page layout of the contact record. 

Display in New Window (URL): 

`/apex/testVcard?id={!Contact.Id}`


