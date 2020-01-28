A standalone on-premise C++ library to assist in creating, managing & converting Microsoft Outlook® & other email files from within C++ apps.

Aspose.Email for C++ enables your C++ applications to work with various Outlook objects including messages, attachments, tasks, contacts, calendar and journal items. You may also convert between different email file formats as well as create & extract message storage files.

## C++ Email API Features
- Open or save emails in popular message formats.
- Parse, read & save MS Outlook messages.
- Embed objects in email messages.
- Use Mail Merge feature to create emails from various data sources.
- Verify email addresses, domain, MX records and so on.
- Create and process PST & OST files.


## Read & Write Email & Storage Files
**Microsoft Outlook:** MSG, PST, OST
**Other:** EML, EMLX

## Getting Started with Aspose.Email for C++
Are you ready to give Aspose.Email for C++ a try? Simply execute `Install-Package Aspose.Email.Cpp` from Package Manager Console in Visual Studio to fetch the NuGet package. If you already have Aspose.Email for C++ and want to upgrade the version, please execute `Update-Package Aspose.Email.Cpp` to get the latest version.

Try executing the below code snippet to see how Aspose.Email for C++ performs in your environment. You may also check the [GitHub Repository](https://github.com/aspose-email/Aspose.Email-for-C) for other common usage scenarios. The following code sample shows 
### Create New Message & Save in EML & MSG Formats
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
message->Save(dataDir + u"output.eml", Aspose::Email::SaveOptions::get_DefaultEml());
message->Save(dataDir + u"output.msg", Aspose::Email::SaveOptions::get_DefaultMsgUnicode());
```

[Product Page](https://products.aspose.com/email/cpp) | [Documentation](https://docs.aspose.com/display/emailcpp/Home) | [API Reference](https://apireference.aspose.com/cpp/email) | [Code Examples](https://github.com/aspose-email/Aspose.Email-for-C) | [Blog](https://blog.aspose.com/category/email/) | [Free Support](https://forum.aspose.com/c/email) |  [Temporary License](https://purchase.aspose.com/temporary-license)