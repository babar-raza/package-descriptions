# C++ Email Parsing Library

[Aspose.Email for C++](https://products.aspose.com/email/cpp) enables your C++ applications to work with various Outlook® objects including messages, tasks, contacts, calendar and journal items.

## Email File Processing Features

- [Create a new email message](https://docs.aspose.com/email/cpp/creating-and-setting-contents-of-emails/) with properties, such as, From, To, Subject, and Body.
- Save the email message in EML, MSG, and MHTML formats.
- Associate human-friendly names to email addresses, to improve accessibility.
- An email can have HTML as well as Text body.
- Set alternate text of email messages for the Email Readers that cannot display HTML content.
- [Fetch and display email header information](https://docs.aspose.com/email/cpp/extracting-message-contents-from-emails/) and email body on screen.
- Save and convert email messages to the [supported file formats](https://docs.aspose.com/email/cpp/supported-file-formats/).
- [Read email messages with TNEF attachments](https://docs.aspose.com/email/cpp/utility-features-mailmessage/) and modify the contents of the attachment.
- Check if the email message is regular or a bounced one.
- Add, remove, display and extract email attachments.
- [Embed objects in emails](https://docs.aspose.com/email/cpp/working-with-attachments-and-embedded-objects/), the size of attachment depends on the email server.
- Extract embedded objects from email messages.
- [Export email to MHT with customized time zone](https://docs.aspose.com/email/cpp/loading-and-saving-message/).
- [Create distribution list](https://docs.aspose.com/email/cpp/working-with-distribution-lists/) of multiple email contacts and save to storage in MSG format.
- Support to [work with MAPI properties](https://docs.aspose.com/email/cpp/working-with-mapi-properties/).
- Add [display or audio reminder](https://docs.aspose.com/email/cpp/working-with-outlook-calendar-items/) to email calendar items.

## New Features & Enhancements in Version 20.6

- Support to perform Advanced Query Search (AQS) queries in Exchange.
- Ability to work with Microsoft Graph API.

## Read & Write Email Formats

**Microsoft Outlook:** MSG, PST, OST, OFT
**Other:** EML, EMLX, MBOX, ICS, VCF, HTML, MHTML

## Read Only Email Formats

**Microsoft Outlook:** OLM

## Getting Started with Aspose.Email for C++

Are you ready to give Aspose.Email for C++ a try? Simply execute `Install-Package Aspose.Email.Cpp` from Package Manager Console in Visual Studio to fetch the NuGet package. If you already have Aspose.Email for C++ and want to upgrade the version, please execute `Update-Package Aspose.Email.Cpp` to get the latest version.

## Create New Message & Save in EML & MSG Formats

Try executing the below code snippet to see how Aspose.Email for C++ performs in your environment. You may also check the [GitHub Repository](https://github.com/aspose-email/Aspose.Email-for-C) for other common usage scenarios.

The following code sample shows how to create new email message and save it in EML & MSG formats using C++.

```c++
// create a new instance of MailMessage class
System::SharedPtr<MailMessage> message = System::MakeObject<MailMessage>();

// set subject of the message
message->set_Subject(u"New message created by Aspose.Email for .NET");

// set HTML body
message->set_IsBodyHtml(true);
message->set_HtmlBody(u"<b>This line is in bold.</b> <br/> <br/><font color=blue>This line is in blue color</font>");

// set sender information
message->set_From(u"from@domain.com");

// add TO recipients
message->get_To()->Add(u"to1@domain.com");
message->get_To()->Add(u"to2@domain.com");

// add CC recipients
message->get_CC()->Add(u"cc1@domain.com");
message->get_CC()->Add(u"cc2@domain.com");

// save message in EML, MSG and MHTML formats
message->Save(dir + u"output.eml", Aspose::Email::SaveOptions::get_DefaultEml());
message->Save(dir + u"output.msg", Aspose::Email::SaveOptions::get_DefaultMsgUnicode());
```

## Send Email via Exchange EWS Client using C++

```c++
// create instance of IEWSClient class by giving credentials
System::SharedPtr<IEWSClient> client = GetExchangeEWSClient(GetExchangeTestUser());

// create instance of type MailMessage
System::SharedPtr<MailMessage> msg = System::MakeObject<MailMessage>();
msg->set_From(MailAddress::to_MailAddress(u"sender@domain.com"));
msg->set_To(MailAddressCollection::to_MailAddressCollection(u"recipient@ domain.com "));
msg->set_Subject(u"Sending message from exchange server");
msg->set_HtmlBody(u"<h3>sending message from exchange server</h3>");

// send the message
client->Send(msg);
```

[Home](https://www.aspose.com/) | [Product Page](https://products.aspose.com/email/cpp) | [Docs](https://docs.aspose.com/email/cpp/) | [Demos](https://products.aspose.app/email/family) | [API Reference](https://apireference.aspose.com/email/cpp) | [Examples](https://github.com/aspose-email/Aspose.Email-for-C) | [Blog](https://blog.aspose.com/category/email/) | [Free Support](https://forum.aspose.com/c/email) |  [Temporary License](https://purchase.aspose.com/temporary-license)
