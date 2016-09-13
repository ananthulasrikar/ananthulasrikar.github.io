---
id: 521
title: Steps for getting free Digital signature for your email from Comodo !
date: 2016-06-23T12:24:30+00:00
author: ananthulasrikar
layout: post
guid: http://srikar.io/?p=521
permalink: /steps-for-getting-free-digital-signature-for-your-email-from-comodo/
categories:
  - Uncategorized
---
  1. <div>
      <a href="https://www.comodo.com/home/email-security/free-email-certificate.php">https://www.comodo.com/home/email-security/free-email-certificate.php</a> ( Use Firefox Browser Only)
    </div>

  2. Fill the details as required.![](http://srikar.io/wp-content/uploads/2016/06/062316_0654_Stepsforget1.png)
  3. <div>
      You will receive email with instructions as below
    </div>
    
    ![](http://srikar.io/wp-content/uploads/2016/06/062316_0654_Stepsforget2.png)</li> 
    
      * Open the link <https://secure.comodo.com/products/!SecureEmailCertificate_Collec2> and enter password as per instructions in email
      * Firefox browser downloads and install certificate and stores in the browser.
      * Export this certificate to your Desktop (place that is feasible for you) by navigating to Preferences Click Alt + T + O (OR) Type &#8220;about:preferences&#8221; in address bar.
      * <div>
          Navigate to Advance -> Certificates -> View Certificates -> select COMODO CA Limited (Appropriate one) -> Backup -> Enter password (which you need in step 8) -> Give file name (say gmail-digital.p12) ->Save
        </div>
        
        ![](http://srikar.io/wp-content/uploads/2016/06/062316_0654_Stepsforget3.png)</li> 
        
          * Double click the exported file -> Current User/Local Machine -> Next ->Next -> Enter Password. -> Certificate will be imported to local user storage. Open Run (Ctrl +R) ->certmgr.msc ->Personal -> Certificates -> You will find a certificate with the email (Eg: xxxx@xxx.com ) -> Right click -> Properties ->Give a Friendly name (so that it can be used while configuring certificate in outlook)
          * Follow the steps for outlook 2016 in <https://kb.wisc.edu/office365/page.php?id=52004>
          * Now you will be able to send Digital signed emails from your outlook 🙂 You have a badge like this![](http://srikar.io/wp-content/uploads/2016/06/062316_0654_Stepsforget4.png)</ol> 
        
        Let me know your inputs/ comments. Congrats for learning how to send email using Digital signatures 😀