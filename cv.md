# Vasilisa Sitnikova #

## Contact information:
**Phone:** +7(931)290-14-03  
**email:** sitnikova.va@mail.ru

## About myself:
I'm very selfdeterminate and a fast learning. I want to become a great developer and to create sometghing great. I had an expirience in java developing, then had a time break for my family, created kid's educational center, but always wanted to return in IT.

## Languages:
*Java
*JavaScript
*HTML, CSS
*Python
*IntelliJ IDEA
*Maven
*Git, GitHub
*Scrum, Canban
*Adobe Photoshop, Illustrator

## Code example:

```java
public void sendMail() {
        Properties props = System.getProperties();
        props.put("mail.smtp.starttls.enable", "true");
        props.put("mail.smtp.host", hostMail);
        props.put("mail.smtp.auth", "true");
        props.put("mail.smtp.user", username);
        props.put("mail.smtp.password", password);
        props.put("mail.debug", "1");
        Session session_m = Session.getDefaultInstance(props, null);

        try {
            MimeMessage message = new MimeMessage(session_m);
            message.setFrom(new InternetAddress(fromEmail, fromFullname));
            message.addRecipient(Message.RecipientType.TO, new InternetAddress(emailUser, fullnameUser));

            message.setSubject(subject);


            message.setText(body);
            message.setHeader("Content-Type", "text/plain;charset=windows-1251");

            SMTPTransport t = (SMTPTransport) session_m.getTransport("smtp");
            t.connect(hostMail, username, password);
            t.sendMessage(message, message.getAllRecipients());
        } catch (Exception e) {
            System.err.println(e);
        }
    }
```