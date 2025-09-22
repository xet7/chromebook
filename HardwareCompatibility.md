# Hardware Compatibility

To run GalliumOS, your ChromeOS device needs firmware support for Legacy/BIOS or UEFI booting.
The table below includes OS and firmware support information for all 237 models of Chromebooks, Chromeboxes, and Chromebases. If a firmware update is required (or recommended) for your model, you can find full details at Firmware.
IMPORTANT: Device support is solely determined by the board name/Hardware ID -- manufacturer, model, etc are all irrelevant. The Hardware ID is listed at the bottom of the Recovery Mode and Developer Mode boot screens. Any devices not listed below are certainly too new to be supported.
If you find any errors or omissions, please let us know!

## GalliumOS Support by Model

Model|Hardware ID[1]|Year|Processor|Supported?|Firmware Update[2]|Known Issues
-----|--------------|----|---------|----------|------------------|------------
Acer AC700-1099 Wifi|ZGB|2011|Intel Pineview[4]|No[4]||
Acer AC700-1529 3G|ZGB|2011|Intel Pineview[4]|No[4]||
Acer C7 Chromebook|PARROT|2012|Intel Sandy Bridge[6]|Yes|Required[2]|-
Acer C7 Chromebook IVB|PARROT|2012|Intel Ivy Bridge[6]|Yes|Required[2]|-
Acer Chromebase|KITTY|2015|ARM[5]|No[5]||
Acer Chromebase 24|BUDDY|2016|Intel Broadwell[8]|Yes|Recommended[2]|-
Acer Chromebase CA24I2|KARMA|2019|Intel Kaby Lake[13]|Yes|Recommended[2]|internal audio, suspend/resume
Acer Chromebook 11 (C720, C720P)|PEPPY|2013|Intel Haswell[7]|Yes|Available|-
Acer Chromebook 11 (C732, C732T, C732L, C732LT)|ASTRONAUT|2018|Intel Apollo Lake[12]|Yes|Required[2]|internal audio, suspend/resume
Acer Chromebook 11 (C740)|PAINE|2014|Intel Broadwell[8]|Yes|Recommended[2]|-
Acer Chromebook 11 (C771, C771T)|LARS|2018|Intel Skylake[11]|Yes|Recommended[2]|internal audio?
Acer Chromebook 11 (CB3-111, C730, C730E)|GNAWTY|2014|Intel Bay Trail[9]|Yes|Required[2]|-
Acer Chromebook 11 (CB3-131, C735)|GNAWTY|2016|Intel Bay Trail[9]|Yes|Required[2]|-
Acer Chromebook 11 (CB311-8H, CB311-8HT)|SANTA|2018|Intel Apollo Lake[12]|Yes|Required[2]|internal audio, suspend/resume
Acer Chromebook 11 N7 (C731, C731T)|RELM|2017|Intel Braswell[10]|Yes|Required[2]|-
Acer Chromebook 13 (CB5-311, C810)|BIG|2014|ARM[5]|No[5]||
Acer Chromebook 13 (CB713-1W)|AKALI|2018|Intel Kaby Lake[13]|Yes|Recommended[2]|internal audio, suspend/resume
Acer Chromebook 14 (CB3-431)|EDGAR|2016|Intel Braswell[10]|Yes|Required[2]|-
Acer Chromebook 14 for Work (CP5-471)|LARS|2016|Intel Skylake[11]|Yes|Recommended[2]|internal audio?
Acer Chromebook 15 (CB3-531)|BANJO|2015|Intel Bay Trail[9]|Yes|Required[2]|-
Acer Chromebook 15 (CB3-532)|BANON|2016|Intel Braswell[10]|Yes|Required[2]|-
Acer Chromebook 15 (CB315-1H, CB315-1HT)|BLUE|2018|Intel Apollo Lake[12]|Yes|Required[2]|internal audio, suspend/resume
Acer Chromebook 15 (CB5-571, C910)|YUNA|2014|Intel Broadwell[8]|Yes|Recommended[2]|-
Acer Chromebook 15 (CB515-1H, CB515-1HT)|SAND|2017|Intel Apollo Lake[12]|Yes|Required[2]|internal audio, suspend/resume
Acer Chromebook 311 (C721)|KASUMI|2019|AMD[17]|||unsupported by GalliumOS 3.1 kernel
Acer Chromebook 311 (C733, C733U, C733T)|BOBBA|2019|Intel Gemini Lake[15]|||no functional legacy boot mode currently
Acer Chromebook 315 (CB315)|BLORB|2019|Intel Gemini Lake[15]|||no functional legacy boot mode currently
Acer Chromebook 315 (CB315-2H)|ALEENA|2019|AMD[17]|||unsupported by GalliumOS 3.1 kernel
Acer Chromebook 512 (C851, C851T)|SPARKY|2019|Intel Gemini Lake[15]|||no functional legacy boot mode currently
Acer Chromebook 514|EPAULETTE|2018|Intel Apollo Lake[12]|Yes|Required[2]|internal audio, suspend/resume
Acer Chromebook 714 (CB714-1W / CB714-1WT)|EKKO|2019|Intel Kaby Lake[13]|Yes|Recommended[2]|internal audio, suspend/resume
Acer Chromebook 715 (CB715-1W / CB715-1WT)|BARD|2019|Intel Kaby Lake[13]|Yes|Recommended[2]|internal audio, suspend/resume
Acer Chromebook R11 (CB5-132T, C738T)|CYAN|2015|Intel Braswell[10]|Yes|Required[2]|-
Acer Chromebook R13 (CB5-312T)|ELM|2016|ARM[5]|No[5]||
Acer Chromebook Spin 11 (CP311-H1, CP311-1HN)|LAVA|2018|Intel Apollo Lake[12]|Yes|Required[2]|internal audio, suspend/resume
Acer Chromebook Spin 11 (R751T / CP511)|REEF|2017|Intel Apollo Lake[12]|Yes|Required[2]|internal audio, suspend/resume
Acer Chromebook Spin 13 (CP713-1WN)|AKALI360|2018|Intel Kaby Lake[13]|Yes|Recommended[2]|internal audio, suspend/resume
Acer Chromebook Spin 15 (CP315)|BRUCE|2018|Intel Kaby Lake[13]|Yes|Recommended[2]|internal audio, suspend/resume
Acer Chromebook Spin 311 (CP311), Spin 511 (R752T, R752TN)|BOBBA360|2019|Intel Gemini Lake[15]|||no functional legacy boot mode currently
Acer Chromebook Spin 311 (R721T)|KASUMI360|2019|AMD[17]|||unsupported by GalliumOS 3.1 kernel
Acer Chromebook Spin 512 (R851TN)|SPARKY360|2019|Intel Gemini Lake[15]|||no functional legacy boot mode currently
Acer Chromebook Tab 10|SCARLET|2018|ARM[5]|No[5]||
Acer Chromebox|MCCLOUD|2014|Intel Haswell[7]|Yes|Available|-
Acer Chromebox CXI2 / CXV2|RIKKU|2015|Intel Broadwell[8]|Yes|Recommended[2]|-
Acer Chromebox CXI3|SION|2018|Intel Kaby Lake[13]|Yes|Recommended[2]|internal audio, suspend/resume
AOpen Chromebase Commercial|SUMO|2015|Intel Bay Trail[9]|Yes|Required[2]|-
AOpen Chromebase Mini|TIGER|2017|ARM[5]|No[5]||
AOpen Chromebox Commercial|NINJA|2015|Intel Bay Trail[9]|Yes|Required[2]|-
AOpen Chromebox Commercial 2|JAX|2019|Intel Kaby Lake[13]|Yes|Recommended[2]|internal audio, suspend/resume
AOpen Chromebox Mini|FIEVEL|2017|ARM[5]|No[5]||
ASI Chromebook|ENGUARDE|2016|Intel Bay Trail[9]|Yes|Required[2]|-
ASUS Chromebit CS10|MICKEY|2015|ARM[5]|No[5]||
ASUS Chromebook C200|SQUAWKS|2014|Intel Bay Trail[9]|Yes|Required[2]|-
ASUS Chromebook C201PA|SPEEDY|2015|ARM[5]|No[5]||
ASUS Chromebook C202SA|TERRA|2016|Intel Braswell[10]|Yes|Required[2]|-
ASUS Chromebook C204|APEL|2019|Intel Gemini Lake[15]|||no functional legacy boot mode currently
ASUS Chromebook C223|BABYMEGA|2018|Intel Apollo Lake[12]|Yes|Required[2]|internal audio, suspend/resume
ASUS Chromebook C300|QUAWKS|2014|Intel Bay Trail[9]|Yes|Required[2]|-
ASUS Chromebook C300SA / C301SA|TERRA|2016|Intel Braswell[10]|Yes|Required[2]|-
ASUS Chromebook C403|BABYMAKO|2019|Intel Apollo Lake[12]|Yes|Required[2]|internal audio, suspend/resume
ASUS Chromebook C423|RABBID|2019|Intel Apollo Lake[12]|Yes|Required[2]|internal audio, suspend/resume
ASUS Chromebook C425|LEONA|2019|Intel Amber Lake[14]|||unsupported by GalliumOS 3.1 kernel
ASUS Chromebook C523|BABYTIGER|2018|Intel Apollo Lake[12]|Yes|Required[2]|internal audio, suspend/resume
ASUS Chromebook Flip C100PA|MINNIE|2015|ARM[5]|No[5]||
ASUS Chromebook Flip C101PA|BOB|2017|ARM[5]|No[5]||
ASUS Chromebook Flip C213|REEF|2017|Intel Apollo Lake[12]|Yes|Required[2]|internal audio, suspend/resume
ASUS Chromebook Flip C214|AMPTON|2019|Intel Gemini Lake[15]|||no functional legacy boot mode currently
ASUS Chromebook Flip C302|CAVE|2016|Intel Skylake[11]|Yes|Recommended[2]|internal audio?
ASUS Chromebook Flip C433|SHYVANA|2019|Intel Amber Lake[14]|||unsupported by GalliumOS 3.1 kernel
ASUS Chromebook Flip C434|SHYVANA|2019|Intel Amber Lake[14]|||unsupported by GalliumOS 3.1 kernel
ASUS Chromebook Tablet CT100|DUMO|2019|ARM[5]|No[5]||
ASUS Chromebox (CN60)|PANTHER|2014|Intel Haswell[7]|Yes|Available|USB init on factory firmware only
ASUS Chromebox 2 (CN62)|GUADO|2015|Intel Broadwell[8]|Yes|Recommended[2]|-
ASUS Chromebox 3 (CN65)|TEEMO|2018|Intel Kaby Lake[13]|Yes|Recommended[2]|internal audio, suspend/resume
Bobicus Chromebook 11|EXPRESSO|2014|ARM[5]|No[5]||
Chromebook 314 (CB314)|DROID|2019|Intel Gemini Lake[15]|||no functional legacy boot mode currently
Crambo Chromebook|ENGUARDE|2016|Intel Bay Trail[9]|Yes|Required[2]|-
CTL Chromebook J41 / J41T|WHITETIP|2018|Intel Apollo Lake[12]|Yes|Required[2]|internal audio, suspend/resume
CTL chromebook NL7|BLACKTIP|2018|Intel Apollo Lake[12]|Yes|Required[2]|internal audio, suspend/resume
CTL Chromebook NL7 / NL7T-360 / NL7TW-360|BLACKTIP360|2018|Intel Apollo Lake[12]|Yes|Required[2]|internal audio, suspend/resume
CTL Chromebook NL7 LTE|BLACKTIPLTE|2019|Intel Apollo Lake[12]|Yes|Required[2]|internal audio, suspend/resume
CTL Chromebook Tablet Tx1 for Education|DRUWL|2019|ARM[5]|No[5]||
CTL Chromebox CBx1|WUKONG|2018|Intel Kaby Lake[13]|Yes|Recommended[2]|internal audio, suspend/resume
CTL J2 / J4 Chromebook|JERRY|2015|ARM[5]|No[5]||
CTL J5 Chromebook|WIZPIG|2016|Intel Braswell[10]|Yes|Required[2]|-
CTL N6 Education Chromebook|ENGUARDE|2014|Intel Bay Trail[9]|Yes|Required[2]|-
CTL NL61 Chromebook|RELM|2016|Intel Braswell[10]|Yes|Required[2]|-
Dell Chromebook 11|WOLF|2014|Intel Haswell[7]|Yes|Required[2]|-
Dell Chromebook 11 (3120)|CANDY|2015|Intel Bay Trail[9]|Yes|Required[2]|-
Dell Chromebook 11 (3180)|KEFKA|2017|Intel Braswell[10]|Yes|Required[2]|-
Dell Chromebook 11 (5190)|NASHER|2018|Intel Apollo Lake[12]|Yes|Required[2]|internal audio, suspend/resume
Dell Chromebook 11 2-in-1 (3189)|KEFKA|2017|Intel Braswell[10]|Yes|Required[2]|-
Dell Chromebook 11 2-in-1 (5190)|NASHER360|2018|Intel Apollo Lake[12]|Yes|Required[2]|internal audio, suspend/resume
Dell Chromebook 13 (3380)|ASUKA|2017|Intel Skylake[11]|Yes|Recommended[2]|internal audio?
Dell Chromebook 13 (7310)|LULU|2015|Intel Broadwell[8]|Yes|Recommended[2]|-
Dell Chromebook 3100|FLEEX|2019|Intel Gemini Lake[15]|||
Dell Chromebook 3100 2-in-1|GRABBITER|2019|Intel Gemini Lake[15]|||
Dell Chromebook 3400|ORBATRIX|2019|Intel Gemini Lake[15]|||
Dell Chromebox|TRICKY|2014|Intel Haswell[7]|Yes|Available|-
Dell Inspiron Chromebook 14 2-in-1 (7486)|VAYNE|2018|Intel Kaby Lake[13]|Yes|Recommended[2]|internal audio, suspend/resume
Dell Latitude 5300 2-in-1 Chromebook Enterprise|ARCADA|2019|Intel Whiskey Lake[16]|TBD[23]||
Dell Latitude 5400 Chromebook Enterprise|SARIEN|2019|Intel Whiskey Lake[16]|TBD[23]||
EduGear Chromebook K|JERRY|2015|ARM[5]|No[5]||
EduGear Chromebook M|MIGHTY|2015|ARM[5]|No[5]||
eduGear Chromebook R|ENGUARDE|2016|Intel Bay Trail[9]|Yes|Required[2]|-
Edugear CMT Chromebook|WIZPIG|2016|Intel Braswell[10]|Yes|Required[2]|-
Edxis Chromebook|EXPRESSO|2014|ARM[5]|No[5]||
Edxis Chromebook 11|BLACKTIP|2019|Intel Apollo Lake[12]|Yes|Required[2]|internal audio, suspend/resume
Edxis Chromebook X11|BLACKTIP360|2019|Intel Apollo Lake[12]|Yes|Required[2]|internal audio, suspend/resume
Edxis Education Chromebook (NL6)|ENGUARDE|2014|Intel Bay Trail[9]|Yes|Required[2]|-
Edxis Education Chromebook (NL6D)|RELM|2016|Intel Braswell[10]|Yes|Required[2]|-
Epik 11.6" Chromebook ELB1101|JERRY|2019|ARM[5]|No[5]||
Google Chromebook Pixel|LINK|2013|Intel Ivy Bridge[6]|Yes|Recommended[2]|HiDPI[19]
Google Chromebook Pixel (2015)|SAMUS|2015|Intel Broadwell[8]|Yes|Recommended[2]|HiDPI[19]
Google Cr-48|MARIO|2011|Intel Pineview[4]|No[4]||
Google Pixel Slate|NOCTURNE|2018|Intel Amber Lake[14]|||unsupported by GalliumOS 3.1 kernel
Google Pixelbook|EVE|2017|Intel Kaby Lake[13]|Yes|Required[2]|(multiple)
Google Pixelbook Go|ATLAS|2019|Intel Amber Lake[14]|||unsupported by GalliumOS 3.1 kernel
Haier Chromebook 11|JAQ|2015|ARM[5]|No[5]||
Haier Chromebook 11 C|WIZPIG|2017|Intel Braswell[10]|Yes|Required[2]|-
Haier Chromebook 11 G2|HELI|2015|Intel Bay Trail[9]|Yes|Required[2]|-
Haier Chromebook 11e|MIGHTY|2015|ARM[5]|No[5]||
HEXA Chromebook Pi|EXPRESSO|2014|ARM[5]|No[5]||
HiSense Chromebook 11|JERRY|2015|ARM[5]|No[5]||
HP Chromebook 11 G1|SPRING|2013|ARM[5]|No[5]||
HP Chromebook 11 G2|SKATE|2013|ARM[5]|No[5]||
HP Chromebook 11 G3/G4/G4 EE|KIP|2015|Intel Bay Trail[9]|Yes|Required[2]|-
HP Chromebook 11 G5|SETZER|2016|Intel Braswell[10]|Yes|Required[2]|-
HP Chromebook 11 G5 EE|RELM|2016|Intel Braswell[10]|Yes|Required[2]|-
HP Chromebook 11 G6 EE|SNAPPY|2018|Intel Apollo Lake[12]|Yes|Required[2]|internal audio, suspend/resume
HP Chromebook 11 G7 EE|MIMROCK|2019|Intel Gemini Lake[15]|||no functional legacy boot mode currently
HP Chromebook 11A G6 EE|BARLA|2019|AMD[17]|||unsupported by GalliumOS 3.1 kernel
HP Chromebook 13 G1|CHELL|2016|Intel Skylake[11]|Yes|Recommended[2]|HiDPI[19]
HP Chromebook 14/14A G5|CAREENA|2019|AMD[17]|||unsupported by GalliumOS 3.1 kernel
HP Chromebook 14 G3|BLAZE|2014|ARM[5]|No[5]||
HP Chromebook 14 G4|KIP|2015|Intel Bay Trail[9]|Yes|Required[2]|-
HP Chromebook 14 G5|SNAPPY|2018|Intel Apollo Lake[12]|Yes|Required[2]|internal audio, suspend/resume
HP Chromebook 14 q000-q099 / HP Chromebook 14-SMB Atheros|FALCO|2013|Intel Haswell[7]|Yes|Available|-
HP Chromebook 14 q000-q099 WP2 / HP Chromebook 14-SMB Intel Corp|FALCO|2013|Intel Haswell[7]|Yes|Available|-
HP Chromebook 15|SYNDRA|2019|Intel Kaby Lake[13]|Yes|Recommended[2]|internal audio, suspend/resume
HP Chromebook x2|SORAKA|2018|Intel Kaby Lake[13]|Yes|Recommended[2]|internal audio, suspend/resume
HP Chromebook x360 11 G1 EE|SNAPPY|2017|Intel Apollo Lake[12]|Yes|Required[2]|internal audio, suspend/resume
HP Chromebook x360 11 G2 EE|MEEP|2019|Intel Gemini Lake[15]|||no functional legacy boot mode currently
HP Chromebook x360 12b|BLOOG|2019|Intel Gemini Lake[15]|||
HP Chromebook x360 14|SONA|2018|Intel Kaby Lake[13]|Yes|Recommended[2]|internal audio, suspend/resume
HP Chromebook x360 14b|BLOOGUARD|2019|Intel Gemini Lake[15]|||
HP Chromebox G1|ZAKO|2014|Intel Haswell[7]|Yes|Available|USB init on factory firmware only
HP Chromebox G2|KENCH|2018|Intel Kaby Lake[13]|Yes|Recommended[2]|internal audio, suspend/resume
HP Pavilion Chromebook 14|BUTTERFLY|2013|Intel Sandy Bridge[6]|Yes|Required[2]|-
JP Sa Couto Chromebook|ENGUARDE|2017|Intel Bay Trail[9]|Yes|Required[2]|-
Lava Xolo Chromebook|JAQ|2015|ARM[5]|No[5]||
Lenovo 100e Chromebook|ROBO|2018|Intel Apollo Lake[12]|Yes|Required[2]|internal audio, suspend/resume
Lenovo 100e Chromebook 2nd Gen|PHASER|2019|Intel Gemini Lake[15]|||no functional legacy boot mode currently
Lenovo 100e Chromebook 2nd Gen MTK|HANA|2019|ARM[5]|No[5]||
Lenovo 100S Chromebook|ORCO|2015|Intel Bay Trail[9]|Yes|Required[2]|-
Lenovo 14e Chromebook, Lenovo Chromebook S345-14|LIARA|2019|AMD[17]|||unsupported by GalliumOS 3.1 kernel
Lenovo 300e Chromebook 2nd Gen MTK|HANA|2019|ARM[5]|No[5]||
Lenovo C340-11, 300e/500e Chromebook 2nd Gen|PHASER360|2019|Intel Gemini Lake[15]|||no functional legacy boot mode currently
Lenovo 300e/N23 Yoga/Flex 11 Chromebook|HANA|2017|ARM[5]|No[5]||
Lenovo 500e Chromebook|ROBO360|2018|Intel Apollo Lake[12]|Yes|Required[2]|internal audio, suspend/resume
Lenovo Yoga C630 Chromebook, Lenovo C340-15 Chromebook|PANTHEON|2018|Intel Kaby Lake[13]|Yes|Recommended[2]|internal audio, suspend/resume
Lenovo Chromebook S340-14 and Lenovo Chromebook S340-14 Touch|LASER14|2019|Intel Gemini Lake[15]|||no functional legacy boot mode currently|
Lenovo Ideapad C330 Chromebook|HANA|2018|ARM[5]|No[5]||
Lenovo Ideapad S330 Chromebook|HANA|2018|ARM[5]|No[5]||
Lenovo N20 Chromebook|CLAPPER|2014|Intel Bay Trail[9]|Yes|Required[2]|-
Lenovo N21 Chromebook|ENGUARDE|2015|Intel Bay Trail[9]|Yes|Required[2]|-
Lenovo N22 Chromebook|REKS|2016|Intel Braswell[10]|Yes|Required[2]|-
Lenovo N23 Chromebook|REKS|2016|Intel Braswell[10]|Yes|Required[2]|-
Lenovo N23 Chromebook (Touch)|REKS|2016|Intel Braswell[10]|Yes|Required[2]|-
Lenovo N42 Chromebook|REKS|2016|Intel Braswell[10]|Yes|Required[2]|-
Lenovo ThinkCentre Chromebox|TIDUS|2015|Intel Broadwell[8]|Yes|Recommended[2]|-
Lenovo ThinkPad 11e 3rd Gen Chromebook|ULTIMA|2016|Intel Braswell[10]|Yes|Required[2]|-
Lenovo ThinkPad 11e 4th Gen Chromebook|PYRO|2017|Intel Apollo Lake[12]|Yes|Required[2]|internal audio, suspend/resume
Lenovo ThinkPad 11e Chromebook|GLIMMER|2014|Intel Bay Trail[9]|Yes|Required[2]|-
Lenovo ThinkPad 13|SENTRY|2016|Intel Skylake[11]|Yes|Recommended[2]|-
Lenovo Thinkpad X131e Chromebook|STOUT|2013|Intel Ivy Bridge[6]|Yes|Required[2]|-
LG Chromebase (22CB25S)|MONROE|2016|Intel Haswell[7]|Yes|Available|-
LG Chromebase (22CV241)|MONROE|2014|Intel Haswell[7]|Yes|Available|-
Lumos Education Chromebook|MIGHTY|2016|ARM[5]|No[5]||
M&A Chromebook|ENGUARDE|2014|Intel Bay Trail[9]|Yes|Required[2]|-
Mecer Chromebook|JERRY|2017|ARM[5]|No[5]||
Mecer V2 Chromebook|RELM|2017|Intel Braswell[10]|Yes|Required[2]|-
Medion Chromebook Akoya S2013|JAQ|2016|ARM[5]|No[5]||
MEDION Chromebook S2015|MIGHTY|2016|ARM[5]|No[5]||
Multilaser Chromebook M11C|WIZPIG|2017|Intel Braswell[10]|Yes|Required[2]|-
N/A|RELM|2016|Intel Braswell[10]|Yes|Required[2]|-
NComputing Chromebook CX100|JERRY|2016|ARM[5]|No[5]||
Nexian Chromebook 11.6"|MIGHTY|2015|ARM[5]|No[5]||
Packard Bell Chromebook 314|DROID|2019|Intel Gemini Lake[15]|||
PCmerge Chromebook AL116|WHITETIP|2018|Intel Apollo Lake[12]|Yes|Required[2]|internal audio, suspend/resume
PCMerge Chromebook PCM-116E/PCM-116EB|MIGHTY|2016|ARM[5]|No[5]||
PCMerge Chromebook PCM-116T-432B|WIZPIG|2016|Intel Braswell[10]|Yes|Required[2]|-
Poin2 Chromebook 11|JERRY|2015|ARM[5]|No[5]||
Poin2 Chromebook 11C|HANA|2017|ARM[5]|No[5]||
Poin2 Chromebook 14|HANA|2017|ARM[5]|No[5]||
Positivo Chromebook C216B|RELM|2018|Intel Braswell[10]|Yes|Required[2]|-
Positivo Chromebook CH1190|JERRY|2017|ARM[5]|No[5]||
Positivo Chromebook N2110|BLACKTIP|2019|Intel Apollo Lake[12]|Yes|Required[2]|internal audio, suspend/resume
Positivo Chromebook N2112|BLACKTIP360|2019|Intel Apollo Lake[12]|Yes|Required[2]|internal audio, suspend/resume
Promethean Chromebox|WUKONG|2019|Intel Kaby Lake[13]|Yes|Recommended[2]|internal audio, suspend/resume
Prowise Chromebook Eduline|WHITETIP|2018|Intel Apollo Lake[12]|Yes|Required[2]|internal audio, suspend/resume
Prowise Chromebook Eduline / Prowise Chromebook Eduline 360|HANA|2019|ARM[5]|No[5]||
Prowise Chromebook Entryline|MIGHTY|2019|ARM[5]|No[5]||
Prowise Chromebook Proline|WIZPIG|2017|Intel Braswell[10]|Yes|Required[2]|-
RGS Education Chromebook|ENGUARDE|2016|Intel Bay Trail[9]|Yes|Required[2]|-
Samsung Chromebook - XE303|SNOW|2012|ARM[5]|No[5]||
Samsung Chromebook 2 11"|PIT|2014|ARM[5]|No[5]||
Samsung Chromebook 2 11" - XE500C12|WINKY|2014|Intel Bay Trail[9]|Yes|Required[2]|-
Samsung Chromebook 2 13"|PI|2014|ARM[5]|No[5]||
Samsung Chromebook 3|CELES|2016|Intel Braswell[10]|Yes|Required[2]|(multiple)[22]
Samsung Chromebook 4|BLUEBIRD|2019|Intel Gemini Lake[15]|||no functional legacy boot mode currently
Samsung Chromebook 4+|CASTA|2019|Intel Gemini Lake[15]|||no functional legacy boot mode currently
Samsung Chromebook Plus|KEVIN|2017|ARM[5]|No[5]||
Samsung Chromebook Plus (LTE)|NAUTILUS|2018|Intel Kaby Lake[13]|Yes|Recommended[2]|internal audio, suspend/resume
Samsung Chromebook Plus (V2)|NAUTILUS|2018|Intel Kaby Lake[13]|Yes|Recommended[2]|internal audio, suspend/resume
Samsung Chromebook Pro|CAROLINE|2017|Intel Skylake[11]|Yes|Recommended[2]|HiDPI[19]
Samsung Chromebook Series 5|ALEX|2011|Intel Pineview[4]|No[4]||
Samsung Chromebook Series 5 550|LUMPY|2012|Intel Sandy Bridge[6]|Yes|Required[2]|-
Samsung Chromebook Series 5 US 3G only|ALEX|2011|Intel Pineview[4]|No[4]||
Samsung Chromebox Series 3|STUMPY|2012|Intel Sandy Bridge[6]|Yes|Required[2]|-
Sector 5 E1 Rugged Chromebook|MIGHTY|2015|ARM[5]|No[5]||
Sector 5 E3 Chromebook|WHITETIP|2018|Intel Apollo Lake[12]|Yes|Required[2]|internal audio, suspend/resume
Senkatel C1101 Chromebook|ENGUARDE|2014|Intel Bay Trail[9]|Yes|Required[2]|-
Toshiba Chromebook|LEON|2014|Intel Haswell[7]|Yes|Available|-
Toshiba Chromebook 2|SWANKY|2014|Intel Bay Trail[9]|Yes|Required[2]|-
Toshiba Chromebook 2 (2015 Edition)|GANDOF|2015|Intel Broadwell[8]|Yes|Recommended[2]|-
True IDC Chromebook|ENGUARDE|2016|Intel Bay Trail[9]|Yes|Required[2]|-
True IDC Chromebook 11|JAQ|2015|ARM[5]|No[5]||
Videonet Chromebook|ENGUARDE|2016|Intel Bay Trail[9]|Yes|Required[2]|-
VideoNet Chromebook BL10|JERRY|2017|ARM[5]|No[5]||
ViewSonic NMP660 Chromebox|WUKONG|2018|Intel Kaby Lake[13]|Yes|Recommended[2]|internal audio, suspend/resume
Viglen Chromebook 11|MIGHTY|2015|ARM[5]|No[5]||
Viglen Chromebook 11C|WHITETIP|2018|Intel Apollo Lake[12]|Yes|Required[2]|internal audio, suspend/resume
Viglen Chromebook 360|WIZPIG|2016|Intel Braswell[10]|Yes|Required[2]|-

## Notes

1. **Hardware ID**: Each Chromebook/box/base model is given a hardware ID, which is used to differentiate it from other models, without interfering with branding and marketing names. Some manufacturers reuse model names for different hardware IDs (e.g. Samsung), and others sell the same hardware ID under multiple marketing names (e.g. HP). You can check your Hardware ID from the Developer Mode boot screen ("OS verification is OFF"), from the Terminal (sudo dmidecode -s system-product-name) or from inside ChromeOS by navigating to chrome://system, where it's called hardware_class. N.B.: Technically, the hardware ID is the full string, e.g. PEPPY C6A-V3C-A86, and the name alone, e.g. PEPPY is called the codename. The terms are used interchangeably, but in almost all cases, only the codename is important.
2. **Firmware Updates** are available for most models, and required for some. See Firmware.
3. **Dual-Booting** (GalliumOS and ChromeOS) is possible where the factory firmware supports legacy booting (SeaBIOS), or updated RW_LEGACY firmware is available. Dual-boot setups are installed using chrx. (Jump up↑)
4. **Pineview** models do not ship with compatible firmware. Custom firmware is available for MARIO (Google Cr-48). See Support/Pineview.
5. **ARM** models do not ship with compatible firmware, and custom firmware is not available at this time. See Support/ARM.
6. **Sandy/Ivy Bridge** models are supported. See Support/SandyIvy.
7. **Haswell** models are well-supported. See Support/Haswell.
8. **Broadwell** models are well-supported. See Support/Broadwell.
9. **Bay Trail** models are well-supported. See Support/BayTrail.
10. **Braswell** models are well-supported. See Support/Braswell.
11. **Skylake** models are mostly supported. See Support/Skylake and Skylake Platform Validation.
12. **Apollo Lake** models are partially supported, with known issues. See Support/ApolloLake and Apollo Lake Platform Validation.
13. **Kaby Lake** models are partially supported, with known issues. See Support/KabyLake and Kaby Lake Platform Validation.
14. **Amber Lake** models are new, and support is uncertain. See Support/AmberLake and Amber Lake Platform Validation.
15. **Gemini Lake** models are new, and support is uncertain. See Support/GeminiLake and Gemini Lake Platform Validation.
16. **Whiskey Lake** models are new, and support is uncertain. See Support/WhiskeyLake and Whiskey Lake Platform Validation.
17. **AMD** models are **partially** supported. See Support/AMD and AMD Platform Validation.
18. **Text Mode**: The factory firmware of Broadwell Chromebooks fails to display text-mode output, so messages printed to screen during the early boot process will be invisible. This can be functional, but very difficult to debug if problems arise. Updated FULL ROM firmware fixes this issue. See Firmware. (Jump up↑)
19. **HiDPI**: This model has a high definition display. GalliumOS (Xfce-4.12, Gtk2, xfwm4) will work at this display density, but some GUI elements will be uncomfortably small in default configuration. You can install the galliumos-hidpi package for some scaling improvements (chrx will install this package automatically).
20. **SAMUS** (Google Pixel, 2015) See Installing/Samus for some notes on audio and HiDPI config. (Jump up↑)
21. **PANTHER/ZAKO** (ASUS Chromebox, 2014 / HP Chromebox, 2014) have a broken factory legacy boot payload that fails to initialize the USB3 ports; custom firmware is the only resolution. See also Installing/Panther. (Jump up↑)
22. **CELES** (Samsung Chromebook 3) This model has been problematic for many users, but it has also been perfectly successful for others, We haven't been able to find the differences that separate these two groups, so we do not recommend CELES. If you already own a CELES, and would like to try GalliumOS, give it a shot! You might be one of the lucky ones. However, if you are looking to purchase a Chromebook with the intention of running GalliumOS, we strongly suggest choosing a different model.
23. **TBD** (to be determined) Please get in touch if you can help us fill in any of these details. Thanks!


Viglen Chromebook 360C|BLACKTIP360|2019|Intel Apollo Lake[12]|Yes|Required[2]|internal audio, suspend/resume
