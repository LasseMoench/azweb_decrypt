<b>Paywall Hack / Issue</b></br>

The <b>"decryption" isn't working</b> any more since 25.04.2020.<br></s>

- no more JS 
- same cleartext, different ciphertext:

<b>clear:</b><br>
Die etwas älteren unter den Alemannia-Fans werden sich noch an die Jahreshauptversammlungen erinnern,<br>

<b>cipher:</b><br>
Die eatws teäenlr tuern end lmnaaeiAnn-saF nrwede hics noch na ied avmaeJslthrrnnepaumguseh rennrn,ie<br>
Die weats tenälre untre den na-anmeFanilsA dwnere sihc ocnh an die lhunJgaesvtpasaruenmhrme ,irennnre<br>
ieD wtesa rteälne trune dne emaanFlsani-An rndewe cish chno an ide ehnuhraautvsJegrmpansmel ennri,enr<br>

Looks like exploding or moving strings/chars but no simmilarities have been found yet.

__________________________________________________________________________________________________
__________________________________________________________________________________________________
__________________________________________________________________________________________________
__________________________________________________________________________________________________
__________________________________________________________________________________________________

<s><b>!!! Design Changes and Site Relaunch on 10.09.18 !!!</b><br>

The <b>decryptions isn't working</b> any more since 10.09.18 after a design relaunch.<br></s>
Paywall has changed in general.<br>

see https://www.aachener-zeitung.de/digital/neue-webseite-mit-neuem-design-bei-az-und-an_aid-32816053


<b>Update 10.09.18</b><br>
Bookmarklet and extension working again. Make sure to use version >=0.3
- Click on image to go to decrypted version of article if using direct links to paywall.

<s>
Usage change:

1. visit website (e.g. https://www.aachener-zeitung.de)
2. Use bookmarklet to prepare az-web links
3. No paywall.</s>

<b>Download Chrome Extension:</b><br>
https://chrome.google.com/webstore/detail/azan-decrypt/lmffohencfjcmgodmepkjajnfgbokcli?hl=de<br><br>

<s><b>mobile version</b><br>
Mobile version of website just hides the "real" content.
- Added bookmarklet for use in mobile browser.</s>

__________________________________________________________________________________________________
__________________________________________________________________________________________________
__________________________________________________________________________________________________
__________________________________________________________________________________________________
__________________________________________________________________________________________________
The following information are no longer valid because of design changes. (still here for the sake of completeness)


www.aachener-zeitung.de</br>
www.aachener-nachrichten.de</br>

<b>0. information</b></br>

The websites are offering a mixture of free and payed articles hidden by paywall. (http://www.aachener-zeitung.de/zva/pc/)
The websites use AESUtils and CryptoJS to hide articles.

The provider leaks <b>sensitive data like password, IV and salt which are used for encryption</b> and can be used to decrypt the articles.
<b>This issue does not leak any personal data of (registered) users.</b>

free article: http://www.aachener-zeitung.de/lokales/juelich/zukunft-von-haus-overbach-ist-langfristig-gesichert-1.1610013
hidden article: http://www.aachener-zeitung.de/lokales/juelich/feierabendmarkt-in-juelich-mit-bilderbuchstart-1.1622101

<b>1. timeline</b></br>

<ul>
<li>04.05.2017 20:53: informed "AZ - Lokales" via facebook pages about the possibility to read all hidden content (https://www.facebook.com/azlokalesaachen/)</li>
<li>04.05.2017 21:04: response with information that the issue will be forwarded</li>
<li>08/2017: release scripts & chrome extension</li>
</ul>

<b>2. PoC</b></br>

    var iv = "F27D5C9927726BCEFE7510B1BDD3D137";
    var salt = "3FF2EC019C627B945225DEBAD71A01B6985FE84C95A70EB132882F88C0A59A55";
    var keySize = 128;
    var iterationCount = 100;
    var passPhrase = "Zeitungsverlag Aachen GmbH";


<b>3. responsible disclosure</b></br>
responsible disclosure until 04.08.2017
</ul>
