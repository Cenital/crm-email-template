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

-----

# Correos

## Verificación de email por registro

```
Acá Javier Borelli, responsable de Comunidad y membresía de Cenital. Quiero darte la bienvenida e invitarte a que te suscribas para recibir nuestros contenidos en tu casilla de correo. Pero para eso primero necesitamos validar tu cuenta haciendo click en este enlace {{CONFIRMACION_URL}}.   

Una vez hecho eso ya podrás acceder a tu perfil en el sitio y elegir los newsletters que sean de tu interés. Si sos integrante de nuestro círculo de Mejores amigos, además podrás ver allí todos los beneficios que gestionamos en agradecimiento por tu apoyo.

Gracias nuevamente por tu interés en Cenital. Esperamos estar a la altura de tus expectativas.
Un saludo de parte de toda la redacción. 

Javier
```

## Bienvenida por registro

```
Hola, {{user_first_name}}.

Acá Javier Borelli, de nuevo. Te escribo para confirmarte que ya sos parte de nuestra comunidad de lectores de Cenital. Eso quiere decir que ya podés acceder a tu panel de usuario en el sitio para elegir los newsletters que gustes y/o modificar tus preferencias. Allí también podrás hacerte Mejor amigo de Cenital y descubrir los beneficios que hemos conseguido en agradecimiento al apoyo de nuestros lectores.

Como sabrás, todo nuestro periodismo se ofrece de manera gratuita con el fin de que cada vez más personas puedan acceder a información de calidad sobre los temas de interés público. De todas maneras invitamos a quienes puedan a que se sumen al círculo de Mejores amigos que sostiene Cenital. Hoy el ingreso más importante de nuestro medio lo aportan los lectores y eso nos permite trabajar sin condicionamientos. Si te interesa ser parte de este proyecto, podés sumarte acá o hacerlo desde la pestaña Mejores amigos de tu perfil de usuario.

Cualquier duda o consulta quedo a tu disposición.
Un abrazo
Javier
```

## Bienvenida por newsletter

```
Hola, {{user_first_name}}.

Acá Javier Borelli, responsable de Comunidad y membresía de Cenital. Te escribo porque vimos que te suscribiste a nuestros newsletters desde la web. A partir de ahora comenzarás a recibir en esta casilla los correos que elegiste de nuestros autores.

Además, desde tu panel de usuario en el sitio vas a poder modificar tus preferencias. Allí también podrás hacerte Mejor amigo de Cenital y descubrir los beneficios que hemos conseguido en agradecimiento al apoyo de nuestros lectores.. Eso te permitirá acceder a un panel de usuario en el sitio para modificar tus preferencias y comunicarte con nosotros. Allí también podrás hacerte Mejor amigo de Cenital y descubrir los beneficios que hemos conseguido en agradecimiento al apoyo de nuestros lectores.

Como sabrás, todo nuestro periodismo se ofrece de manera gratuita con el fin de que cada vez más personas puedan acceder a información de calidad sobre los temas de interés público. De todas maneras invitamos a quienes puedan a que se sumen al círculo de Mejores amigos que sostiene Cenital. Hoy el ingreso más importante de nuestro medio lo aportan los lectores y eso nos permite trabajar sin condicionamientos. Si te interesa ser parte de este proyecto, podés sumarte acá o hacerlo desde la pestaña Mejores amigos de tu perfil de usuario.

Cualquier duda o consulta quedo a tu disposición.
Un abrazo
Javier
```

## Bienvenida por membresía

```
Hola {{user_first_name}}, muchas gracias por sumarte a nuestro círculo de Mejores amigos y permitirnos seguir haciendo periodismo de calidad.

Cuando decidimos fundar Cenital, el Día del Periodista de 2019, lo hicimos pensando en que -a pesar de la polarización y los gritos- había lugar para ofrecerle a la audiencia contenido de calidad y con un abordaje profundo sin ser solemnes. Tiempo después, entendemos que ese diagnóstico fue correcto.

Cenital se sostiene hoy gracias a sus lectoras y lectores, cuya contribución voluntaria representa el ingreso más importante de nuestro medio. Eso nos pone orgullosos y nos da la tranquilidad necesaria para hacer el periodismo en que creemos. 

Ser parte de nuestros Mejores amigos no te da acceso a contenidos exclusivos porque creemos que la información de calidad debe ser accesible para todos, pero sí te hace parte de un grupo de pertenencia con el que tenemos comunicación permanente y a quienes ofrecemos en agradecimiento descuentos en libros y eventos culturales, así como también cursos de idiomas, posgrados, maestrías y otros talleres de formación. 

Podés conocer nuestra oferta de newsletters y elegir los que sean de tu preferencia desde tu panel de usuario en el sitio {{home_url}}. Allí también podrás ver los beneficios vigentes..

Ante cualquier duda siempre podrás contactarte con nosotros en la casilla info@cenital.com. 

Esperamos estar a la altura de tus expectativas.

Gracias otra vez, 

Iván

```

## Nueva membresía para usuario registrado

```
Hola {{user_first_name}}, muchas gracias por sumarte a nuestro círculo de Mejores amigos y permitirnos seguir haciendo periodismo de calidad. Me alegra especialmente saber que ya eras un lector de Cenital y que te convenciste de sumarte a nuestra comunidad.

Cuando decidimos fundar Cenital, el Día del Periodista de 2019, lo hicimos pensando en que -a pesar de la polarización y los gritos- había lugar para ofrecerle a la audiencia contenido de calidad y con un abordaje profundo sin ser solemnes. Tiempo después, entendemos que ese diagnóstico fue correcto.

Cenital se sostiene hoy gracias a sus lectoras y lectores, cuya contribución voluntaria representa el ingreso más importante de nuestro medio. Eso nos pone orgullosos y nos da la tranquilidad necesaria para hacer el periodismo en que creemos. 

Ser parte de nuestros Mejores amigos no te da acceso a contenidos exclusivos porque creemos que la información de calidad debe ser accesible para todos, pero sí te hace parte de un grupo de pertenencia con el que tenemos comunicación permanente y a quienes ofrecemos en agradecimiento descuentos en libros y eventos culturales, así como también cursos de idiomas, posgrados, maestrías y otros talleres de formación. 

En instantes vas a recibir un nuevo correo de Cenital invitándote a completar tu perfil como integrante de nuestra comunidad. Ahí te contaremos cómo seleccionar los newsletters que querés recibir en tu casilla de mail, cómo tramitar tu credencial de MA y acceder a los beneficios que hemos gestionado en reconocimiento de su apoyo.

Ante cualquier duda siempre podrás contactarte con nosotros en la casilla info@cenital.com. 

Esperamos estar a la altura de tus expectativas.

Gracias otra vez,

Iván

```

## Cambio de método de pago

```
Hola, {{user_first_name}}.

Quiero agradecerte por renovar tu apoyo a Cenital. El aporte de los lectores es nuestra fuente de ingresos más importante y nos permite seguir invirtiendo en periodismo. 

Si tenés alguna consulta recordá que siempre podés escribirnos a info@cenital.com. 

Un abrazo espectral,

Iván
```

## Cambio de monto de membresía


```
Hola, {{user_first_name}}.

Quiero agradecerte por renovar tu apoyo a Cenital. El aporte de los lectores es nuestra fuente de ingresos más importante y nos permite seguir invirtiendo en periodismo. 

Si tenés alguna consulta recordá que siempre podés escribirnos a info@cenital.com. 

Un abrazo espectral,

Iván
```

## Baja de membresía sin responser encuesta

```
Hola, {{user_first_name}}.

Mi nombre es Javier Borelli y trabajo como responsable de Comunidad y membresía en Cenital. Te escribo en respuesta al pedido de baja que hiciste. Primero que nada quería agradecerte por tu apoyo hasta acá. Para un proyecto como el nuestro el aporte de los lectores es fundamental ya que nos permite hacer periodismo sin condicionantes. 

La baja ya fue realizada y no se te realizará ningún nuevo descuento de nuestra parte. Pero en función de tu experiencia en el círculo de Mejores amigos de Cenital quiero ponerme a disposición para conversar y preguntarte si hay algo que podemos hacer para mejorar. 

Te mando un abrazo
Javier
```

## Baja por temas económicos

```
Hola, {{user_first_name}}.

Mi nombre es Javier Borelli y trabajo como responsable de Membresía y Comunidad en Cenital. Te escribo en respuesta al pedido de baja que hiciste. Primero que nada quería agradecerte por tu apoyo hasta acá. Para un proyecto como el nuestro el aporte de los lectores es fundamental ya que nos permite hacer periodismo sin condicionantes. 

La baja ya fue realizada y no se te realizará ningún nuevo descuento de nuestra parte. Pero en función de tu experiencia en el círculo de Mejores amigos de Cenital quiero ponerme a disposición para conversar y preguntarte si hay algo que podemos hacer para mejorar. En caso de que necesites bajar tu aporte mensual también podemos evaluarlo.

Para nosotros es muy importante la opinión de nuestras lectoras y lectores y nos gustaría que el vínculo con nuestra comunidad no se resienta. Decinos por favor si hay algo que podemos hacer para que reconsideres tu decisión o simplemente para que mejoremos la experiencia del resto de lxs lectores.

Te mando un abrazo
Javier

```

## Baja por temas no económicos


```
Hola, {{user_first_name}}.

Mi nombre es Javier Borelli y trabajo como responsable de Comunidad y membresía en Cenital. Te escribo en respuesta al pedido de baja que hiciste. Primero que nada quería agradecerte por tu apoyo hasta acá. Para un proyecto como el nuestro el aporte de los lectores es fundamental ya que nos permite hacer periodismo sin condicionantes. 

La baja ya fue realizada y no se te realizará ningún nuevo descuento de nuestra parte. Pero en función de tu experiencia en el círculo de Mejores amigos de Cenital quiero ponerme a disposición para conversar y preguntarte si hay algo que podemos hacer para mejorar. 

Te mando un abrazo
Javier
```

## Verificar email para unificar cuentas

```
Hola, {{user_first_name}}.

¿Cómo estás? Acá Javier Borelli nuevamente, el responsable de Comunidad y Membresía de Cenital. Te escribo porque notamos que todavía no recibís ninguno de nuestros newsletters en este correo y queríamos invitarte a probar otra forma de informarte.

Para conocer nuestra oferta y elegir aquellos contenidos que te resulten más interesantes podés ingresar a tu cuenta de usuario en nuestra web {{home_url}} y presionar en la pestaña “newsletters”. Ahí solo tenés que seleccionar las opciones de tu preferencia y presionar “guardar” para comenzar a recibir los mails en tu casilla de correo. Si alguno de ellos luego no te gusta, siempre podés darte de baja.

En caso de que estés recibiendo tus newsletters en otra dirección de correo, por favor avisanos asi unificamos y no te llenamos la casilla.

Cualquier duda o consulta quedo a tu disposición.
Un abrazo
Javier
```

## Magic Link

```
<br /><a href={{magic_link_url}}>Con este link podés ingresar al sitio.</a>
<h1>CHAU</h1>
```