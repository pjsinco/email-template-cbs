#Steps to Send an Email
<hr>
###1. List Prep
* Open in Excel and eyeball
    * Every row should have a specialty
* Save as tab-delimited txt
    * Ex: ```cbs-expiration-aobim-im-primary-2017-02-27.txt```
* Open in Textmate
    * Add me as a recipient
    * Add the board's administrator as a recipient
    * Remove the header row
    * Save with
        * File Encoding: UTF8 
        * Line Endings:  LF 
* Verify correct formatting with ```csvlook``` on the command line
    * ```csvlook -t <filename>```

###2. Upload Subscriber List Informz
* Upload the list to Informz
    * ```Subscribers > Upload > Upload Subscribers```

* Upload the file
    * The Data Format should already exist.
        * Ex. for expiration emails, the Data Format is ```cbs-expiration```
    * Create a new interest, if needed
        * Ex: ```cbs-aobem```
        * Ex: ```cbs-aobim-im-primary```
    * **"Replace existing subscribers" should be checked**

###3. Create the Email
* Ex. Name: ```cbs-expiration-aobim-im-primary-2017-02-27```
* Template: ```CBS - Blank```
* Ex. To: ```Interests: cbs-aobim-im-primary```
* Ex. From:
      * Email Address: ```aobim@osteopathic.org```
      * Friendly From: ```American Osteopathic Board of Internal Medicine```
* Ex. Subject Line: ```Certification expiring```
* Ex. Reply To: ```aobim@osteopathic.org```
  

###Create the Email
* Run ```npm start``` to view the template in a browser
* Update ```/src/views/index.jade```
    * Set the board in the ```board``` variable
    * Set the ```exam``` mixin
    * **Verify that *Date* is correctly singular or plural** in "Your OCC Exam Date in 2017"
* Using Chrome Dev Tools, copy the email
    * Use "Copy OuterHTML" to copy the root table
* Paste into the Informz email
* Test and send



#Boards
AOBEM
American Osteopathic Board of Emergency Medicine

AOBIM
American Osteopathic Board of Internal Medicine

AOBFP
American Osteopathic Board of Family Physicians

AOBS 
American Osteopathic Board of Surgery

Sports Medicine
American Osteopathic Conjoint Sports Medicine Examination Committee

AOBD
American Osteopathic Board of Dermatology

AOBNMM
American Osteopathic Board of Neuromusculoskeletal Medicine

AOBPa
American Osteopathic Board of Pathology

AOBP
American Osteopathic Board of Pediatrics

AOBPMR
American Osteopathic Board of Physical Medicine and Rehabilitation

AOBPr
American Osteopathic Board of Proctology

AOBR
American Osteopathic Board of Radiology

###First go-round
AOBEM  
AOBIM  
AOBFP  
AOBS   
Sports Medicine  
AOBD  
AOBNMM  
AOBPa  
AOBP  
AOBPMR  
AOBPr  
AOBR  

#Variations

###Per batch
board  
board_friendly  
board_url  
board_phone  
board_email  


###Per individual
#####Direct
email  
last_name  
expiration  
specialty  

#####Derived
name ("Dr. [last_name]" | "Diplomate")  
eligibility_years (from [expiration_date])  





* [Good Copy • Email copy from great companies](http://www.goodemailcopy.com/)

* [Email Templates | MailChimp](https://mailchimp.com/features/email-templates/)

* [html - How to Put Text Over an Image (in email)? - Stack Overflow](http://stackoverflow.com/questions/39422875/how-to-put-text-over-an-image-in-email)

* [Bulletproof background images | Campaign Monitor](https://backgrounds.cm/)

* [How to address image blocking in email marketing | Campaign Monitor](https://www.campaignmonitor.com/resources/guides/image-blocking-in-email/)

#####Thu Jan 12 11:29:21 2017 CST  
**CME report link**  
[Log in to the AOA Physician Portal](https://physicianportal.osteopathic.org/TraCMEReport/DownloadTraCMEReport) to view your CME report
[https://physicianportal.osteopathic.org/TraCMEReport/DownloadTraCMEReport](https://physicianportal.osteopathic.org/TraCMEReport/DownloadTraCMEReport)
> Patrick,
>  
> Use this URL for "Run your CME Report" links in emails to diplomates:
>  
> https://physicianportal.osteopathic.org/TraCMEReport/DownloadTraCMEReport
>  
> There will be a password challenge if they are not already logged in to the PhysicianPortal (which uses a cookie to remember logins for 24 hours).
>  
> Bud
 

#####Fri Jan 20 15:19:38 2017 CST
* [The Ultimate Guide to Sending Email in Laravel | Scotch](https://scotch.io/tutorials/ultimate-guide-on-sending-email-in-laravel)
