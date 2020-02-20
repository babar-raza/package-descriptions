This .NET Email API assists you in processing the Microsoft Outlook®, Mac Outlook® & other email file formats from within .NET based applications. 

Aspose.Email for .NET allows you to work with MIME messages, appointments, Outlook items, Outlook storage files, various clients (SMTP, POP3, IMAP, Exchange EWS, Exchange WebDav), Gmail, Thunderbird, Zimbra, IBM Notes & AMP HTML emails. Email verification is also supported.

## Email API Features
- Open or save emails in Microsoft Outlook & other formats.
- Parse, read & save MS Outlook emails & PST files.
- Support for MIME messages.
- Send & receive emails via POP3, IMAP, Microsoft Exchange Server.
- Send emails in bulk while performing mail merge via various types of data sources.
- Send iCalendar compliant messages.
- Consume and produce recurrence patterns in the iCalendar (RFC 2445) format.
- Tools to verify email addresses, email syntax, email domain, mail server & MX records.
- Extract objects from various mail storage formats as well as create storage files from scratch.

## Read & Write Email Formats
**Microsoft Outlook:** MSG, PST, OST, OFT
**Email:** EML, EMLX, MBOX
**Others:** ICS, VCF, HTML, MHTML

## Read Email Formats
**Mac Outlook:** OLM

## Platform Independence
Aspose.Email for .NET is implemented using Managed C# and can be used with any .NET based languages including C#, VB.NET, J# and so on. Aspose.Email for .NET can be integrated with any kind of application on Windows, Linux, Mac OS X and Xamarin Platforms.

## Getting Started with Aspose.Email for .NET
Are you ready to give Aspose.Email for .NET a try? Simply execute `Install-Package Aspose.Email` from Package Manager Console in Visual Studio to fetch the NuGet package. If you already have Aspose.Email for .NET and want to upgrade the version, please execute `Update-Package Aspose.Email` to get the latest version.

## Create an Email Message & Save it in MSG Format using C#
You can execute below code snippet to see how Aspose.Email API performs in your environment or check the [GitHub Repository](https://github.com/aspose-email/Aspose.Email-for-.NET) for other common usage scenarios. 

```csharp
// create an instance of the MailMessage class
var message = new MailMessage();
// set from, to, subject and body properties
message.From = "sender@domain.com";
message.To = "receiver@domain.com";
message.Subject = "This is test message";
mamessageilMsg.Body = "This is test body";
// create an instance of the MapiMessage class and pass object of MailMessage as argument
var msg = MapiMessage.FromMailMessage(message);
// save file on disc
msg.Save(dir + "output.msg");
```
[Product Page](https://products.aspose.com/email/net) | [Documentation](https://docs.aspose.com/display/emailnet/Home) | [API Reference](https://apireference.aspose.com/net/email) | [Code Examples](https://github.com/aspose-email/Aspose.Email-for-.NET) | [Blog](https://blog.aspose.com/category/email/) | [Free Support](https://forum.aspose.com/c/email) | [Temporary License](https://purchase.aspose.com/temporary-license)