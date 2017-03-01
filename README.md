 ( U | - | 2 | 3 | 2 )-( S | O | U | R | C | E )-( C | O | D | E )  
  \_/ \_/ \_/ \_/ \_/   \_/ \_/ \_/ \_/ \_/ \_/   \_/ \_/ \_/ \_/   

U-232 V5 -> High performance Bittorrent tracker
Italian Language Pack - U-232
Language Translator

    FBI

Support Forum

    https://forum-u-232.servebeer.com

Set Up Instructions:

Upload the files to your server to /lang/5

Then edit the following files of your U-232 V5 site:
/usercp.php

After :

<option value='4'" . ($CURUSER['language'] == '4' ? " selected='selected'" : "") . ">New</option>

Add :

<option value='5'" . ($CURUSER['language'] == '5' ? " selected='selected'" : "") . ">IT</option>;

/take_lang.php

After :

<option value='4'" . ($CURUSER['language'] == '4' ? " selected='selected'" : "") . ">FR</option>

Add :

<option value='5'" . ($CURUSER['language'] == '5' ? " selected='selected'" : "") . ">IT</option>";

/include/bittorrent.php

After :

case ($lang_charset == 4):
        return "UTF-8";

Add :

case ($lang_charset == 5):
        return "UTF-8";

and just check /include/config.php to verify the following is correct :

//==charset
$INSTALLER09['char_set'] = 'UTF-8'; //also to be used site wide in meta tags
if (ini_get('default_charset') != $INSTALLER09['char_set']) {
    ini_set('default_charset', $INSTALLER09['char_set']);

