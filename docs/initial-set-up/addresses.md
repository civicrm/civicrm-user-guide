# Address Settings

## Mailing Labels

**Individual Name Format** - The order and the specific fields for Individual Contact names **when they are included in mailing labels**.

Default is: `{individual_prefix}{ }{first_name}{ }{middle_name}{ }{last_name}`

**Mailing Label Format** - Use [tokens](/common-workflows/tokens-and-mail-merge.md) to show how you want addresses formatted for mailing labels. **You must include the {contact_name} token if you want to include the contact name in your labels.**

Use "state_province" if you prefer to use the state/province abbreviation or "state_province_name" if you prefer to use the full state/province name.

The standard format is:

```
{contact_name}
{street_address}
{supplemental_address_1}
{supplemental_address_2}
{city}{, }{state_province}{ }{postal_code}
{country}
```

Address Formatting

**Address Formatting** - Use tokens to show how you want addresses formatted for display.

Use "state_province" if you prefer to use the state/province abbreviation or "state_province_name" if you prefer to use the full state/province name.

The standard format is:

```
{street_address}
{supplemental_address_1}
{supplemental_address_2}
{city}{, }{state_province}{ }{postal_code}
{country}
```

**Maximum Locations** - Type in the maximum number of different locations/addresses that you want to allow for contacts.

**Include County?** - Indicate if you want a County field to be included in contact address input forms.

## Address Standardization

!!! note
    CiviCRM includes an optional plugin for interfacing the the United States Postal Services (USPS) Address Standardization web service. You must register to use the USPS service at [https://www.usps.com/business/webtools.htm](https://www.usps.com/business/webtools.htm). If you are approved, they will provide you with a User ID and the URL for the service.


**Provider - Address Standardization Provider. Currently, only 'USPS' is supported.**

**User ID** - USPS-provided User ID.
**Web Service URL** - USPS-provided web service URL.

Click **Save** to save your action or **Cancel** to cancel it.

!!! note
    There is a [how-to guide on integrating with USPS for address standardization](https://wiki.civicrm.org/confluence/display/CRMDOC/Configuring+Address+Standardization+to+work+with+USPS).
    
## Configuring Address Standardization to work with USPS

!!! note
    Address Standardization is currently only available for The United States Postal Service API.

### Register for USPS Web Tools ID

Go to: [https://secure.shippingapis.com/registration/](https://secure.shippingapis.com/registration/)

* **Will use:** => Exclusively on my website

Upon submission you will receive a confirmation email. You will need the Web Tools ID for the next step.

### Request access to the Address Information API

Go to: [https://www.usps.com/business/webtools-address-information.htm](https://www.usps.com/business/webtools-address-information.htm)

* Enter the URL of your CiviCRM website - The address of the site of the owner of the
 (may be one Web Tools ID per company/individual that owns the website, and a unique USPS provided Server User ID per actual website, e.g. domain name [needs confirmed])

Select from the following:

* U.S. Postal Service® package shipments
* U.S. Postal Service letters
* Do not select other choices, as these uses are not provided or permitted for this API.

If there are questions, The USPS Internet Customer Care Center (ICCC) will contact you via the listed email address, seeking more information.

> Dear USPS Customer,
>
> Address Information APIs are accessible with special permission. The APIs can only be used in conjunction with USPS SHIPPING SERVICES ONLY.
>
> We must first understand how you'll be using the API. We need a commitment that the API will be used on a transactional basis (not batch processing or cleansing of a database, but as a customer enters the information into a form on a website). Also, you must state that you will use the output from this API solely in association with USPS SHIPPING SERVICES ONLY.
> 
> Please provide a detailed description how you plan to use the APIs, include the URL of the site (development or production). We will review the material received to see if you meet our requirements.

The USPS needs to read two things, and read them very clearly.

1. You are using the USPS provided information only to ship letters or packages via United States Postal Service.
1. The user's address will be updated only when users modify their postal information. (e.g. transactional basis)

### Sending test requests using your Web Tools ID

Before USPS can grant you access to their production servers, they need to receive some requests from you that include the Web Tools ID they gave you.

You may be able to skip this step by calling them or emailing them and saying that you are using a fully developed open-source project (see below), but it will be easier for them to approve you if you show that you are capable of making requests to their servers correctly.

In CiviCRM, you should go to Administer -> Localization > Address Settings [Address Standardization]:

Select USPS as the standardization provider, enter your Web Tools ID, and enter the server name below:

```
http://testing.shippingapis.com/shippingapitest.dll
```

Now you can send a few test requests. Create a contact and input the following two addresses:

* 6406 Ivy Lane, Greenbelt, MD
* 8 Wildwood Drive, Old Lyme, CT 06371

 After saving, CiviCRM should display the complete, standardized addresses, or should display an error warning you that the address did not validate with USPS. Either way, you have successfully completed your tests by sending some requests to the API. If you don't think it worked, go back and check your settings, and if the address standardization provider dropdown does not show, USPS, see [CRM-11337](http://issues.civicrm.org/jira/browse/CRM-11337).

!!! note

    Not all addresses work with this service. Only preset addresses addresses validate. For other addresses, USPS will return an API error (This information is not contained in the testing API), but CiviCRM doesn't know how to interpret that and will just say the address could not be validated with USPS. For more information about this API, see [https://www.usps.com/webtools/_pdf/Address-Information-v3-1b.pdf](https://www.usps.com/webtools/_pdf/Address-Information-v3-1b.pdf)


!!! note

    It is important that you do not stop at this step. The test server is not intended for long term use and does not work for all addresses. Your access rights could be halted if you use the test server for too long.


### Request access to the Production Server & Address Standardization

Once you have been approved to use the Address Standardization API, you should ask for access to the production server. Email them or call them as indicated in the email indicated by them.

Inform them that you are using CiviCRM and it is a fully developed Open Source project, so you are not developing anything.

**At this stage the ICCC may ask you more specific questions via email, or you may need to call them to get over this last hurdle**. (contact info below)

They may want to see how your production website uses the service. Including a URL to the forms your users enter their postal address postal address should speed things up. It might even help to make a temp account for them, if the forms are only available to registered users.

### Setup CiviCRM to access the USPS production server

Successful completion of task three should reward you with an email such as this:

Dear USPS Customer,
 Thank you for contacting us. Congratulations on completing your testing using the U.S. Postal Service's Internet Shipping Application Program Interfaces (APIs).
 Your profile has been updated to allow you access to the Production Server.
  1. The Production Server URL is: [http://production.shippingapis.com](http://production.shippingapis.com/). For APIs calling the secure server, the URL is [https://secure.shippingapis.com](https://secure.shippingapis.com/).
  1. There is a line of code that refers to "shippingapitest.dll". You'll need to remove the word "test".
 If you are using third party software and need assistance, please contact the vendor of the software. They should be able to assist you in obtaining live information using our APIs.

In CiviCRM, you should go to Administer -> Localization > Address Settings [Address Standardization], and enter the following server:

```
http://production.shippingapis.com/shippingapi.dll
```

#### Sample Production Setup

Input under Administer->Localization->Address settings.

![](https://wiki.civicrm.org/confluence/download/attachments/22904945/CiviCRMAddressStandardizationSample.png?version=1&modificationDate=1252275467000&api=v2)

### The USPS Internet Customer Care Center (ICCC)

staffed from 7:00AM to 11:00PM Eastern Time
**E-mail:** [icustomercare@usps.com](mailto:icustomercare@usps.com)
**Telephone:** 1-800-344-7779

### USPS Terms of Service violations that can terminate your service

> This unique User ID cannot be shared with others outside your organization, nor is it to be packaged and distributed or sold to other individuals, businesses or e-commerce web site entities.> If the U.S. Postal Service discovers use of the same User ID from more than one web site, all users will be subject to loss of access to the USPS production server

!!! warning
    CiviCRM invokes the address standardization API even when doing contact 
    imports. Be careful to either turn off the standardization feature when 
    doing imports, or to limit yourself to imports containing only a addresses

What some may be viewing as technical problems may just be the result of being caught violating the terms of service.

!!! note

    If you are developing a website for a client, you need a Web Tools ID for each client. You may even have them fill out the Web Tools forms. For email contact, a unique email address that the client owns is a good idea. You can forward the address to your email while in development, or send to both yourself and the client. This will allow you to remain in compliance with the agreement while also directly receiving the communications.


### Other Related discussions or Internet Resources

[USPS Address Standardization Returns BLANKS](http://forum.civicrm.org/index.php?topic=2745.0 "CiviCRM Forum Post")

[Is anyone using the United States Postal Services (USPS) Address Standardization web service plugin?](http://civicrm.org/node/627 "CiviCRM node")
[OSDir.com > USPS Address Standardization web service: msg](http://osdir.com/ml/crm.civicrm.devel/2007-01/msg00284.html "OSDir.com Discussion with Lobo")

[https://www.usps.com/webtools/_pdf/Address-Information-v3-1b.pdf](https://www.usps.com/webtools/_pdf/Address-Information-v3-1b.pdf)
