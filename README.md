# django-dian
Modulo para integrar la facturación electrónica del sistema de la DIAN con su proyecto Django.

# Documentación DIAN

## Presentación

### ¿Qué es la Factura Electrónica?​
Es, ante todo, una factura. Esto significa que tiene los mismos efectos legales que una factura en papel, se expide y recibe en formato electrónico. En otras palabras, es un documento que soporta transacciones de venta bienes y/o servicios y que operativamente tiene lugar a través de sistemas computacionales y/o soluciones informáticas permitiendo el cumplimiento de las características y condiciones en relación con la expedición, recibo, rechazo y conservación.

#### Características de la Factura Electrónica

- Utiliza el formato electrónico de generación XML estándar establecido por la DIAN.
- Lleva la numeración consecutiva autorizada por la DIAN.
- Cumple los requisitos del 617 ET y discrimina el impuesto al consumo cuando es el caso.
- Incluye la firma digital o electrónica para garantizar autenticidad e integridad y no repudio de la factura electrónica, de acuerdo con la política de firma adoptada por la DIAN.
- Incluye el Código Único de Factura Electrónica CUFE.

#### Modelo de Operación de la Factura Electrónica​

El modelo de facturación fue adoptado en el país a través del Decreto 2242 de 2015, compilado en el Decreto Único Reglamentario 1625 de 2016, y su objetivo principal es la masificación en el uso de la factura electrónica en Colombia, y, para ello, facilita la interoperabilidad entre quienes facturan de forma electrónica y quienes adquieren bienes que son facturados por ese medio, con los siguientes elementos:

- Un formato estándar de generación de la factura en XML que para su construcción utiliza el estándar UBL V2.0, el cual es de uso obligatorio para quienes facturan electrónicamente.
- Otros formatos estándar relacionados con el proceso de facturación son las notas débito y crédito a través de las cuales se realizan ajustes a las facturas electrónicas emitidas; estos formatos también tienen un formato estándar en XML y UBL V 2.0, e igualmente son obligatorios.
- La firma digital es elemento que permite garantizar la integridad, autenticidad y no repudio de la factura electrónica.
- Para aquellos adquirentes que no reciben el formato estándar electrónico de la factura se expedirá una representación gráfica que contiene elementos técnicos como un código QR.

La DIAN dispone de un servicio electrónico para pruebas de habilitación, recepción de ejemplares de factura electrónica, autorización de proveedores tecnológicos y un catálogo con la información de los participantes en factura electrónica. Este modelo permite que quienes deseen, pueden voluntariamente postularse para facturar electrónicamente. También le otorga facultades a la DIAN para seleccionar a contribuyentes y/o sectores para que facturen por este medio.

Esta modalidad de operación representa para las empresas una disminución del costo de facturación, respecto de los sistemas de facturación en papel y por computador.

#### Documentos que Pueden Ser Emitidos Electrónicamente

Los documentos que pueden ser emitidos electrónicamente, relacionados con la facturación son:

- Facturas​
- Notas Crédito
- Notas Débito
- Acuse de recibo
- Normatividad relacionada (Decreto 2242 de 2015, compilado Decreto 1625 de 2016)


### Beneficios y Ventajas

Los siguientes son algunos de beneficios que podrán tener quienes facturan electrónicamente:

- Eliminación de riesgo de pérdida de documentos físicos
- Eficiente gestión documental
- Cuidado y protección del medio ambiente
- Consulta en línea.
- Facilidad en las transacciones
- Mejora la trazabilidad y seguridad de operaciones
- Mejora la gestión de cobro
- Ahorro en costos de impresión, despacho, y almacenamiento.
- Procesos administrativos más rápidos y eficientes. Integración de procesos misionales, logísticos, contables, financieros y administrativos.
- Mejora la relación cliente/Proveedor.​​​

### Normatividad

En este espacio encontrará la normatividad relacionada con factura electrónica.

- Estatuto Tributario
- Artículo 511. Deber de entregar factura o documento equivalente.
- Artículo 615. del Estatuto Tributario-obligados a expedir y entregar factura o documento equivalente.
- Artículo 616-1. Factura o documento equivalente.
- Artículo 616-4. Proveedores autorizados, obligaciones e infracciones.
- Artículo 617. Requisitos de la factura para efectos tributarios.
- Artículo 618. La factura o documento equivalente, exigible por los adquirentes.
- Artículo 684-2. La DIAN puede prescribir sistemas técnicos de control a determ​inados contribuyentes o sectores.
- Artículo 684-4. Sanciones aplicables a los proveedores autorizados.
- Ley 962 de 2005. Artículo 26 - factura electrónica.
- Decreto Único Tributario 1625 de 2016. Artículo 1.6.1.4.1.1. hasta el 1.6.1.4.1.20.
- Resolución 000019 del 24 Febrero de 2016. Reglamentó el Decreto 2242 de 2015, que fue compilado en el Decreto 1625 de 2016.
- Resolución 0055 del 14 de julio de 2016. Reglamenta el servicio técnico de solicitud de numeración de facturas.
- Concepto 0907 del 16 de septiembre de 2016. Se pronuncia sobre el requisito de activos fijos que debe acreditar un solicitante de autorización como proveedor tecnológico.
- Resolución 000010 del 6 de febrero de 2018. 
- Resolución 000072 del 29 de diciembre de 2017. 
- Listado Obligados Resolución 000072 del 29 de diciembre de 2017. 
- Decreto 2242 de 2015
- Decreto 1625 de 2016 
- Resolución 0000062 del 30 de noviembre de 2018
- Resolución 000001 del 03012019. Mediante la cual se señalan las reglas y validaciones aplicables a la Factura Electrónica de que trata el artículo 616-1 del Estatuto Tributario
- Resolución 000002 del 03012019, Por la cual se selecciona un grupo de sujetos obligados a facturar electrónicamente y se establecen los requisitos que aplican en caso de impedimento, inconvenientes tecnológicos y/o de tipo comercial.
- Resolución 000013 del 15-02-2019, Por la cual se modifica el artículo 11 de la resolución 000019 del 24 de febrero de 2016, los artículos 6o y 8o de la Resolución 000055 del 14 de julio de 2016 y se derogan algunas disposiciones.


## Facture Electrónicamente

### Requisitos

Los interesados en participar en el Modelo de Factura Electrónica previsto por la DIAN deben pertenecer a uno de estos grupos:

- Las personas naturales o jurídicas seleccionadas por la DIAN para expedir factura electrónica o decidan acogerse de forma voluntaria.
- Personas que, no siendo obligadas a facturar, opten por expedir factura electrónica.
- En cualquiera de los casos, las personas naturales o jurídicas deberán surtir procedimiento habilitación previsto en el artículo 1.6.1.4.1.10 del Decreto 1625 de 2016.

### Procedimiento de Habilitación

- Es el procedimiento establecido por la DIAN, a través del cual los sujetos seleccionados por la DIAN para facturar electrónicamente o que optaron voluntariamente por ello, realizan entre otras, las pruebas tecnológicas tendientes a demostrar que el software que han dispuesto para facturar electrónicamente, cumple con las condiciones técnicas de expedición (generación -entrega) de la factura electrónica, recibo, rechazo
- Durante las pruebas de habilitación el interesado enviará facturas, notas débito y crédito electrónicas al servicio web desarrollado por la DIAN, con información ficticia, con el fin de comprobar que se ajustan a las condiciones técnicas fijadas por la DIAN
- El interesado en facturar electrónicamente puede hacer las pruebas con un software dispuesto directamente por él o seleccionando a un proveedor tecnológico previamente autorizado por la DIAN
- Guía de Usuario Externo Facturador Electrónico

### Autorización de Proveedor tecnológico

Es el evento, en el sistema de Facturación Electrónica, que les otorga a los participantes, denominados proveedores tecnológicos, autorización para ofrecer servicios inherentes a la factura electrónica a los obligados a facturar y a los adquirentes, que así lo decidan. Para poder obtener esta autorización un proveedor tecnológico deberá, entre otros requisitos, surtir el procedimiento de habilitación.

## Facturación Gratuita DIAN

### Términos y Condiciones
https://www.dian.gov.co/fizcalizacioncontrol/herramienconsulta/FacturaElectronica/Facturaci%C3%B3n_Gratuita_DIAN/Documents/Documento%20de%20T%C3%A9rminos.pdf

### Guía de uso
https://www.dian.gov.co/fizcalizacioncontrol/herramienconsulta/FacturaElectronica/Facturaci%C3%B3n_Gratuita_DIAN/Documents/Gu%C3%ADa_Factura_Electronica.pdf

### Video
https://www.youtube.com/watch?v=f6P0Jf5Troc&feature=youtu.be

### Servicio Web
​https://facturaciongratuita.dian.gov.co

La DIAN dispone de un servicio Web Gratuito con el fin de facilitar la expedición de la factura electrónica en condiciones establecidas en el Decreto 2242 de 2015 a microempresas y pequeñas empresas conforme con definiciones del artículo 2 de la Ley 905 2004 o las que establezca el Gobierno Nacional en desarrollo del artículo 43 de la Ley 1450 de 2011 o las disposiciones que modifiquen o sustituyan estas normas.

Para facilitar la interoperabilidad de la factura electrónica entre los participantes de la cadena de valor, esta solución permite la generación de los siguientes elementos:

- Un formato estándar de generación de la factura en XML, formato que para su construcción utiliza el estándar UBL V2, el cual es definido por la DIAN y es de uso obligatorio para quienes facturan electrónicamente. Otros formatos estándar relacionados con el proceso de facturación son las notas débito y crédito a través de las cuales se realizan ajustes a las facturas emitidas; estos formatos XML igualmente son obligatorios.
- La firma electrónica y/o digital es elemento que permite garantizar la integridad, autenticidad y no repudio de la factura electrónica.
- Disponer de una representación gráfica de la factura electrónica para aquellos adquirentes que no reciben el formato estándar electrónico, con elementos gráficos como los códigos QR.

Esta modalidad de operación representa para las empresas una disminución del costo de facturación y un aumento de su productividad al permitir él envió electrónico de los anteriores productos o documentos al receptor (Comprador), emisor (Vendedor) y a la Dian (Entidad de control).


## Información técnica

Aquí encontrará información técnica para definir y desarrollar las aplicaciones para factura electrónica desde su creación como documento XML, su firma digital y su respectivo envío a la DIAN. A continuación, se presenta la guía de usuario externo, mediante la cual se podrá identificar paso a paso como ingresar a la factura electrónica en Colombia: Guía de Usuario Externo Facturador Electrónico 

### Anexos Técnicos​

Esta documentación complementa la resolución 0019 de 2016 para definir los parámetros técnicos que deben cumplir las aplicaciones desarrolladas por los interesados en Facturar de forma Electrónica.

- Anexo Técnico 001. Formatos de los Documentos XML de Fac-e V2
- Anexo Técnico 002. Política de Firma de los Doc-eXML V2
- Anexo Técnico 003. Mecanismos Sistema Técnico de Control V2
- Anexo Técnico 004. Condiciones de Operatividad Tecnológica
- Anexo Técnico 005. Servicio de Recepcion de Facturas Electronicas V2
- Anexo Técnico 006. Servicio de Consulta Rangos Numeración Facturación V1
- Resolución 00001 del 05 de enero de 2018. Por la cual se modifican los Anexos Técnicos No. 001, 002, 003 y 005 de la Resolución 000019 del 24 de febrero 2016 y se adiciona el anexo No 006.​
- Ubl-Invoice Referencias Cruzadas. Tomo 1 - Tomo 2 - Tomo 3
- Versión 202 sección 2
- Transcribiendo Factura

#### Cambios Propuestos Anexos Técnicos​

- Anexo1 V204 tablas
- Anexo Técnico 002 Política de Firma de los Doc-eXML V202
- Anexo3_Mecanismos Sistema Técnico de Control V206 sección 2

### Documentos de Apoyo​

- DIAN - WebService Para Entregar Factura Electrónica
- DIAN - WebService Consulta Resultado de Transacciones de Factura Electrónica
- DIAN - WebService Consulta Resoluciones de Numeración de Facturación
- XSD DIAN UBL - XSD UBL2
- Ejemplos de apoyo         


# Instalación

pip install django-dian