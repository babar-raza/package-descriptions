# Aspose.Email for Java

[Aspose.Email for Java](https://products.aspose.com/email/java) is a complete set of Email Processing APIs to create, read and manipulate emails from within your applications. It makes it easier to work with many Outlook email message formats such as MSG, EML, EMLX and MHT files without the need of installing Microsoft Outlook. It also enables you to manage message storage files - Personal Storage Files (PST), Offline Storage Files (OST) along with message sending and receiving capabilities. You can also read and extract Outlook PST file that can be saved to disk in MSG format.

This repository contains [Examples](Examples) and [Plugins](Plugins) for [Aspose.Email for Java](https://products.aspose.com/email/java) to help you learn and write your applications.

<p align="center">
  <a title="Download complete Aspose.Email for Java source code" href="https://github.com/asposeemail/Aspose_Email_Java/archive/master.zip">
    <img src="http://i.imgur.com/hwNhrGZ.png" />
  </a>
</p>

## Email API Features

- Create and Set contents of MIME messages.
- Extract message contents from emails.
- Load and save [appointment in ICS format](https://docs.aspose.com/display/emailjava/Working+with+Appointments#WorkingwithAppointments-LoadandSaveAppointmentinICSFormat).
- Ability to connect to SMTP, POP3, IMAP, Exchange server.
- Works with Thunderbird, Zimbra and IBM Notes.
- [Many many more](https://docs.aspose.com/display/emailjava/Developer+Guide).

## Read & Write Email Formats

**Microsoft Outlook:** MSG, PST, OST, OFT
**Email:** EML, EMLX, MBOX
**Others:** ICS, VCF, HTML, MHTML

## Read Email Formats

**Mac Outlook:** OLM

## Supported Operating Systems

Aspose.Email for Java supports any operating system that runs the Java runtime including, but not limited:

- Windows
- Linux (Ubuntu, openSUSE, CentOS and others)
- Mac OS X

## Supported Java Versions

- `J2SE 6.0 (1.6)`
- `J2SE 7.0 (1.7)`
- `J2SE 8.0 (1.8)`
- or above.

## Get Started with Aspose.Email for Java

Aspose hosts all Java APIs at the [Aspose Repository](https://repository.aspose.com/webapp/#/artifacts/browse/tree/General/repo/com/aspose/aspose-email). You can easily use Aspose.BarCode for Java API directly in your Maven projects with simple configurations.

First you need to specify Aspose Repository configuration / location in your Maven `pom.xml` as below:

```xml
<repositories>
    <repository>
        <id>AsposeJavaAPI</id>
        <name>Aspose Java API</name>
        <url>https://repository.aspose.com/repo/</url>
    </repository>
</repositories>
```

Then define Aspose.Email for Java API dependency in your `pom.xml` as follows:

```xml
<dependencies>
    <dependency>
        <groupId>com.aspose</groupId>
        <artifactId>aspose-email</artifactId>
        <version>20.6</version>
        <classifier>jdk16</classifier>
    </dependency>
</dependencies>
```

Congratulations! You have successfully defined the Aspose.Email for Java Maven dependency in your Maven project.

## Perform IMAP Message Backup Operation using Java

```java
ImapClient imapClient = new ImapClient();
imapClient.setHost("<HOST>");
imapClient.setPort(993);
imapClient.setUsername("<USERNAME>");
imapClient.setPassword("<PASSWORD>");
imapClient.setSupportedEncryption(EncryptionProtocols.Tls);
imapClient.setSecurityOptions(SecurityOptions.SSLImplicit);

ImapMailboxInfo mailboxInfo = imapClient.getMailboxInfo();

ImapFolderInfo info = imapClient.getFolderInfo(mailboxInfo.getInbox().getName());
ImapFolderInfoCollection infos = new ImapFolderInfoCollection();
infos.add(info);

imapClient.backup(infos, dataDir + "\\ImapBackup.pst", BackupOptions.None);
```

[Product Page](https://products.aspose.com/email/java) | [Docs](https://docs.aspose.com/display/emailjava/Home) | [Demos](https://products.aspose.app/email/family) | [API Reference](https://docs.aspose.com/display/emailjava/Home) | [Examples](https://github.com/aspose-email/Aspose.Email-for-Java) | [Blog](https://blog.aspose.com/category/email/) | [Free Support](https://forum.aspose.com/c/email) | [Temporary License](https://purchase.aspose.com/temporary-license)
