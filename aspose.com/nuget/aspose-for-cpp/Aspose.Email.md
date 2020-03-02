# C++ Email Parsing Library
[Aspose.Email for C++](https://products.aspose.com/email/cpp) enables your C++ applications to work with various Outlook® objects including messages, tasks, contacts, calendar and journal items. You may also convert between different email file formats as well as create & extract message storage files. Aspose.Email for C++ is best suited for mail management features such as content editing, manipulation of recipients, extraction & manipulation of MAPI properties and attachments as well as for the advanced features such as message storage files management including PST & OST. 

## Email File Processing Features
- Create plain & HTML emails from scratch using the API.
- Load variety of formats for editing or just inspection.
- Inter-convert email file formats with just a few lines of code.
- Supply alternative message bodies.
- Manage email headers, embedded objects & attachments.
- Save messages as draft.
- Use Mail Merge feature to create emails from various data sources.

## Storage File Processing Features
- Create PST & OST files from scratch using the API.
- Manage [messages](https://docs.aspose.com/display/emailcpp/Working+with+Messages+in+a+PST+File), [contacts](https://docs.aspose.com/display/emailcpp/Working+with+Contacts+in+PST+File), [calendar items](https://docs.aspose.com/display/emailcpp/Working+with+Calendar+Items+in+PST+File), [tasks](https://docs.aspose.com/display/emailcpp/Working+with+MapiTask+in+PST), [notes](https://docs.aspose.com/display/emailcpp/Working+with+MapiNote+in+PST) and [journals](https://docs.aspose.com/display/emailcpp/Working+with+MapiJournal+in+PST) in PST.
- Split & merge PST files.

## Calendar & Appointment Managment Features
- Produce & consume iCalendar (RFC 2445) recurrence patterns.
- Easily and reliably calculate occurrence dates and times for even the most complex recurrence patterns.
- Create recurrence patterns programmatically via an intuitive object model.
- Use yearly, monthly, weekly, daily, hourly, minutely and secondly recurrence patterns.
- Represent recurrence patterns in your windows, web or a mobile application.
- Create appointments & export appointment to ICS format.
- Format appointment text and read appointment information.

## Read & Write Email & Storage Files
**Microsoft Outlook:** MSG, PST, OST
**Other:** EML, EMLX

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

[Product Page](https://products.aspose.com/email/cpp) | [Documentation](https://docs.aspose.com/display/emailcpp/Home) | [API Reference](https://apireference.aspose.com/cpp/email) | [Code Examples](https://github.com/aspose-email/Aspose.Email-for-C) | [Blog](https://blog.aspose.com/category/email/) | [Free Support](https://forum.aspose.com/c/email) |  [Temporary License](https://purchase.aspose.com/temporary-license)