# Free Responsive HTML Email Template

Sometimes all you want is a really simple responsive HTML email template with a clear call-to-action button. Here it is.

[See live preview](http://leemunroe.github.io/responsive-html-email-template/email.html).

<img src="https://user-images.githubusercontent.com/15963/29055956-8dcca38e-7bb4-11e7-8a86-7b056ebf673d.png" alt="Simple HTML Email" width="500">

## Inline your CSS before sending

Email is notorious for inconsistent CSS support. Therefore you should always inline your CSS and send a test to yourself before sending.

### Sending emails directly from your codebase or using a developer service?

For an API service (like Mailgun, SendGrid, Postmark) **you need to inline the CSS before sending**. See `email-inlined.html` for an example.

You can use this [Email CSS Inliner](https://htmlemail.io/inline/) and then [send a test email to yourself](https://postdrop.io) to verify it works as expected. 

* Copy all of email.html
* Paste the HTML as the source into the inliner
* Copy the HTML output and use this as the email template you send

### Sending emails using a marketing service like Mailchimp?

Use the template `email.html` as is. They'll put the CSS inline for you when you put together your campaign.

## Images in email

When inserting images remember to include the following attributes or risk them breaking in different clients:

* `src`
* `alt`
* `width`
* `height`
* `border`

Example:

`<img src="https://absolute-path-to-image.jpg" alt="Useful alt text" width="500" height="300" border="0" style="border:0; outline:none; text-decoration:none; display:block;">`

[More information here](https://www.smashingmagazine.com/2017/01/introduction-building-sending-html-email-for-web-developers/)

-----
# Tools

## Auttomatic Juice

Found on https://github.com/Automattic/juice

```
npm install juice -g
juice email.html email-inlined.html 
juice --web-resources-images false email-verification.html email-verification-inlined.html
```


# Cenital CRM

## Nuevo registro

```
<h1>HOLA</h1>
{{site_name}}, {{home_url}}, {{site_email}}, {{user_first_name}}, {{user_last_name}}, {{user_email}}
```

## Verificar dirección de correo electrónico

```
<br /><a href={{verification_link}}>VERIFICAR</a>
```

## Firma y magic link

```
<br /><a href={{magic_link_url}}>Con este link podés ingresar al sitio.</a>
<h1>CHAU</h1>
```