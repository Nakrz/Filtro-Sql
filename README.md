# FILTRO MySQL  

Angeli Nicol Corredor Rodriguez, Andres David Paniagua Villada

Obtener los nombres de todos los actores y las películas en las
que han actuado.

```sql
SELECT CONCAT(a.nombre,' ',a.apellidos) AS nombre_Completo, p.titulo
    -> FROM actor a 
    -> JOIN pelicula_actor pa ON a.id_actor=pa.id_actor
    -> JOIN pelicula p ON p.id_pelicula=pa.id_pelicula
    -> ;
+----------------------+-----------------------------+
| nombre_Completo      | titulo                      |
+----------------------+-----------------------------+
| PENELOPE GUINESS     | ACADEMY DINOSAUR            |
| PENELOPE GUINESS     | ANACONDA CONFESSIONS        |
| PENELOPE GUINESS     | ANGELS LIFE                 |
| PENELOPE GUINESS     | BULWORTH COMMANDMENTS       |
| PENELOPE GUINESS     | CHEAPER CLYDE               |
| PENELOPE GUINESS     | COLOR PHILADELPHIA          |
| PENELOPE GUINESS     | ELEPHANT TROJAN             |
| PENELOPE GUINESS     | GLEAMING JAWBREAKER         |
| PENELOPE GUINESS     | HUMAN GRAFFITI              |
| PENELOPE GUINESS     | KING EVOLUTION              |
| PENELOPE GUINESS     | LADY STAGE                  |
```

Listar todos los clientes y los almacenes donde están
registrados.

```sql
SELECT CONCAT(c.nombre,' ',c.apellidos) AS nombre_Completo, a.id_almacen
    -> FROM cliente c JOIN almacen a ON c.id_almacen=a.id_almacen;
+-----------------------+------------+
| nombre_Completo       | id_almacen |
+-----------------------+------------+
| BARBARA JONES         |          2 |
| JENNIFER DAVIS        |          2 |
| SUSAN WILSON          |          2 |
| MARGARET MOORE        |          2 |
| LISA ANDERSON         |          2 |
| KAREN JACKSON         |          2 |
| BETTY WHITE           |          2 |
| SANDRA MARTIN         |          2 |
| CAROL GARCIA          |          2 |
| SHARON ROBINSON       |          2 |
| SARAH LEWIS           |          2 |
```

Encontrar todas las películas y sus respectivas categorías.

```sql
 SELECT p.titulo, c.nombre 
 FROM pelicula p
 JOIN pelicula_categoria pc ON p.id_pelicula = pc.id_pelicula
 JOIN categoria c ON pc.id_categoria = c.id_categoria;xxxxxxxxxx SELECT p.    SELECT p.titulo AS pelicula_titulo, c.nombre AS categoria_nombre FROM pelicula p  JOIN pelicula_categoria pc ON p.id_pelicula = pc.id_pelicula JOIN categoria c ON   pc.id_categoria = c.id_categoria;FROM pelicula as p
 
 +-----------------------------+------------------+
| titulo                       |           nombre |
+-----------------------------+------------------+
| AMADEUS HOLY                | Action           |
| AMERICAN CIRCUS             | Action           |
| ANTITRUST TOMATOES          | Action           |
| ARK RIDGEMONT               | Action           |
| BAREFOOT MANCHURIAN         | Action           |
| BERETS AGENT                | Action           |
| BRIDE INTRIGUE              | Action           |
| BULL SHAWSHANK              | Action           |
| CADDYSHACK JEDI             | Action           |
| CAMPUS REMEMBER             | Action           |
| CASUALTIES ENCINO           | Action           |
| CELEBRITY HORN              | Action           |
| CLUELESS BUCKET             | Action           |
| CROW GREASE                 | Action           |
| DANCES NONE                 | Action           |
| DARKO DORADO                | Action           |
| DARN FORRESTER              | Action           |
| DEVIL DESIRE                | Action           |
| DRAGON SQUAD                | Action           |
| DREAM PICKUP                | Action           |
| DRIFTER COMMANDMENTS        | Action           |
| EASY GLADIATOR              | Action           |
| ENTRAPMENT SATISFACTION     | Action           |
| EXCITEMENT EVE              | Action           |
| FANTASY TROOPERS            | Action           |
| FIREHOUSE VIETNAM           | Action           |
| FOOL MOCKINGBIRD            | Action           |
| FORREST SONS                | Action           |
| GLASS DYING                 | Action           |
| GOSFORD DONNIE              | Action           |
| GRAIL FRANKENSTEIN          | Action           |
| HANDICAP BOONDOCK           | Action           |
| HILLS NEIGHBORS             | Action           |
| KISSING DOLLS               | Action           |
| LAWRENCE LOVE               | Action           |
| LORD ARIZONA                | Action           |
| LUST LOCK                   | Action           |
| MAGNOLIA FORRESTER          | Action           |
| MIDNIGHT WESTWARD           | Action           |
| MINDS TRUMAN                | Action           |
| MOCKINGBIRD HOLLYWOOD       | Action           |
| MONTEZUMA COMMAND           | Action           |
| PARK CITIZEN                | Action           |
| PATRIOT ROMAN               | Action           |
| PRIMARY GLASS               | Action           |
| QUEST MUSSOLINI             | Action           |
| REAR TRADING                | Action           |
| RINGS HEARTBREAKERS         | Action           |
| RUGRATS SHAKESPEARE         | Action           |
| SHRUNK DIVINE               | Action           |
| SIDE ARK                    | Action           |
| SKY MIRACLE                 | Action           |
| SOUTH WAIT                  | Action           |
| SPEAKEASY DATE              | Action           |
| STAGECOACH ARMAGEDDON       | Action           |
| STORY SIDE                  | Action           |
| SUSPECTS QUILLS             | Action           |
| TRIP NEWTON                 | Action           |
| TRUMAN CRAZY                | Action           |
| UPRISING UPTOWN             | Action           |
| WATERFRONT DELIVERANCE      | Action           |
| WEREWOLF LOLA               | Action           |
| WOMEN DORADO                | Action           |
| WORST BANGER                | Action           |
| ALTER VICTORY               | Animation        |
| ANACONDA CONFESSIONS        | Animation        |
| ARGONAUTS TOWN              | Animation        |
| BIKINI BORROWERS            | Animation        |
| BLACKOUT PRIVATE            | Animation        |
| BORROWERS BEDAZZLED         | Animation        |
| CANYON STOCK                | Animation        |
| CAROL TEXAS                 | Animation        |
| CHAMPION FLATLINERS         | Animation        |
| CLASH FREDDY                | Animation        |
| CLUB GRAFFITI               | Animation        |
| CROSSROADS CASUALTIES       | Animation        |
| DARES PLUTO                 | Animation        |
| DESIRE ALIEN                | Animation        |
| DOGMA FAMILY                | Animation        |
| DONNIE ALLEY                | Animation        |
| DOORS PRESIDENT             | Animation        |
| DOUBLE WRATH                | Animation        |
| DUCK RACER                  | Animation        |
| EARLY HOME                  | Animation        |
| FALCON VOLUME               | Animation        |
| FIGHT JAWBREAKER            | Animation        |
| FLOATS GARDEN               | Animation        |
| FLYING HOOK                 | Animation        |
| FORRESTER COMANCHEROS       | Animation        |
| GANGS PRIDE                 | Animation        |
| GHOSTBUSTERS ELF            | Animation        |
| HARPER DYING                | Animation        |
| HOOK CHARIOTS               | Animation        |
| HORN WORKING                | Animation        |
| INCH JET                    | Animation        |
| INSECTS STONE               | Animation        |
| INTENTIONS EMPIRE           | Animation        |
| ISHTAR ROCKETEER            | Animation        |
| JUGGLER HARDLY              | Animation        |
| LAWLESS VISION              | Animation        |
| LUKE MUMMY                  | Animation        |
| MASSAGE IMAGE               | Animation        |
| MENAGERIE RUSHMORE          | Animation        |
| MIRACLE VIRTUAL             | Animation        |
| MISSION ZOOLANDER           | Animation        |
| NASH CHOCOLAT               | Animation        |
| OSCAR GOLD                  | Animation        |
| OZ LIAISONS                 | Animation        |
| PACKER MADIGAN              | Animation        |
| POND SEATTLE                | Animation        |
| POTLUCK MIXED               | Animation        |
| POTTER CONNECTICUT          | Animation        |
| PRIDE ALAMO                 | Animation        |
| PUNK DIVORCE                | Animation        |
| ROOM ROMAN                  | Animation        |
| SLEEPLESS MONSOON           | Animation        |
| SNOWMAN ROLLERCOASTER       | Animation        |
| SONS INTERVIEW              | Animation        |
| STORM HAPPINESS             | Animation        |
| SUGAR WONKA                 | Animation        |
| SUNRISE LEAGUE              | Animation        |
| TELEMARK HEARTBREAKERS      | Animation        |
| THEORY MERMAID              | Animation        |
| THIEF PELICAN               | Animation        |
| TITANIC BOONDOCK            | Animation        |
| TRACY CIDER                 | Animation        |
```

Listar los nombres de las ciudades junto con sus países.

```sql
    SELECT ci.nombre AS ciudad_nombre, pa.nombre AS pais_nombre
    FROM ciudad ci
    JOIN pais pa ON ci.id_pais = pa.id_pais;
    
+----------------------------+---------------------------------------+
| ciudad_nombre              | pais_nombre                           |
+----------------------------+---------------------------------------+
| Kabul                      | Afghanistan                           |
| Batna                      | Algeria                               |
| Bchar                      | Algeria                               |
| Skikda                     | Algeria                               |
| Tafuna                     | American Samoa                        |
| Benguela                   | Angola                                |
| Namibe                     | Angola                                |
| South Hill                 | Anguilla                              |
| Almirante Brown            | Argentina                             |
| Avellaneda                 | Argentina                             |
| Baha Blanca                | Argentina                             |
| Crdoba                     | Argentina                             |
| Escobar                    | Argentina                             |
| Ezeiza                     | Argentina                             |
| La Plata                   | Argentina                             |
| Merlo                      | Argentina                             |
| Quilmes                    | Argentina                             |
| San Miguel de Tucumn       | Argentina                             |
| Santa F                    | Argentina                             |
| Tandil                     | Argentina                             |
| Vicente Lpez               | Argentina                             |
| Yerevan                    | Armenia                               |
| Woodridge                  | Australia                             |
| Graz                       | Austria                               |
| Linz                       | Austria                               |
| Salzburg                   | Austria                               |
| Baku                       | Azerbaijan                            |
| Sumqayit                   | Azerbaijan                            |
| al-Manama                  | Bahrain                               |
| Dhaka                      | Bangladesh                            |
| Jamalpur                   | Bangladesh                            |
| Tangail                    | Bangladesh                            |
| Mogiljov                   | Belarus                               |
| Molodetno                  | Belarus                               |
| El Alto                    | Bolivia                               |
| Sucre                      | Bolivia                               |
| Alvorada                   | Brazil                                |
| Angra dos Reis             | Brazil                                |
| Anpolis                    | Brazil                                |
| Aparecida de Goinia        | Brazil                                |
| Araatuba                   | Brazil                                |
| Bag                        | Brazil                                |
| Belm                       | Brazil                                |
| Blumenau                   | Brazil                                |
| Boa Vista                  | Brazil                                |
| Braslia                    | Brazil                                |
| Goinia                     | Brazil                                |
| Guaruj                     | Brazil                                |
| guas Lindas de Gois        | Brazil                                |
| Ibirit                     | Brazil                                |
| Juazeiro do Norte          | Brazil                                |
| Juiz de Fora               | Brazil                                |
| Luzinia                    | Brazil                                |
| Maring                     | Brazil                                |
| Po                         | Brazil                                |
| Poos de Caldas             | Brazil                                |
| Rio Claro                  | Brazil                                |
| Santa Brbara dOeste        | Brazil                                |
| Santo Andr                 | Brazil                                |
| So Bernardo do Campo       | Brazil                                |
| So Leopoldo                | Brazil                                |
| Sorocaba                   | Brazil                                |
| Vila Velha                 | Brazil                                |
| Vitria de Santo Anto       | Brazil                                |
| Bandar Seri Begawan        | Brunei                                |
| Ruse                       | Bulgaria                              |
| Stara Zagora               | Bulgaria                              |
| Battambang                 | Cambodia                              |
| Phnom Penh                 | Cambodia                              |
| Bamenda                    | Cameroon                              |
| Yaound                     | Cameroon                              |
| Gatineau                   | Canada                                |
| Halifax                    | Canada                                |
| Lethbridge                 | Canada                                |
| London                     | Canada                                |
| Oshawa                     | Canada                                |
| Richmond Hill              | Canada                                |
| Vancouver                  | Canada                                |
| NDjamna                    | Chad                                  |
| Antofagasta                | Chile                                 |
| Coquimbo                   | Chile                                 |
| Rancagua                   | Chile                                 |
| Baicheng                   | China                                 |
| Baiyin                     | China                                 |
| Binzhou                    | China                                 |
| Changzhou                  | China                                 |
| Datong                     | China                                 |
| Daxian                     | China                                 |
| Dongying                   | China                                 |
| Emeishan                   | China                                 |
| Enshi                      | China                                 |
| Ezhou                      | China                                 |
| Fuyu                       | China                                 |
| Fuzhou                     | China                                 |
| Haining                    | China                                 |
| Hami                       | China                                 |
| Hohhot                     | China                                 |
| Huaian                     | China                                 |
| Jinchang                   | China                                 |
| Jining                     | China                                 |
| Jinzhou                    | China                                 |
| Junan                      | China                                 |
| Korla                      | China                                 |
| Laiwu                      | China                                 |
| Laohekou                   | China                                 |
| Lengshuijiang              | China                                 |
| Leshan                     | China                                 |
| Liaocheng                  | China                                 |
| Meixian                    | China                                 |
| Nanyang                    | China                                 |
| Pingxiang                  | China                                 |
| Qinhuangdao                | China                                 |
| Rizhao                     | China                                 |
| Sanya                      | China                                 |
| Shanwei                    | China                                 |
| Shaoguan                   | China                                 |
| Shenzhen                   | China                                 |
| Suihua                     | China                                 |
| Tianjin                    | China                                 |
| Tiefa                      | China                                 |
| Tieli                      | China                                 |
| Tongliao                   | China                                 |
| Weifang                    | China                                 |
| Xiangfan                   | China                                 |
| Xiangtan                   | China                                 |
| Xintai                     | China                                 |
| Xinxiang                   | China                                 |
| Yantai                     | China                                 |
| Yinchuan                   | China                                 |
| Yingkou                    | China                                 |
| Yuncheng                   | China                                 |
| Yuzhou                     | China                                 |
| Zalantun                   | China                                 |
| Zaoyang                    | China                                 |
| Zhoushan                   | China                                 |
| Buenaventura               | Colombia                              |
| Dos Quebradas              | Colombia                              |
| Florencia                  | Colombia                              |
| Pereira                    | Colombia                              |
| Sincelejo                  | Colombia                              |
| Sogamoso                   | Colombia                              |
| Lubumbashi                 | Congo, The Democratic Republic of the |
| Mwene-Ditu                 | Congo, The Democratic Republic of the |
| Olomouc                    | Czech Republic                        |
| La Romana                  | Dominican Republic                    |
| San Felipe de Puerto Plata | Dominican Republic                    |
| Santiago de los Caballeros | Dominican Republic                    |
| Loja                       | Ecuador                               |
| Portoviejo                 | Ecuador                               |
| Robamba                    | Ecuador                               |
| Bilbays                    | Egypt                                 |
| Idfu                       | Egypt                                 |
| Mit Ghamr                  | Egypt                                 |
| Qalyub                     | Egypt                                 |
| Sawhaj                     | Egypt                                 |
| Shubra al-Khayma           | Egypt                                 |
| Tartu                      | Estonia                               |
| Addis Abeba                | Ethiopia                              |
| Trshavn                    | Faroe Islands                         |
| Oulu                       | Finland                               |
| Brest                      | France                                |
| Le Mans                    | France                                |
| Toulon                     | France                                |
| Toulouse                   | France                                |
| Cayenne                    | French Guiana                         |
| Faaa                       | French Polynesia                      |
| Papeete                    | French Polynesia                      |
| Banjul                     | Gambia                                |
| Duisburg                   | Germany                               |
| Erlangen                   | Germany                               |
| Halle/Saale                | Germany                               |
| Mannheim                   | Germany                               |
| Saarbrcken                 | Germany                               |
| Siegen                     | Germany                               |
| Witten                     | Germany                               |
| Athenai                    | Greece                                |
| Patras                     | Greece                                |
| Nuuk                       | Greenland                             |
| Citt del Vaticano          | Holy See (Vatican City State)         |
| Kowloon and New Kowloon    | Hong Kong                             |
| Szkesfehrvr                | Hungary                               |
| Adoni                      | India                                 |
| Ahmadnagar                 | India                                 |
| Allappuzha (Alleppey)      | India                                 |
| Ambattur                   | India                                 |
| Amroha                     | India                                 |
| Balurghat                  | India                                 |
| Berhampore (Baharampur)    | India                                 |
| Bhavnagar                  | India                                 |
| Bhilwara                   | India                                 |
| Bhimavaram                 | India                                 |
| Bhopal                     | India                                 |
| Bhusawal                   | India                                 |
| Bijapur                    | India                                 |
| Chandrapur                 | India                                 |
| Chapra                     | India                                 |
| Dhule (Dhulia)             | India                                 |
```

Obtener los detalles de los alquileres, incluyendo el cliente y el
empleado que gestionó el alquiler.

```sql
SELECT r.id_alquiler, r.fecha_alquiler, r.fecha_devolucion, c.nombre AS cliente_nombre, c.apellidos AS cliente_apellido, e.nombre AS empleado_nombre, e.apellidos AS empleado_apellido
FROM alquiler r
JOIN cliente c ON r.id_cliente = c.id_cliente
JOIN empleado e ON r.id_empleado = e.id_empleado;

TRON          | Jon             | Stephens          |
|        6800 | 2005-07-12 17:03:56 | 2005-07-21 20:32:56 | AUSTIN         | CINTRON          | Jon             | Stephens          |
|        6895 | 2005-07-12 21:23:59 | 2005-07-19 20:47:59 | AUSTIN         | CINTRON          | Jon             | Stephens          |
|        8965 | 2005-07-30 03:52:37 | 2005-08-05 01:28:37 | AUSTIN         | CINTRON          | Jon             | Stephens          |
|        9630 | 2005-07-31 04:57:07 | 2005-08-07 10:55:07 | AUSTIN         | CINTRON          | Jon             | Stephens          |
|        9679 | 2005-07-31 06:41:19 | 2005-08-02 07:23:19 | AUSTIN         | CINTRON          | Mike            | Hillyer           |
|       11522 | 2005-08-17 00:05:05 | 2005-08-24 04:56:05 | AUSTIN         | CINTRON          | Mike            | Hillyer           |
|       14233 | 2005-08-21 05:07:08 | 2005-08-28 03:20:08 | AUSTIN         | CINTRON          | Mike            | Hillyer           |
|       14599 | 2005-08-21 17:43:42 | 2005-08-22 18:53:42 | AUSTIN         | CINTRON          | Mike            | Hillyer           |
|       14719 | 2005-08-21 21:41:57 | 2005-08-25 20:37:57 | AUSTIN         | CINTRON          | Mike            | Hillyer           |
|       15590 | 2005-08-23 06:09:44 | 2005-09-01 06:53:44 | AUSTIN         | CINTRON          | Jon             | Stephens          |
|       15719 | 2005-08-23 11:08:46 | 2005-08-25 07:25:46 | AUSTIN         | CINTRON          | Mike            | Hillyer           |
|       15725 | 2005-08-23 11:25:00 | 2005-08-26 11:46:00 | AUSTIN         | CINTRON          | Mike            | Hillyer           |
+-------------+---------------------+---------------------+----------------+------------------+-----------------+-------------------+
16045 rows in set (0,03 sec)

```

Encontrar todas las películas que se encuentran en un almacén
específico.

```sql

    SELECT p.titulo
    FROM inventario i
    JOIN pelicula p ON i.id_pelicula = p.id_pelicula
    WHERE i.id_almacen = 1;

+-----------------------------+
| pelicula_titulo             |
+-----------------------------+
| ACADEMY DINOSAUR            |
| ACADEMY DINOSAUR            |
| ACADEMY DINOSAUR            |
| ACADEMY DINOSAUR            |
| AFFAIR PREJUDICE            |
| AFFAIR PREJUDICE            |
| AFFAIR PREJUDICE            |
| AFFAIR PREJUDICE            |
| AGENT TRUMAN                |
| AGENT TRUMAN                |
| AGENT TRUMAN                |
| AIRPLANE SIERRA             |
| AIRPLANE SIERRA             |
| ALABAMA DEVIL               |
| ALABAMA DEVIL               |
| ALABAMA DEVIL               |
| ALADDIN CALENDAR            |
| ALADDIN CALENDAR            |
| ALADDIN CALENDAR            |
| ALADDIN CALENDAR            |
| ALAMO VIDEOTAPE             |
| ALAMO VIDEOTAPE             |
| ALAMO VIDEOTAPE             |
| ALAMO VIDEOTAPE             |
| ALASKA PHANTOM              |
| ALASKA PHANTOM              |
| ALASKA PHANTOM              |
| ALIEN CENTER                |
| ALIEN CENTER                |
| ALLEY EVOLUTION             |
| ALLEY EVOLUTION             |
| ALONE TRIP                  |
| ALONE TRIP                  |
| ALONE TRIP                  |
| ALTER VICTORY               |
| ALTER VICTORY               |
| ALTER VICTORY               |
| AMADEUS HOLY                |
| AMADEUS HOLY                |
| AMADEUS HOLY                |
| AMADEUS HOLY                |
| AMELIE HELLFIGHTERS         |
| AMELIE HELLFIGHTERS         |
| AMELIE HELLFIGHTERS         |
| AMERICAN CIRCUS             |
| AMERICAN CIRCUS             |
| AMISTAD MIDSUMMER           |
| AMISTAD MIDSUMMER           |
| AMISTAD MIDSUMMER           |
| AMISTAD MIDSUMMER           |
| ANACONDA CONFESSIONS        |
| ANACONDA CONFESSIONS        |
| ANACONDA CONFESSIONS        |
| ANALYZE HOOSIERS            |
| ANALYZE HOOSIERS            |
| ANALYZE HOOSIERS            |
| ANALYZE HOOSIERS            |
| ANGELS LIFE                 |
| ANGELS LIFE                 |
| ANGELS LIFE                 |
| ANGELS LIFE                 |
| ANNIE IDENTITY              |
| ANNIE IDENTITY              |
| ANONYMOUS HUMAN             |
| ANONYMOUS HUMAN             |
| ANONYMOUS HUMAN             |
| ANONYMOUS HUMAN             |
| ANTHEM LUKE                 |
| ANTHEM LUKE                 |
| ANTHEM LUKE                 |
| ANTITRUST TOMATOES          |
| ANTITRUST TOMATOES          |
| ANYTHING SAVANNAH           |
| ANYTHING SAVANNAH           |
| APACHE DIVINE               |
| APACHE DIVINE               |
| APACHE DIVINE               |
| APACHE DIVINE               |
| ARACHNOPHOBIA ROLLERCOASTER |
| ARACHNOPHOBIA ROLLERCOASTER |
| ARACHNOPHOBIA ROLLERCOASTER |
| ARACHNOPHOBIA ROLLERCOASTER |
| ARIZONA BANG                |
| ARIZONA BANG                |
| ARIZONA BANG                |
| ARIZONA BANG                |
| ARMAGEDDON LOST             |
| ARMAGEDDON LOST             |
| ARMAGEDDON LOST             |
| ATLANTIS CAUSE              |
| ATLANTIS CAUSE              |
| ATLANTIS CAUSE              |
| ATTACKS HATE                |
| ATTACKS HATE                |
| ATTRACTION NEWTON           |
| ATTRACTION NEWTON           |
| ATTRACTION NEWTON           |
| ATTRACTION NEWTON           |
| BACKLASH UNDEFEATED         |
| BACKLASH UNDEFEATED         |
| BADMAN DAWN                 |
| BADMAN DAWN                 |
| BADMAN DAWN                 |
| BAKED CLEOPATRA             |
| BAKED CLEOPATRA             |
| BAKED CLEOPATRA             |
| BALLOON HOMEWARD            |
| BALLOON HOMEWARD            |
| BANG KWAI                   |
| BANG KWAI                   |
| BANGER PINOCCHIO            |
| BANGER PINOCCHIO            |
| BANGER PINOCCHIO            |
| BARBARELLA STREETCAR        |
| BARBARELLA STREETCAR        |
| BARBARELLA STREETCAR        |
| BARBARELLA STREETCAR        |
| BAREFOOT MANCHURIAN         |
| BAREFOOT MANCHURIAN         |
| BAREFOOT MANCHURIAN         |
| BASIC EASY                  |
| BASIC EASY                  |
| BASIC EASY                  |
| BASIC EASY                  |
| BEAR GRACELAND              |
| BEAR GRACELAND              |
| BEAR GRACELAND              |
| BEAST HUNCHBACK             |
| BEAST HUNCHBACK             |
| BEAST HUNCHBACK             |
| BEAUTY GREASE               |
| BEAUTY GREASE               |
| BEAUTY GREASE               |
| BEAUTY GREASE               |
| BEDAZZLED MARRIED           |
| BEDAZZLED MARRIED           |
| BENEATH RUSH                |
| BENEATH RUSH                |
| BENEATH RUSH                |
| BERETS AGENT                |
| BERETS AGENT                |
| BETRAYED REAR               |
| BETRAYED REAR               |
| BEVERLY OUTLAW              |
| BEVERLY OUTLAW              |
| BEVERLY OUTLAW              |
| BEVERLY OUTLAW              |
| BIKINI BORROWERS            |
| BIKINI BORROWERS            |
| BILL OTHERS                 |
| BILL OTHERS                 |
| BILL OTHERS                 |
| BILL OTHERS                 |
| BINGO TALENTED              |
| BINGO TALENTED              |
| BINGO TALENTED              |
| BINGO TALENTED              |
| BIRCH ANTITRUST             |
| BIRCH ANTITRUST             |
| BIRCH ANTITRUST             |
| BIRDCAGE CASPER             |
| BIRDCAGE CASPER             |
| BIRDCAGE CASPER             |
| BIRDS PERDITION             |
| BIRDS PERDITION             |
| BIRDS PERDITION             |
| BIRDS PERDITION             |
| BLACKOUT PRIVATE            |
| BLACKOUT PRIVATE            |
| BLACKOUT PRIVATE            |
| BLADE POLISH                |
| BLADE POLISH                |
| BLADE POLISH                |
| BLANKET BEVERLY             |
| BLANKET BEVERLY             |
| BLANKET BEVERLY             |
| BLANKET BEVERLY             |
| BLINDNESS GUN               |
| BLINDNESS GUN               |
| BLINDNESS GUN               |
| BLINDNESS GUN               |
| BLOOD ARGONAUTS             |
| BLOOD ARGONAUTS             |
| BLUES INSTINCT              |
| BLUES INSTINCT              |
| BLUES INSTINCT              |
| BOILED DARES                |
| BOILED DARES                |
| BOILED DARES                |
| BOILED DARES                |
| BOOGIE AMELIE               |
| BOOGIE AMELIE               |
| BOOGIE AMELIE               |
| BOOGIE AMELIE               |
| BORROWERS BEDAZZLED         |
| BORROWERS BEDAZZLED         |
| BORROWERS BEDAZZLED         |
| BOULEVARD MOB               |
| BOULEVARD MOB               |
| BOULEVARD MOB               |
| BOUND CHEAPER               |
| BOUND CHEAPER               |
| BOUND CHEAPER               |
| BOUND CHEAPER               |
| BOWFINGER GABLES            |
| BOWFINGER GABLES            |
| BRAVEHEART HUMAN            |
| BRAVEHEART HUMAN            |
| BREAKFAST GOLDFINGER        |
| BREAKFAST GOLDFINGER        |
| BREAKING HOME               |
| BREAKING HOME               |
| BREAKING HOME               |
| BRIDE INTRIGUE              |
| BRIDE INTRIGUE              |
| BRIDE INTRIGUE              |
| BRIDE INTRIGUE              |
| BRIGHT ENCOUNTERS           |
| BRIGHT ENCOUNTERS           |
| BRIGHT ENCOUNTERS           |
| BRINGING HYSTERICAL         |
| BRINGING HYSTERICAL         |
| BRINGING HYSTERICAL         |
| BROOKLYN DESERT             |
| BROOKLYN DESERT             |
| BROOKLYN DESERT             |
| BROOKLYN DESERT             |
| BROTHERHOOD BLANKET         |
| BROTHERHOOD BLANKET         |
| BROTHERHOOD BLANKET         |
| BROTHERHOOD BLANKET         |
| BUCKET BROTHERHOOD          |
| BUCKET BROTHERHOOD          |
| BUCKET BROTHERHOOD          |
| BUCKET BROTHERHOOD          |
| BULL SHAWSHANK              |
| BULL SHAWSHANK              |
| BULWORTH COMMANDMENTS       |
| BULWORTH COMMANDMENTS       |
| BUTTERFLY CHOCOLAT          |
| BUTTERFLY CHOCOLAT          |
| BUTTERFLY CHOCOLAT          |
| BUTTERFLY CHOCOLAT          |
| CABIN FLASH                 |
| CABIN FLASH                 |
| CABIN FLASH                 |
| CABIN FLASH                 |
| CALENDAR GUNFIGHT           |
| CALENDAR GUNFIGHT           |
| CALENDAR GUNFIGHT           |
| CALENDAR GUNFIGHT           |
| CAMELOT VACATION            |
| CAMELOT VACATION            |
| CAMELOT VACATION            |
| CAMELOT VACATION            |
| CAMPUS REMEMBER             |
| CAMPUS REMEMBER             |
| CAMPUS REMEMBER             |
| CANDIDATE PERDITION         |
| CANDIDATE PERDITION         |
| CANDLES GRAPES              |
| CANDLES GRAPES              |
| CANDLES GRAPES              |
| CANDLES GRAPES              |
| CANYON STOCK                |
| CANYON STOCK                |
| CANYON STOCK                |
| CANYON STOCK                |
| CAPER MOTIONS               |
| CAPER MOTIONS               |
| CAPER MOTIONS               |
| CARIBBEAN LIBERTY           |
| CARIBBEAN LIBERTY           |
| CARIBBEAN LIBERTY           |
| CAROL TEXAS                 |
| CAROL TEXAS                 |
| CAROL TEXAS                 |
| CARRIE BUNCH                |
| CARRIE BUNCH                |
| CARRIE BUNCH                |
| CARRIE BUNCH                |
| CASABLANCA SUPER            |
| CASABLANCA SUPER            |
| CAT CONEHEADS               |
| CAT CONEHEADS               |
| CAT CONEHEADS               |
| CAT CONEHEADS               |
| CAUSE DATE                  |
| CAUSE DATE                  |
| CAUSE DATE                  |
| CELEBRITY HORN              |
| CELEBRITY HORN              |
| CENTER DINOSAUR             |
| CENTER DINOSAUR             |
| CENTER DINOSAUR             |
| CENTER DINOSAUR             |
| CHAINSAW UPTOWN             |
| CHAINSAW UPTOWN             |
| CHAINSAW UPTOWN             |
| CHAINSAW UPTOWN             |
| CHAMBER ITALIAN             |
| CHAMBER ITALIAN             |
| CHANCE RESURRECTION         |
| CHANCE RESURRECTION         |
| CHANCE RESURRECTION         |
| CHAPLIN LICENSE             |
| CHAPLIN LICENSE             |
| CHAPLIN LICENSE             |
| CHARIOTS CONSPIRACY         |
| CHARIOTS CONSPIRACY         |
| CHASING FIGHT               |
| CHASING FIGHT               |
| CHASING FIGHT               |
| CHASING FIGHT               |
| CHEAPER CLYDE               |
| CHEAPER CLYDE               |
| CHICAGO NORTH               |
| CHICAGO NORTH               |
| CHICAGO NORTH               |
| CHICKEN HELLFIGHTERS        |
| CHICKEN HELLFIGHTERS        |
| CHICKEN HELLFIGHTERS        |
| CHILL LUCK                  |
| CHILL LUCK                  |
| CHILL LUCK                  |
| CHILL LUCK                  |
| CHITTY LOCK                 |
| CHITTY LOCK                 |
| CHITTY LOCK                 |
| CHOCOLAT HARRY              |
| CHOCOLAT HARRY              |
| CHOCOLAT HARRY              |
| CHRISTMAS MOONSHINE         |
| CHRISTMAS MOONSHINE         |
| CHRISTMAS MOONSHINE         |
| CIDER DESIRE                |
| CIDER DESIRE                |
| CINCINATTI WHISPERER        |
| CINCINATTI WHISPERER        |
| CIRCUS YOUTH                |
| CIRCUS YOUTH                |
| CIRCUS YOUTH                |
| CIRCUS YOUTH                |
| CITIZEN SHREK               |
| CITIZEN SHREK               |
| CITIZEN SHREK               |
| CITIZEN SHREK               |
| CLASH FREDDY                |
| CLASH FREDDY                |
| CLASH FREDDY                |
| CLEOPATRA DEVIL             |
| CLEOPATRA DEVIL             |
| CLONES PINOCCHIO            |
| CLONES PINOCCHIO            |
| CLOSER BANG                 |
| CLOSER BANG                 |
| CLOSER BANG                 |
| CLOSER BANG                 |
| CLUB GRAFFITI               |
| CLUB GRAFFITI               |
| CLUE GRAIL                  |
| CLUE GRAIL                  |
| CLUELESS BUCKET             |
| CLUELESS BUCKET             |
| CLUELESS BUCKET             |
| COAST RAINBOW               |
| COAST RAINBOW               |
| COLDBLOODED DARLING         |
| COLDBLOODED DARLING         |
| COLDBLOODED DARLING         |
| COLOR PHILADELPHIA          |
| COLOR PHILADELPHIA          |
| COLOR PHILADELPHIA          |
| COLOR PHILADELPHIA          |
| COMA HEAD                   |
| COMA HEAD                   |
| COMA HEAD                   |
| COMA HEAD                   |
| COMANCHEROS ENEMY           |
| COMANCHEROS ENEMY           |
| COMFORTS RUSH               |
| COMFORTS RUSH               |
| COMMAND DARLING             |
| COMMAND DARLING             |
| CONEHEADS SMOOCHY           |
| CONEHEADS SMOOCHY           |
| CONEHEADS SMOOCHY           |
| CONEHEADS SMOOCHY           |
| CONFESSIONS MAGUIRE         |
| CONFESSIONS MAGUIRE         |
| CONFESSIONS MAGUIRE         |
| CONFIDENTIAL INTERVIEW      |
| CONFIDENTIAL INTERVIEW      |
| CONFIDENTIAL INTERVIEW      |
| CONFIDENTIAL INTERVIEW      |
| CONFUSED CANDLES            |
| CONFUSED CANDLES            |
| CONGENIALITY QUEST          |
| CONGENIALITY QUEST          |
| CONNECTION MICROCOSMOS      |
| CONNECTION MICROCOSMOS      |
| CONQUERER NUTS              |
| CONQUERER NUTS              |
| CONQUERER NUTS              |
| CONQUERER NUTS              |
| CONTACT ANONYMOUS           |
| CONTACT ANONYMOUS           |
| CONTACT ANONYMOUS           |
| CONTROL ANTHEM              |
| CONTROL ANTHEM              |
| CONVERSATION DOWNHILL       |
| CONVERSATION DOWNHILL       |
| CONVERSATION DOWNHILL       |
| CORE SUIT                   |
| CORE SUIT                   |
| COWBOY DOOM                 |
| COWBOY DOOM                 |
| CRAFT OUTFIELD              |
| CRAFT OUTFIELD              |
| CRAZY HOME                  |
| CRAZY HOME                  |
| CRAZY HOME                  |
| CREATURES SHAKESPEARE       |
| CREATURES SHAKESPEARE       |
| CROOKED FROGMEN             |
| CROOKED FROGMEN             |
| CROOKED FROGMEN             |
| CROSSROADS CASUALTIES       |
| CROSSROADS CASUALTIES       |
| CROSSROADS CASUALTIES       |
| CROSSROADS CASUALTIES       |
| CROW GREASE                 |
| CROW GREASE                 |
| CRUELTY UNFORGIVEN          |
| CRUELTY UNFORGIVEN          |
| CRUSADE HONEY               |
| CRUSADE HONEY               |
| CUPBOARD SINNERS            |
| CUPBOARD SINNERS            |
| CUPBOARD SINNERS            |
| CUPBOARD SINNERS            |
| CURTAIN VIDEOTAPE           |
| CURTAIN VIDEOTAPE           |
| CURTAIN VIDEOTAPE           |
| CURTAIN VIDEOTAPE           |
| CYCLONE FAMILY              |
| CYCLONE FAMILY              |
| CYCLONE FAMILY              |
| CYCLONE FAMILY              |
| DADDY PITTSBURGH            |
| DADDY PITTSBURGH            |
| DADDY PITTSBURGH            |
| DALMATIONS SWEDEN           |
| DALMATIONS SWEDEN           |
| DALMATIONS SWEDEN           |
| DALMATIONS SWEDEN           |
| DANCES NONE                 |
| DANCES NONE                 |
| DANCES NONE                 |
| DANCES NONE                 |
| DANCING FEVER               |
| DANCING FEVER               |
| DANCING FEVER               |
| DANCING FEVER               |
| DANGEROUS UPTOWN            |
| DANGEROUS UPTOWN            |
| DANGEROUS UPTOWN            |
| DANGEROUS UPTOWN            |
| DARES PLUTO                 |
| DARES PLUTO                 |
| DARES PLUTO                 |
| DARKNESS WAR                |
| DARKNESS WAR                |
| DARKNESS WAR                |
| DARKNESS WAR                |
| DARLING BREAKING            |
| DARLING BREAKING            |
| DARN FORRESTER              |
| DARN FORRESTER              |
| DARN FORRESTER              |
| DATE SPEED                  |
| DATE SPEED                  |
| DATE SPEED                  |
| DATE SPEED                  |
| DAWN POND                   |
| DAWN POND                   |
| DAWN POND                   |
| DAY UNFAITHFUL              |
| DAY UNFAITHFUL              |
| DECEIVER BETRAYED           |
| DECEIVER BETRAYED           |
| DECEIVER BETRAYED           |
| DECEIVER BETRAYED           |
| DEEP CRUSADE                |
| DEEP CRUSADE                |
| DEEP CRUSADE                |
| DEEP CRUSADE                |
| DEER VIRGINIAN              |
| DEER VIRGINIAN              |
| DEER VIRGINIAN              |
| DEER VIRGINIAN              |
| DESERT POSEIDON             |
| DESERT POSEIDON             |
| DESPERATE TRAINSPOTTING     |
| DESPERATE TRAINSPOTTING     |
| DESTINATION JERK            |
| DESTINATION JERK            |
| DESTINATION JERK            |
| DESTINY SATURDAY            |
| DESTINY SATURDAY            |
| DETAILS PACKER              |
| DETAILS PACKER              |
| DETAILS PACKER              |
| DETECTIVE VISION            |
| DETECTIVE VISION            |
| DETECTIVE VISION            |
| DEVIL DESIRE                |
| DEVIL DESIRE                |
| DIARY PANIC                 |
| DIARY PANIC                 |
| DINOSAUR SECRETARY          |
| DINOSAUR SECRETARY          |
| DINOSAUR SECRETARY          |
| DINOSAUR SECRETARY          |
| DIRTY ACE                   |
| DIRTY ACE                   |
| DIRTY ACE                   |
| DISCIPLE MOTHER             |
| DISCIPLE MOTHER             |
| DISCIPLE MOTHER             |
| DISCIPLE MOTHER             |
| DISTURBING SCARFACE         |
| DISTURBING SCARFACE         |
| DISTURBING SCARFACE         |
| DISTURBING SCARFACE         |
| DIVIDE MONSTER              |
| DIVIDE MONSTER              |
| DIVORCE SHINING             |
| DIVORCE SHINING             |
| DOCTOR GRAIL                |
| DOCTOR GRAIL                |
| DOGMA FAMILY                |
| DOGMA FAMILY                |
| DOGMA FAMILY                |
| DOGMA FAMILY                |
| DONNIE ALLEY                |
| DONNIE ALLEY                |
| DONNIE ALLEY                |
| DONNIE ALLEY                |
| DOOM DANCING                |
| DOOM DANCING                |
| DOORS PRESIDENT             |
| DOORS PRESIDENT             |
| DORADO NOTTING              |
| DORADO NOTTING              |
| DORADO NOTTING              |
| DORADO NOTTING              |
| DOUBLE WRATH                |
| DOUBLE WRATH                |
| DOUBLE WRATH                |
| DOWNHILL ENOUGH             |
| DOWNHILL ENOUGH             |
| DOWNHILL ENOUGH             |
| DRACULA CRYSTAL             |
| DRACULA CRYSTAL             |
| DRAGONFLY STRANGERS         |
| DRAGONFLY STRANGERS         |
| DREAM PICKUP                |
| DREAM PICKUP                |
| DREAM PICKUP                |
| DRIFTER COMMANDMENTS        |
| DRIFTER COMMANDMENTS        |
| DRIFTER COMMANDMENTS        |
| DRIFTER COMMANDMENTS        |
| DRIVER ANNIE                |
| DRIVER ANNIE                |
| DRIVING POLISH              |
| DRIVING POLISH              |
| DRIVING POLISH              |
| DRIVING POLISH              |
| DUCK RACER                  |
| DUCK RACER                  |
| DUFFEL APOCALYPSE           |
| DUFFEL APOCALYPSE           |
| DURHAM PANKY                |
| DURHAM PANKY                |
| DURHAM PANKY                |
| DURHAM PANKY                |
| DYING MAKER                 |
| DYING MAKER                 |
| DYING MAKER                 |
| DYING MAKER                 |
| DYNAMITE TARZAN             |
| DYNAMITE TARZAN             |
| DYNAMITE TARZAN             |
| DYNAMITE TARZAN             |
| EAGLES PANKY                |
| EAGLES PANKY                |
| EAGLES PANKY                |
| EAGLES PANKY                |
| EARRING INSTINCT            |
| EARRING INSTINCT            |
| EARTH VISION                |
| EARTH VISION                |
| EARTH VISION                |
| EASY GLADIATOR              |
| EASY GLADIATOR              |
| EASY GLADIATOR              |
| EDGE KISSING                |
| EDGE KISSING                |
| EDGE KISSING                |
| EDGE KISSING                |
| EFFECT GLADIATOR            |
| EFFECT GLADIATOR            |
| EFFECT GLADIATOR            |
| EFFECT GLADIATOR            |
| EGG IGBY                    |
| EGG IGBY                    |
| EGG IGBY                    |
| EGYPT TENENBAUMS            |
| EGYPT TENENBAUMS            |
| EGYPT TENENBAUMS            |
| ELEMENT FREDDY              |
| ELEMENT FREDDY              |
| ELEMENT FREDDY              |
| ELEMENT FREDDY              |
| ELEPHANT TROJAN             |
| ELEPHANT TROJAN             |
| ELEPHANT TROJAN             |
| ELF MURDER                  |
| ELF MURDER                  |
| ELIZABETH SHANE             |
| ELIZABETH SHANE             |
| EMPIRE MALKOVICH            |
| EMPIRE MALKOVICH            |
| EMPIRE MALKOVICH            |
| EMPIRE MALKOVICH            |
| ENCINO ELF                  |
| ENCINO ELF                  |
| ENCOUNTERS CURTAIN          |
| ENCOUNTERS CURTAIN          |
| ENCOUNTERS CURTAIN          |
| ENDING CROWDS               |
| ENDING CROWDS               |
| ENDING CROWDS               |
| ENEMY ODDS                  |
| ENEMY ODDS                  |
| ENEMY ODDS                  |
| ENGLISH BULWORTH            |
| ENGLISH BULWORTH            |
| ENGLISH BULWORTH            |
| ENOUGH RAGING               |
| ENOUGH RAGING               |
| ENTRAPMENT SATISFACTION     |
| ENTRAPMENT SATISFACTION     |
| ESCAPE METROPOLIS           |
| ESCAPE METROPOLIS           |
| EVE RESURRECTION            |
| EVE RESURRECTION            |
| EVERYONE CRAFT              |
| EVERYONE CRAFT              |
| EVERYONE CRAFT              |
| EVOLUTION ALTER             |
| EVOLUTION ALTER             |
| EVOLUTION ALTER             |
| EVOLUTION ALTER             |
| EXCITEMENT EVE              |
| EXCITEMENT EVE              |
| EXCITEMENT EVE              |
| EXORCIST STING              |
| EXORCIST STING              |
| EXPECATIONS NATURAL         |
| EXPECATIONS NATURAL         |
| EXPENDABLE STALLION         |
| EXPENDABLE STALLION         |
| EXPENDABLE STALLION         |
| EXPENDABLE STALLION         |
| EXPRESS LONELY              |
| EXPRESS LONELY              |
| EXPRESS LONELY              |
| EXPRESS LONELY              |
| EYES DRIVING                |
| EYES DRIVING                |
| FACTORY DRAGON              |
| FACTORY DRAGON              |
| FACTORY DRAGON              |
| FACTORY DRAGON              |
| FALCON VOLUME               |
| FALCON VOLUME               |
| FAMILY SWEET                |
| FAMILY SWEET                |
| FAMILY SWEET                |
| FAMILY SWEET                |
| FANTASIA PARK               |
| FANTASIA PARK               |
| FANTASY TROOPERS            |
| FANTASY TROOPERS            |
| FANTASY TROOPERS            |
| FANTASY TROOPERS            |
| FARGO GANDHI                |
| FARGO GANDHI                |
| FARGO GANDHI                |
| FARGO GANDHI                |
| FATAL HAUNTED               |
| FATAL HAUNTED               |
| FATAL HAUNTED               |
| FATAL HAUNTED               |
| FEATHERS METAL              |
| FEATHERS METAL              |
| FEATHERS METAL              |
| FELLOWSHIP AUTUMN           |
| FELLOWSHIP AUTUMN           |
| FELLOWSHIP AUTUMN           |
| FERRIS MOTHER               |
| FERRIS MOTHER               |
| FEUD FROGMEN                |
| FEUD FROGMEN                |
| FEVER EMPIRE                |
| FEVER EMPIRE                |
| FICTION CHRISTMAS           |
| FICTION CHRISTMAS           |
| FICTION CHRISTMAS           |
| FIDELITY DEVIL              |
| FIDELITY DEVIL              |
| FIDELITY DEVIL              |
| FIDELITY DEVIL              |
| FIGHT JAWBREAKER            |
| FIGHT JAWBREAKER            |
| FIREBALL PHILADELPHIA       |
| FIREBALL PHILADELPHIA       |
| FIREBALL PHILADELPHIA       |
| FIREBALL PHILADELPHIA       |
| FISH OPUS                   |
| FISH OPUS                   |
| FISH OPUS                   |
| FLAMINGOS CONNECTICUT       |
| FLAMINGOS CONNECTICUT       |
| FLAMINGOS CONNECTICUT       |
| FLASH WARS                  |
| FLASH WARS                  |
| FLASH WARS                  |
| FLASH WARS                  |
| FLATLINERS KILLER           |
| FLATLINERS KILLER           |
| FLATLINERS KILLER           |
| FLATLINERS KILLER           |
| FLINTSTONES HAPPINESS       |
| FLINTSTONES HAPPINESS       |
| FLINTSTONES HAPPINESS       |
| FLYING HOOK                 |
| FLYING HOOK                 |
| FOOL MOCKINGBIRD            |
| FOOL MOCKINGBIRD            |
| FOOL MOCKINGBIRD            |
| FOOL MOCKINGBIRD            |
| FORREST SONS                |
| FORREST SONS                |
| FORREST SONS                |
| FORRESTER COMANCHEROS       |
| FORRESTER COMANCHEROS       |
| FORRESTER COMANCHEROS       |
| FORRESTER COMANCHEROS       |
| FORWARD TEMPLE              |
| FORWARD TEMPLE              |
| FORWARD TEMPLE              |
| FORWARD TEMPLE              |
| FREAKY POCUS                |
| FREAKY POCUS                |
| FREDDY STORM                |
| FREDDY STORM                |
| FREEDOM CLEOPATRA           |
| FREEDOM CLEOPATRA           |
| FRENCH HOLIDAY              |
| FRENCH HOLIDAY              |
| FRENCH HOLIDAY              |
| FRIDA SLIPPER               |
| FRIDA SLIPPER               |
| FRONTIER CABIN              |
| FRONTIER CABIN              |
| FROST HEAD                  |
| FROST HEAD                  |
| FROST HEAD                  |
| FROST HEAD                  |
| FUGITIVE MAGUIRE            |
| FUGITIVE MAGUIRE            |
| FUGITIVE MAGUIRE            |
| FUGITIVE MAGUIRE            |
| FULL FLATLINERS             |
| FULL FLATLINERS             |
| FURY MURDER                 |
| FURY MURDER                 |
| FURY MURDER                 |
| GABLES METROPOLIS           |
| GABLES METROPOLIS           |
| GABLES METROPOLIS           |
| GALAXY SWEETHEARTS          |
| GALAXY SWEETHEARTS          |
| GAMES BOWFINGER             |
| GAMES BOWFINGER             |
| GAMES BOWFINGER             |
| GAMES BOWFINGER             |
| GANGS PRIDE                 |
| GANGS PRIDE                 |
| GANGS PRIDE                 |
| GANGS PRIDE                 |
| GARDEN ISLAND               |
| GARDEN ISLAND               |
| GARDEN ISLAND               |
| GARDEN ISLAND               |
| GASLIGHT CRUSADE            |
| GASLIGHT CRUSADE            |
| GASLIGHT CRUSADE            |
| GENTLEMEN STAGE             |
| GENTLEMEN STAGE             |
| GHOST GROUNDHOG             |
| GHOST GROUNDHOG             |
| GHOST GROUNDHOG             |
| GIANT TROOPERS              |
| GIANT TROOPERS              |
| GIANT TROOPERS              |
| GIANT TROOPERS              |
| GILMORE BOILED              |
| GILMORE BOILED              |
| GILMORE BOILED              |
| GILMORE BOILED              |
| GLASS DYING                 |
| GLASS DYING                 |
| GLASS DYING                 |
| GLASS DYING                 |
| GLEAMING JAWBREAKER         |
| GLEAMING JAWBREAKER         |
| GLEAMING JAWBREAKER         |
| GLEAMING JAWBREAKER         |
| GLORY TRACY                 |
| GLORY TRACY                 |
| GO PURPLE                   |
| GO PURPLE                   |
| GO PURPLE                   |
| GODFATHER DIARY             |
| GODFATHER DIARY             |
| GODFATHER DIARY             |
| GOLD RIVER                  |
| GOLD RIVER                  |
| GOLDFINGER SENSIBILITY      |
| GOLDFINGER SENSIBILITY      |
| GOLDFINGER SENSIBILITY      |
| GOLDFINGER SENSIBILITY      |
| GOLDMINE TYCOON             |
| GOLDMINE TYCOON             |
| GOLDMINE TYCOON             |
| GOLDMINE TYCOON             |
| GONE TROUBLE                |
| GONE TROUBLE                |
| GOODFELLAS SALUTE           |
| GOODFELLAS SALUTE           |
| GOODFELLAS SALUTE           |
| GOODFELLAS SALUTE           |
| GORGEOUS BINGO              |
| GORGEOUS BINGO              |
| GORGEOUS BINGO              |
| GOSFORD DONNIE              |
| GOSFORD DONNIE              |
| GOSFORD DONNIE              |
| GRACELAND DYNAMITE          |
| GRACELAND DYNAMITE          |
| GRADUATE LORD               |
| GRADUATE LORD               |
| GRADUATE LORD               |
| GRAFFITI LOVE               |
| GRAFFITI LOVE               |
| GRAFFITI LOVE               |
| GRAIL FRANKENSTEIN          |
| GRAIL FRANKENSTEIN          |
| GRAPES FURY                 |
| GRAPES FURY                 |
| GRAPES FURY                 |
| GRAPES FURY                 |
| GREASE YOUTH                |
| GREASE YOUTH                |
| GREASE YOUTH                |
| GREATEST NORTH              |
| GREATEST NORTH              |
| GREATEST NORTH              |
| GREATEST NORTH              |
| GREEK EVERYONE              |
| GREEK EVERYONE              |
| GRINCH MASSAGE              |
| GRINCH MASSAGE              |
| GRIT CLOCKWORK              |
| GRIT CLOCKWORK              |
| GRIT CLOCKWORK              |
| GRIT CLOCKWORK              |
| GROOVE FICTION              |
| GROOVE FICTION              |
| GROOVE FICTION              |
| GROUNDHOG UNCUT             |
| GROUNDHOG UNCUT             |
| GUN BONNIE                  |
| GUN BONNIE                  |
| GUN BONNIE                  |
| GUNFIGHT MOON               |
| GUNFIGHT MOON               |
| GUNFIGHT MOON               |
| GUNFIGHTER MUSSOLINI        |
| GUNFIGHTER MUSSOLINI        |
| GUYS FALCON                 |
| GUYS FALCON                 |
| GUYS FALCON                 |
| HALF OUTFIELD               |
| HALF OUTFIELD               |
| HALF OUTFIELD               |
| HALF OUTFIELD               |
| HALL CASSIDY                |
| HALL CASSIDY                |
| HALL CASSIDY                |
| HALL CASSIDY                |
| HALLOWEEN NUTS              |
| HALLOWEEN NUTS              |
| HAMLET WISDOM               |
| HAMLET WISDOM               |
| HAMLET WISDOM               |
| HAMLET WISDOM               |
| HANDICAP BOONDOCK           |
| HANDICAP BOONDOCK           |
| HANDICAP BOONDOCK           |
| HANKY OCTOBER               |
| HANKY OCTOBER               |
| HANKY OCTOBER               |
| HARDLY ROBBERS              |
| HARDLY ROBBERS              |
| HAROLD FRENCH               |
| HAROLD FRENCH               |
| HARPER DYING                |
| HARPER DYING                |
| HARPER DYING                |
| HARRY IDAHO                 |
| HARRY IDAHO                 |
| HARRY IDAHO                 |
| HARRY IDAHO                 |
| HAUNTING PIANIST            |
| HAUNTING PIANIST            |
| HAWK CHILL                  |
| HAWK CHILL                  |
| HEAD STRANGER               |
| HEAD STRANGER               |
| HEAD STRANGER               |
| HEAD STRANGER               |
| HEARTBREAKERS BRIGHT        |
| HEARTBREAKERS BRIGHT        |
| HEARTBREAKERS BRIGHT        |
| HEARTBREAKERS BRIGHT        |
| HEAVEN FREEDOM              |
| HEAVEN FREEDOM              |
| HEAVEN FREEDOM              |
| HEAVENLY GUN                |
| HEAVENLY GUN                |
| HEAVYWEIGHTS BEAST          |
| HEAVYWEIGHTS BEAST          |
| HEAVYWEIGHTS BEAST          |
| HEAVYWEIGHTS BEAST          |
| HEDWIG ALTER                |
| HEDWIG ALTER                |
| HEDWIG ALTER                |
| HELLFIGHTERS SIERRA         |
| HELLFIGHTERS SIERRA         |
| HELLFIGHTERS SIERRA         |
| HIGH ENCINO                 |
| HIGH ENCINO                 |
| HIGH ENCINO                 |
| HIGHBALL POTTER             |
| HIGHBALL POTTER             |
| HILLS NEIGHBORS             |
| HILLS NEIGHBORS             |
| HILLS NEIGHBORS             |
| HILLS NEIGHBORS             |
| HOBBIT ALIEN                |
| HOBBIT ALIEN                |
| HOBBIT ALIEN                |
| HOBBIT ALIEN                |
| HOLES BRANNIGAN             |
| HOLES BRANNIGAN             |
| HOLLYWOOD ANONYMOUS         |
| HOLLYWOOD ANONYMOUS         |
| HOLOCAUST HIGHBALL          |
| HOLOCAUST HIGHBALL          |
| HOLOCAUST HIGHBALL          |
| HOMEWARD CIDER              |
| HOMEWARD CIDER              |
| HOMEWARD CIDER              |
| HOMEWARD CIDER              |
| HOMICIDE PEACH              |
| HOMICIDE PEACH              |
| HOMICIDE PEACH              |
| HOMICIDE PEACH              |
| HONEY TIES                  |
| HONEY TIES                  |
| HOPE TOOTSIE                |
| HOPE TOOTSIE                |
| HOPE TOOTSIE                |
| HORN WORKING                |
| HORN WORKING                |
| HORN WORKING                |
| HORN WORKING                |
| HORROR REIGN                |
| HORROR REIGN                |
| HORROR REIGN                |
| HORROR REIGN                |
| HOTEL HAPPINESS             |
| HOTEL HAPPINESS             |
| HOURS RAGE                  |
| HOURS RAGE                  |
| HOURS RAGE                  |
| HOUSE DYNAMITE              |
| HOUSE DYNAMITE              |
| HUMAN GRAFFITI              |
| HUMAN GRAFFITI              |
| HUNCHBACK IMPOSSIBLE        |
| HUNCHBACK IMPOSSIBLE        |
| HUNCHBACK IMPOSSIBLE        |
| HUNCHBACK IMPOSSIBLE        |
| HUNGER ROOF                 |
| HUNGER ROOF                 |
| HUNTER ALTER                |
| HUNTER ALTER                |
| HUNTING MUSKETEERS          |
| HUNTING MUSKETEERS          |
| HUNTING MUSKETEERS          |
| HURRICANE AFFAIR            |
| HURRICANE AFFAIR            |
| HURRICANE AFFAIR            |
| HUSTLER PARTY               |
| HUSTLER PARTY               |
| HUSTLER PARTY               |
| HUSTLER PARTY               |
| HYDE DOCTOR                 |
| HYDE DOCTOR                 |
| HYDE DOCTOR                 |
| HYSTERICAL GRAIL            |
| HYSTERICAL GRAIL            |
| ICE CROSSING                |
| ICE CROSSING                |
| ICE CROSSING                |
| ICE CROSSING                |
| IDAHO LOVE                  |
| IDAHO LOVE                  |
| IDOLS SNATCHERS             |
| IDOLS SNATCHERS             |
| IDOLS SNATCHERS             |
| IGBY MAKER                  |
| IGBY MAKER                  |
| IMAGE PRINCESS              |
| IMAGE PRINCESS              |
| IMAGE PRINCESS              |
| IMPACT ALADDIN              |
| IMPACT ALADDIN              |
| IMPOSSIBLE PREJUDICE        |
| IMPOSSIBLE PREJUDICE        |
| IMPOSSIBLE PREJUDICE        |
| IMPOSSIBLE PREJUDICE        |
| INCH JET                    |
| INCH JET                    |
| INDEPENDENCE HOTEL          |
| INDEPENDENCE HOTEL          |
| INDIAN LOVE                 |
| INDIAN LOVE                 |
| INNOCENT USUAL              |
| INNOCENT USUAL              |
| INNOCENT USUAL              |
| INNOCENT USUAL              |
| INSECTS STONE               |
| INSECTS STONE               |
| INSIDER ARIZONA             |
| INSIDER ARIZONA             |
| INSTINCT AIRPORT            |
| INSTINCT AIRPORT            |
| INSTINCT AIRPORT            |
| INTENTIONS EMPIRE           |
| INTENTIONS EMPIRE           |
| INTENTIONS EMPIRE           |
| INTENTIONS EMPIRE           |
| INTERVIEW LIAISONS          |
| INTERVIEW LIAISONS          |
| INTOLERABLE INTENTIONS      |
| INTOLERABLE INTENTIONS      |
| INTRIGUE WORST              |
| INTRIGUE WORST              |
| INTRIGUE WORST              |
| INTRIGUE WORST              |
| INVASION CYCLONE            |
| INVASION CYCLONE            |
| INVASION CYCLONE            |
| INVASION CYCLONE            |
| ISHTAR ROCKETEER            |
| ISHTAR ROCKETEER            |
| ISLAND EXORCIST             |
| ISLAND EXORCIST             |
| ISLAND EXORCIST             |
| JACKET FRISCO               |
| JACKET FRISCO               |
| JASON TRAP                  |
| JASON TRAP                  |
| JASON TRAP                  |
| JAWS HARRY                  |
| JAWS HARRY                  |
| JEDI BENEATH                |
| JEDI BENEATH                |
| JEEPERS WEDDING             |
| JEEPERS WEDDING             |
| JEKYLL FROGMEN              |
| JEKYLL FROGMEN              |
| JEKYLL FROGMEN              |
| JEOPARDY ENCINO             |
| JEOPARDY ENCINO             |
| JEOPARDY ENCINO             |
| JERICHO MULAN               |
| JERICHO MULAN               |
| JERICHO MULAN               |
| JERK PAYCHECK               |
| JERK PAYCHECK               |
| JERK PAYCHECK               |
| JERK PAYCHECK               |
| JET NEIGHBORS               |
| JET NEIGHBORS               |
| JET NEIGHBORS               |
| JET NEIGHBORS               |
| JOON NORTHWEST              |
| JOON NORTHWEST              |
| JUGGLER HARDLY              |
| JUGGLER HARDLY              |
| JUGGLER HARDLY              |
| JUGGLER HARDLY              |
| JUMANJI BLADE               |
| JUMANJI BLADE               |
| JUMPING WRATH               |
| JUMPING WRATH               |
| JUNGLE CLOSER               |
| JUNGLE CLOSER               |
| KARATE MOON                 |
| KARATE MOON                 |
| KARATE MOON                 |
| KARATE MOON                 |
| KICK SAVANNAH               |
| KICK SAVANNAH               |
| KILLER INNOCENT             |
| KILLER INNOCENT             |
| KING EVOLUTION              |
| KING EVOLUTION              |
| KISS GLORY                  |
| KISS GLORY                  |
| KISS GLORY                  |
| KISS GLORY                  |
| KISSING DOLLS               |
| KISSING DOLLS               |
| KISSING DOLLS               |
| KNOCK WARLOCK               |
| KNOCK WARLOCK               |
| KNOCK WARLOCK               |
| KNOCK WARLOCK               |
| KRAMER CHOCOLATE            |
| KRAMER CHOCOLATE            |
| KRAMER CHOCOLATE            |
| KWAI HOMEWARD               |
| KWAI HOMEWARD               |
| KWAI HOMEWARD               |
| KWAI HOMEWARD               |
| LADY STAGE                  |
| LADY STAGE                  |
| LADY STAGE                  |
| LADY STAGE                  |
| LAWLESS VISION              |
| LAWLESS VISION              |
| LAWLESS VISION              |
| LAWLESS VISION              |
| LAWRENCE LOVE               |
| LAWRENCE LOVE               |
| LEAGUE HELLFIGHTERS         |
| LEAGUE HELLFIGHTERS         |
| LEBOWSKI SOLDIERS           |
| LEBOWSKI SOLDIERS           |
| LIAISONS SWEET              |
| LIAISONS SWEET              |
| LICENSE WEEKEND             |
| LICENSE WEEKEND             |
| LIES TREATMENT              |
| LIES TREATMENT              |
| LIES TREATMENT              |
| LIES TREATMENT              |
| LIGHTS DEER                 |
| LIGHTS DEER                 |
| LION UNCUT                  |
| LION UNCUT                  |
| LOATHING LEGALLY            |
| LOATHING LEGALLY            |
| LOATHING LEGALLY            |
| LOATHING LEGALLY            |
| LOLA AGENT                  |
| LOLA AGENT                  |
| LOLITA WORLD                |
| LOLITA WORLD                |
| LOLITA WORLD                |
| LONELY ELEPHANT             |
| LONELY ELEPHANT             |
| LONELY ELEPHANT             |
| LONELY ELEPHANT             |
| LORD ARIZONA                |
| LORD ARIZONA                |
| LORD ARIZONA                |
| LOSE INCH                   |
| LOSE INCH                   |
| LOSE INCH                   |
| LOSE INCH                   |
| LOST BIRD                   |
| LOST BIRD                   |
| LOST BIRD                   |
| LOUISIANA HARRY             |
| LOUISIANA HARRY             |
| LOVE SUICIDES               |
| LOVE SUICIDES               |
| LOVE SUICIDES               |
| LOVE SUICIDES               |
| LOVELY JINGLE               |
| LOVELY JINGLE               |
| LOVELY JINGLE               |
| LUCK OPUS                   |
| LUCK OPUS                   |
| LUCKY FLYING                |
| LUCKY FLYING                |
| LUCKY FLYING                |
| LUST LOCK                   |
| LUST LOCK                   |
| LUST LOCK                   |
| LUST LOCK                   |
| MADIGAN DORADO              |
| MADIGAN DORADO              |
| MADISON TRAP                |
| MADISON TRAP                |
| MADNESS ATTACKS             |
| MADNESS ATTACKS             |
| MADNESS ATTACKS             |
| MADNESS ATTACKS             |
| MAGNIFICENT CHITTY          |
| MAGNIFICENT CHITTY          |
| MAGNOLIA FORRESTER          |
| MAGNOLIA FORRESTER          |
| MAGUIRE APACHE              |
| MAGUIRE APACHE              |
| MAGUIRE APACHE              |
| MAIDEN HOME                 |
| MAIDEN HOME                 |
| MAIDEN HOME                 |
| MALKOVICH PET               |
| MALKOVICH PET               |
| MALKOVICH PET               |
| MALKOVICH PET               |
| MALLRATS UNITED             |
| MALLRATS UNITED             |
| MALLRATS UNITED             |
| MALTESE HOPE                |
| MALTESE HOPE                |
| MALTESE HOPE                |
| MANCHURIAN CURTAIN          |
| MANCHURIAN CURTAIN          |
| MARRIED GO                  |
| MARRIED GO                  |
| MARRIED GO                  |
| MARRIED GO                  |
| MARS ROMAN                  |
| MARS ROMAN                  |
| MARS ROMAN                  |
| MASK PEACH                  |
| MASK PEACH                  |
| MASK PEACH                  |
| MASK PEACH                  |
| MASKED BUBBLE               |
| MASKED BUBBLE               |
| MASKED BUBBLE               |
| MASKED BUBBLE               |
| MASSACRE USUAL              |
| MASSACRE USUAL              |
| MASSACRE USUAL              |
| MASSACRE USUAL              |
| MATRIX SNOWMAN              |
| MATRIX SNOWMAN              |
| MAUDE MOD                   |
| MAUDE MOD                   |
| MEET CHOCOLATE              |
| MEET CHOCOLATE              |
| MEMENTO ZOOLANDER           |
| MEMENTO ZOOLANDER           |
| MENAGERIE RUSHMORE          |
| MENAGERIE RUSHMORE          |
| MERMAID INSECTS             |
| MERMAID INSECTS             |
| METAL ARMAGEDDON            |
| METAL ARMAGEDDON            |
| METROPOLIS COMA             |
| METROPOLIS COMA             |
| METROPOLIS COMA             |
| METROPOLIS COMA             |
| MICROCOSMOS PARADISE        |
| MICROCOSMOS PARADISE        |
| MICROCOSMOS PARADISE        |
| MICROCOSMOS PARADISE        |
| MIDNIGHT WESTWARD           |
| MIDNIGHT WESTWARD           |
| MIDSUMMER GROUNDHOG         |
| MIDSUMMER GROUNDHOG         |
| MILE MULAN                  |
| MILE MULAN                  |
| MILE MULAN                  |
| MILLION ACE                 |
| MILLION ACE                 |
| MINDS TRUMAN                |
| MINDS TRUMAN                |
| MINDS TRUMAN                |
| MINDS TRUMAN                |
| MINE TITANS                 |
| MINE TITANS                 |
| MINE TITANS                 |
| MINE TITANS                 |
| MINORITY KISS               |
| MINORITY KISS               |
| MINORITY KISS               |
| MISSION ZOOLANDER           |
| MISSION ZOOLANDER           |
| MISSION ZOOLANDER           |
| MIXED DOORS                 |
| MIXED DOORS                 |
| MOCKINGBIRD HOLLYWOOD       |
| MOCKINGBIRD HOLLYWOOD       |
| MOCKINGBIRD HOLLYWOOD       |
| MOCKINGBIRD HOLLYWOOD       |
| MOD SECRETARY               |
| MOD SECRETARY               |
| MOD SECRETARY               |
| MONEY HAROLD                |
| MONEY HAROLD                |
| MONEY HAROLD                |
| MONSTER SPARTACUS           |
| MONSTER SPARTACUS           |
| MONTEZUMA COMMAND           |
| MONTEZUMA COMMAND           |
| MONTEZUMA COMMAND           |
| MOON BUNCH                  |
| MOON BUNCH                  |
| MOON BUNCH                  |
| MOON BUNCH                  |
| MOONSHINE CABIN             |
| MOONSHINE CABIN             |
| MOSQUITO ARMAGEDDON         |
| MOSQUITO ARMAGEDDON         |
| MOSQUITO ARMAGEDDON         |
| MOSQUITO ARMAGEDDON         |
| MOTHER OLEANDER             |
| MOTHER OLEANDER             |
| MOTHER OLEANDER             |
| MOTIONS DETAILS             |
| MOTIONS DETAILS             |
| MOULIN WAKE                 |
| MOULIN WAKE                 |
| MOULIN WAKE                 |
| MOURNING PURPLE             |
| MOURNING PURPLE             |
| MOVIE SHAKESPEARE           |
| MOVIE SHAKESPEARE           |
| MOVIE SHAKESPEARE           |
| MOVIE SHAKESPEARE           |
| MUMMY CREATURES             |
| MUMMY CREATURES             |
| MURDER ANTITRUST            |
| MURDER ANTITRUST            |
| MUSCLE BRIGHT               |
| MUSCLE BRIGHT               |
| MUSCLE BRIGHT               |
| MUSCLE BRIGHT               |
| MUSIC BOONDOCK              |
| MUSIC BOONDOCK              |
| MUSKETEERS WAIT             |
| MUSKETEERS WAIT             |
| MUSKETEERS WAIT             |
| MUSKETEERS WAIT             |
| MYSTIC TRUMAN               |
| MYSTIC TRUMAN               |
| NAME DETECTIVE              |
| NAME DETECTIVE              |
| NAME DETECTIVE              |
| NATIONAL STORY              |
| NATIONAL STORY              |
| NATURAL STOCK               |
| NATURAL STOCK               |
| NATURAL STOCK               |
| NEIGHBORS CHARADE           |
| NEIGHBORS CHARADE           |
| NEMO CAMPUS                 |
| NEMO CAMPUS                 |
| NETWORK PEAK                |
| NETWORK PEAK                |
| NETWORK PEAK                |
| NETWORK PEAK                |
| NEWTON LABYRINTH            |
| NEWTON LABYRINTH            |
| NIGHTMARE CHILL             |
| NIGHTMARE CHILL             |
| NIGHTMARE CHILL             |
| NONE SPIKING                |
| NONE SPIKING                |
| NONE SPIKING                |
| NORTHWEST POLISH            |
| NORTHWEST POLISH            |
| NORTHWEST POLISH            |
| NOVOCAINE FLIGHT            |
| NOVOCAINE FLIGHT            |
| NOVOCAINE FLIGHT            |
| NUTS TIES                   |
| NUTS TIES                   |
| NUTS TIES                   |
| OLEANDER CLUE               |
| OLEANDER CLUE               |
| OLEANDER CLUE               |
| OPEN AFRICAN                |
| OPEN AFRICAN                |
| OPERATION OPERATION         |
| OPERATION OPERATION         |
| OPERATION OPERATION         |
| OPERATION OPERATION         |
| ORANGE GRAPES               |
| ORANGE GRAPES               |
| ORANGE GRAPES               |
| ORIENT CLOSER               |
| ORIENT CLOSER               |
| ORIENT CLOSER               |
| OSCAR GOLD                  |
| OSCAR GOLD                  |
| OSCAR GOLD                  |
| OTHERS SOUP                 |
| OTHERS SOUP                 |
| OTHERS SOUP                 |
| OUTBREAK DIVINE             |
| OUTBREAK DIVINE             |
| OUTBREAK DIVINE             |
| OUTFIELD MASSACRE           |
| OUTFIELD MASSACRE           |
| OUTFIELD MASSACRE           |
| OUTLAW HANKY                |
| OUTLAW HANKY                |
| OUTLAW HANKY                |
| OUTLAW HANKY                |
| OZ LIAISONS                 |
| OZ LIAISONS                 |
| PACIFIC AMISTAD             |
| PACIFIC AMISTAD             |
| PACKER MADIGAN              |
| PACKER MADIGAN              |
| PAJAMA JAWBREAKER           |
| PAJAMA JAWBREAKER           |
| PAJAMA JAWBREAKER           |
| PAJAMA JAWBREAKER           |
| PANIC CLUB                  |
| PANIC CLUB                  |
| PANKY SUBMARINE             |
| PANKY SUBMARINE             |
| PANTHER REDS                |
| PANTHER REDS                |
| PANTHER REDS                |
| PARADISE SABRINA            |
| PARADISE SABRINA            |
| PARADISE SABRINA            |
| PARADISE SABRINA            |
| PARTY KNOCK                 |
| PARTY KNOCK                 |
| PAST SUICIDES               |
| PAST SUICIDES               |
| PAST SUICIDES               |
| PAST SUICIDES               |
| PATHS CONTROL               |
| PATHS CONTROL               |
| PATIENT SISTER              |
| PATIENT SISTER              |
| PATIENT SISTER              |
| PATRIOT ROMAN               |
| PATRIOT ROMAN               |
| PATTON INTERVIEW            |
| PATTON INTERVIEW            |
| PATTON INTERVIEW            |
| PATTON INTERVIEW            |
| PAYCHECK WAIT               |
| PAYCHECK WAIT               |
| PAYCHECK WAIT               |
| PEACH INNOCENT              |
| PEACH INNOCENT              |
| PEAK FOREVER                |
| PEAK FOREVER                |
| PELICAN COMFORTS            |
| PELICAN COMFORTS            |
| PELICAN COMFORTS            |
| PELICAN COMFORTS            |
| PERFECT GROOVE              |
| PERFECT GROOVE              |
| PERSONAL LADYBUGS           |
| PERSONAL LADYBUGS           |
| PET HAUNTING                |
| PET HAUNTING                |
| PET HAUNTING                |
| PHANTOM GLORY               |
| PHANTOM GLORY               |
| PHILADELPHIA WIFE           |
| PHILADELPHIA WIFE           |
| PIANIST OUTFIELD            |
| PIANIST OUTFIELD            |
| PIANIST OUTFIELD            |
| PICKUP DRIVING              |
| PICKUP DRIVING              |
| PICKUP DRIVING              |
| PICKUP DRIVING              |
| PILOT HOOSIERS              |
| PILOT HOOSIERS              |
| PINOCCHIO SIMON             |
| PINOCCHIO SIMON             |
| PIRATES ROXANNE             |
| PIRATES ROXANNE             |
| PIRATES ROXANNE             |
| PITTSBURGH HUNCHBACK        |
| PITTSBURGH HUNCHBACK        |
| PITTSBURGH HUNCHBACK        |
| PITY BOUND                  |
| PITY BOUND                  |
| PITY BOUND                  |
| PITY BOUND                  |
| PLUTO OLEANDER              |
| PLUTO OLEANDER              |
| PLUTO OLEANDER              |
| PLUTO OLEANDER              |
| POCUS PULP                  |
| POCUS PULP                  |
| POCUS PULP                  |
| POLLOCK DELIVERANCE         |
| POLLOCK DELIVERANCE         |
| POLLOCK DELIVERANCE         |
| POLLOCK DELIVERANCE         |
| POND SEATTLE                |
| POND SEATTLE                |
| POND SEATTLE                |
| POND SEATTLE                |
| POSEIDON FOREVER            |
| POSEIDON FOREVER            |
| POSEIDON FOREVER            |
| POTTER CONNECTICUT          |
| POTTER CONNECTICUT          |
| PREJUDICE OLEANDER          |
| PREJUDICE OLEANDER          |
| PREJUDICE OLEANDER          |
| PREJUDICE OLEANDER          |
| PRESIDENT BANG              |
| PRESIDENT BANG              |
| PRIDE ALAMO                 |
| PRIDE ALAMO                 |
| PRIMARY GLASS               |
| PRIMARY GLASS               |
| PRIMARY GLASS               |
| PRIMARY GLASS               |
| PRINCESS GIANT              |
| PRINCESS GIANT              |
| PRINCESS GIANT              |
| PRINCESS GIANT              |
| PRIVATE DROP                |
| PRIVATE DROP                |
| PULP BEVERLY                |
| PULP BEVERLY                |
| PULP BEVERLY                |
| PULP BEVERLY                |
| PURE RUNNER                 |
| PURE RUNNER                 |
| PURPLE MOVIE                |
| PURPLE MOVIE                |
| PURPLE MOVIE                |
| PURPLE MOVIE                |
| QUEEN LUKE                  |
| QUEEN LUKE                  |
| QUEST MUSSOLINI             |
| QUEST MUSSOLINI             |
| QUILLS BULL                 |
| QUILLS BULL                 |
| RACER EGG                   |
| RACER EGG                   |
| RAGE GAMES                  |
| RAGE GAMES                  |
| RAGE GAMES                  |
| RAGE GAMES                  |
| RANGE MOONWALKER            |
| RANGE MOONWALKER            |
| RANGE MOONWALKER            |
| RANGE MOONWALKER            |
| REAP UNFAITHFUL             |
| REAP UNFAITHFUL             |
| REAR TRADING                |
| REAR TRADING                |
| RECORDS ZORRO               |
| RECORDS ZORRO               |
| REDEMPTION COMFORTS         |
| REDEMPTION COMFORTS         |
| REDEMPTION COMFORTS         |
| REDS POCUS                  |
| REDS POCUS                  |
| REEF SALUTE                 |
| REEF SALUTE                 |
| REIGN GENTLEMEN             |
| REIGN GENTLEMEN             |
| REIGN GENTLEMEN             |
| REIGN GENTLEMEN             |
| REMEMBER DIARY              |
| REMEMBER DIARY              |
| REQUIEM TYCOON              |
| REQUIEM TYCOON              |
| REQUIEM TYCOON              |
| RESURRECTION SILVERADO      |
| RESURRECTION SILVERADO      |
| REUNION WITCHES             |
| REUNION WITCHES             |
| REUNION WITCHES             |
| RIDGEMONT SUBMARINE         |
| RIDGEMONT SUBMARINE         |
| RIDGEMONT SUBMARINE         |
| RIDGEMONT SUBMARINE         |
| RINGS HEARTBREAKERS         |
| RINGS HEARTBREAKERS         |
| RINGS HEARTBREAKERS         |
| RINGS HEARTBREAKERS         |
| RIVER OUTLAW                |
| RIVER OUTLAW                |
| RIVER OUTLAW                |
| RIVER OUTLAW                |
| ROAD ROXANNE                |
| ROAD ROXANNE                |
| ROBBERS JOON                |
| ROBBERS JOON                |
| ROBBERS JOON                |
| ROBBERY BRIGHT              |
| ROBBERY BRIGHT              |
| ROBBERY BRIGHT              |
| ROBBERY BRIGHT              |
| ROCK INSTINCT               |
| ROCK INSTINCT               |
| ROCKETEER MOTHER            |
| ROCKETEER MOTHER            |
| ROCKETEER MOTHER            |
| ROCKETEER MOTHER            |
| ROCKY WAR                   |
| ROCKY WAR                   |
| ROMAN PUNK                  |
| ROMAN PUNK                  |
| ROMAN PUNK                  |
| ROMAN PUNK                  |
| ROOM ROMAN                  |
| ROOM ROMAN                  |
| ROOTS REMEMBER              |
| ROOTS REMEMBER              |
| ROSES TREASURE              |
| ROSES TREASURE              |
| ROSES TREASURE              |
| ROSES TREASURE              |
| ROUGE SQUAD                 |
| ROUGE SQUAD                 |
| ROXANNE REBEL               |
| ROXANNE REBEL               |
| RUGRATS SHAKESPEARE         |
| RUGRATS SHAKESPEARE         |
| RUGRATS SHAKESPEARE         |
| RUGRATS SHAKESPEARE         |
| RULES HUMAN                 |
| RULES HUMAN                 |
| RUN PACIFIC                 |
| RUN PACIFIC                 |
| RUN PACIFIC                 |
| RUSH GOODFELLAS             |
| RUSH GOODFELLAS             |
| RUSH GOODFELLAS             |
| RUSH GOODFELLAS             |
| SABRINA MIDNIGHT            |
| SABRINA MIDNIGHT            |
| SABRINA MIDNIGHT            |
| SABRINA MIDNIGHT            |
| SAGEBRUSH CLUELESS          |
| SAGEBRUSH CLUELESS          |
| SAGEBRUSH CLUELESS          |
| SALUTE APOLLO               |
| SALUTE APOLLO               |
| SAMURAI LION                |
| SAMURAI LION                |
| SAMURAI LION                |
| SATISFACTION CONFIDENTIAL   |
| SATISFACTION CONFIDENTIAL   |
| SATISFACTION CONFIDENTIAL   |
| SATURDAY LAMBS              |
| SATURDAY LAMBS              |
| SATURDAY LAMBS              |
| SATURDAY LAMBS              |
| SATURN NAME                 |
| SATURN NAME                 |
| SATURN NAME                 |
| SATURN NAME                 |
| SAVANNAH TOWN               |
| SAVANNAH TOWN               |
| SAVANNAH TOWN               |
| SCALAWAG DUCK               |
| SCALAWAG DUCK               |
| SCALAWAG DUCK               |
| SCALAWAG DUCK               |
| SCARFACE BANG               |
| SCARFACE BANG               |
| SCARFACE BANG               |
| SCORPION APOLLO             |
| SCORPION APOLLO             |
| SCORPION APOLLO             |
| SEA VIRGIN                  |
| SEA VIRGIN                  |
| SEA VIRGIN                  |
| SEA VIRGIN                  |
| SEABISCUIT PUNK             |
| SEABISCUIT PUNK             |
| SEABISCUIT PUNK             |
| SEABISCUIT PUNK             |
| SEARCHERS WAIT              |
| SEARCHERS WAIT              |
| SEARCHERS WAIT              |
| SEARCHERS WAIT              |
| SEATTLE EXPECATIONS         |
| SEATTLE EXPECATIONS         |
| SEATTLE EXPECATIONS         |
| SECRET GROUNDHOG            |
| SECRET GROUNDHOG            |
| SECRETARY ROUGE             |
| SECRETARY ROUGE             |
| SECRETARY ROUGE             |
| SECRETS PARADISE            |
| SECRETS PARADISE            |
| SECRETS PARADISE            |
| SECRETS PARADISE            |
| SHAKESPEARE SADDLE          |
| SHAKESPEARE SADDLE          |
| SHAKESPEARE SADDLE          |
| SHANE DARKNESS              |
| SHANE DARKNESS              |
| SHANE DARKNESS              |
| SHANE DARKNESS              |
| SHANGHAI TYCOON             |
| SHANGHAI TYCOON             |
| SHANGHAI TYCOON             |
| SHAWSHANK BUBBLE            |
| SHAWSHANK BUBBLE            |
| SHAWSHANK BUBBLE            |
| SHAWSHANK BUBBLE            |
| SHEPHERD MIDSUMMER          |
| SHEPHERD MIDSUMMER          |
| SHEPHERD MIDSUMMER          |
| SHINING ROSES               |
| SHINING ROSES               |
| SHINING ROSES               |
| SHIP WONDERLAND             |
| SHIP WONDERLAND             |
| SHOCK CABIN                 |
| SHOCK CABIN                 |
| SHOCK CABIN                 |
| SHOCK CABIN                 |
| SHOOTIST SUPERFLY           |
| SHOOTIST SUPERFLY           |
| SHOOTIST SUPERFLY           |
| SHOOTIST SUPERFLY           |
| SHOW LORD                   |
| SHOW LORD                   |
| SHRUNK DIVINE               |
| SHRUNK DIVINE               |
| SHRUNK DIVINE               |
| SHRUNK DIVINE               |
| SIDE ARK                    |
| SIDE ARK                    |
| SIEGE MADRE                 |
| SIEGE MADRE                 |
| SIEGE MADRE                 |
| SIEGE MADRE                 |
| SIERRA DIVIDE               |
| SIERRA DIVIDE               |
| SILENCE KANE                |
| SILENCE KANE                |
| SILVERADO GOLDFINGER        |
| SILVERADO GOLDFINGER        |
| SIMON NORTH                 |
| SIMON NORTH                 |
| SINNERS ATLANTIS            |
| SINNERS ATLANTIS            |
| SLACKER LIAISONS            |
| SLACKER LIAISONS            |
| SLACKER LIAISONS            |
| SLACKER LIAISONS            |
| SLEEPING SUSPECTS           |
| SLEEPING SUSPECTS           |
| SLEEPING SUSPECTS           |
| SLEEPING SUSPECTS           |
| SLEEPLESS MONSOON           |
| SLEEPLESS MONSOON           |
| SLEEPY JAPANESE             |
| SLEEPY JAPANESE             |
| SLEEPY JAPANESE             |
| SLEUTH ORIENT               |
| SLEUTH ORIENT               |
| SLEUTH ORIENT               |
| SLUMS DUCK                  |
| SLUMS DUCK                  |
| SLUMS DUCK                  |
| SLUMS DUCK                  |
| SMILE EARRING               |
| SMILE EARRING               |
| SMILE EARRING               |
| SMOKING BARBARELLA          |
| SMOKING BARBARELLA          |
| SMOKING BARBARELLA          |
| SNATCH SLIPPER              |
| SNATCH SLIPPER              |
| SNATCH SLIPPER              |
| SNATCHERS MONTEZUMA         |
| SNATCHERS MONTEZUMA         |
| SNATCHERS MONTEZUMA         |
| SNOWMAN ROLLERCOASTER       |
| SNOWMAN ROLLERCOASTER       |
| SNOWMAN ROLLERCOASTER       |
| SNOWMAN ROLLERCOASTER       |
| SOLDIERS EVOLUTION          |
| SOLDIERS EVOLUTION          |
| SOMETHING DUCK              |
| SOMETHING DUCK              |
| SOMETHING DUCK              |
| SONG HEDWIG                 |
| SONG HEDWIG                 |
| SONG HEDWIG                 |
| SONS INTERVIEW              |
| SONS INTERVIEW              |
| SONS INTERVIEW              |
| SONS INTERVIEW              |
| SOUTH WAIT                  |
| SOUTH WAIT                  |
| SOUTH WAIT                  |
| SPEAKEASY DATE              |
| SPEAKEASY DATE              |
| SPEAKEASY DATE              |
| SPICE SORORITY              |
| SPICE SORORITY              |
| SPINAL ROCKY                |
| SPINAL ROCKY                |
| SPIRITED CASUALTIES         |
| SPIRITED CASUALTIES         |
| SPIRITED CASUALTIES         |
| SPLASH GUMP                 |
| SPLASH GUMP                 |
| SPLASH GUMP                 |
| SPLASH GUMP                 |
| SPLENDOR PATTON             |
| SPLENDOR PATTON             |
| SPLENDOR PATTON             |
| SPY MILE                    |
| SPY MILE                    |
| SPY MILE                    |
| SPY MILE                    |
| SQUAD FISH                  |
| SQUAD FISH                  |
| SQUAD FISH                  |
| STAGECOACH ARMAGEDDON       |
| STAGECOACH ARMAGEDDON       |
| STAMPEDE DISTURBING         |
| STAMPEDE DISTURBING         |
| STAMPEDE DISTURBING         |
| STAMPEDE DISTURBING         |
| STAR OPERATION              |
| STAR OPERATION              |
| STAR OPERATION              |
| STATE WASTELAND             |
| STATE WASTELAND             |
| STEEL SANTA                 |
| STEEL SANTA                 |
| STEEL SANTA                 |
| STEEL SANTA                 |
| STEERS ARMAGEDDON           |
| STEERS ARMAGEDDON           |
| STEPMOM DREAM               |
| STEPMOM DREAM               |
| STEPMOM DREAM               |
| STEPMOM DREAM               |
| STING PERSONAL              |
| STING PERSONAL              |
| STING PERSONAL              |
| STING PERSONAL              |
| STONE FIRE                  |
| STONE FIRE                  |
| STONE FIRE                  |
| STORM HAPPINESS             |
| STORM HAPPINESS             |
| STORM HAPPINESS             |
| STORM HAPPINESS             |
| STORY SIDE                  |
| STORY SIDE                  |
| STORY SIDE                  |
| STRAIGHT HOURS              |
| STRAIGHT HOURS              |
| STRAIGHT HOURS              |
| STRANGELOVE DESIRE          |
| STRANGELOVE DESIRE          |
| STRANGELOVE DESIRE          |
| STRANGELOVE DESIRE          |
| STRANGER STRANGERS          |
| STRANGER STRANGERS          |
| STRANGER STRANGERS          |
| STREAK RIDGEMONT            |
| STREAK RIDGEMONT            |
| STREETCAR INTENTIONS        |
| STREETCAR INTENTIONS        |
| STREETCAR INTENTIONS        |
| STREETCAR INTENTIONS        |
| STRICTLY SCARFACE           |
| STRICTLY SCARFACE           |
| STRICTLY SCARFACE           |
| SUGAR WONKA                 |
| SUGAR WONKA                 |
| SUGAR WONKA                 |
| SUIT WALLS                  |
| SUIT WALLS                  |
| SUIT WALLS                  |
| SUMMER SCARFACE             |
| SUMMER SCARFACE             |
| SUMMER SCARFACE             |
| SUN CONFESSIONS             |
| SUN CONFESSIONS             |
| SUN CONFESSIONS             |
| SUN CONFESSIONS             |
| SUNDANCE INVASION           |
| SUNDANCE INVASION           |
| SUNDANCE INVASION           |
| SUNDANCE INVASION           |
| SUNRISE LEAGUE              |
| SUNRISE LEAGUE              |
| SUNRISE LEAGUE              |
| SUNRISE LEAGUE              |
| SUPER WYOMING               |
| SUPER WYOMING               |
| SUPER WYOMING               |
| SUPER WYOMING               |
| SUPERFLY TRIP               |
| SUPERFLY TRIP               |
| SUPERFLY TRIP               |
| SUSPECTS QUILLS             |
| SUSPECTS QUILLS             |
| SUSPECTS QUILLS             |
| SUSPECTS QUILLS             |
| SWARM GOLD                  |
| SWARM GOLD                  |
| SWARM GOLD                  |
| SWARM GOLD                  |
| SWEDEN SHINING              |
| SWEDEN SHINING              |
| SWEETHEARTS SUSPECTS        |
| SWEETHEARTS SUSPECTS        |
| SWEETHEARTS SUSPECTS        |
| SWEETHEARTS SUSPECTS        |
| TALENTED HOMICIDE           |
| TALENTED HOMICIDE           |
| TALENTED HOMICIDE           |
| TARZAN VIDEOTAPE            |
| TARZAN VIDEOTAPE            |
| TAXI KICK                   |
| TAXI KICK                   |
| TAXI KICK                   |
| TELEGRAPH VOYAGE            |
| TELEGRAPH VOYAGE            |
| TELEGRAPH VOYAGE            |
| TELEGRAPH VOYAGE            |
| TELEMARK HEARTBREAKERS      |
| TELEMARK HEARTBREAKERS      |
| TELEMARK HEARTBREAKERS      |
| TELEMARK HEARTBREAKERS      |
| TENENBAUMS COMMAND          |
| TENENBAUMS COMMAND          |
| TENENBAUMS COMMAND          |
| TENENBAUMS COMMAND          |
| TEXAS WATCH                 |
| TEXAS WATCH                 |
| THEORY MERMAID              |
| THEORY MERMAID              |
| THEORY MERMAID              |
| THEORY MERMAID              |
| THIEF PELICAN               |
| THIEF PELICAN               |
| THIEF PELICAN               |
| THIEF PELICAN               |
| THIN SAGEBRUSH              |
| THIN SAGEBRUSH              |
| THIN SAGEBRUSH              |
| THIN SAGEBRUSH              |
| TIES HUNGER                 |
| TIES HUNGER                 |
| TIES HUNGER                 |
| TIGHTS DAWN                 |
| TIGHTS DAWN                 |
| TIGHTS DAWN                 |
| TIMBERLAND SKY              |
| TIMBERLAND SKY              |
| TIMBERLAND SKY              |
| TITANIC BOONDOCK            |
| TITANIC BOONDOCK            |
| TITANIC BOONDOCK            |
| TITANS JERK                 |
| TITANS JERK                 |
| TITANS JERK                 |
| TITANS JERK                 |
| TOMATOES HELLFIGHTERS       |
| TOMATOES HELLFIGHTERS       |
| TOMATOES HELLFIGHTERS       |
| TOMORROW HUSTLER            |
| TOMORROW HUSTLER            |
| TOMORROW HUSTLER            |
| TOMORROW HUSTLER            |
| TOOTSIE PILOT               |
| TOOTSIE PILOT               |
| TORQUE BOUND                |
| TORQUE BOUND                |
| TORQUE BOUND                |
| TORQUE BOUND                |
| TOURIST PELICAN             |
| TOURIST PELICAN             |
| TOURIST PELICAN             |
| TOWERS HURRICANE            |
| TOWERS HURRICANE            |
| TOWERS HURRICANE            |
| TOWN ARK                    |
| TOWN ARK                    |
| TRACY CIDER                 |
| TRACY CIDER                 |
| TRACY CIDER                 |
| TRACY CIDER                 |
| TRADING PINOCCHIO           |
| TRADING PINOCCHIO           |
| TRADING PINOCCHIO           |
| TRADING PINOCCHIO           |
| TRAIN BUNCH                 |
| TRAIN BUNCH                 |
| TRAINSPOTTING STRANGERS     |
| TRAINSPOTTING STRANGERS     |
| TRAINSPOTTING STRANGERS     |
| TRAMP OTHERS                |
| TRAMP OTHERS                |
| TRANSLATION SUMMER          |
| TRANSLATION SUMMER          |
| TRANSLATION SUMMER          |
| TRANSLATION SUMMER          |
| TRAP GUYS                   |
| TRAP GUYS                   |
| TRIP NEWTON                 |
| TRIP NEWTON                 |
| TRIP NEWTON                 |
| TRIP NEWTON                 |
| TROJAN TOMORROW             |
| TROJAN TOMORROW             |
| TROJAN TOMORROW             |
| TROOPERS METAL              |
| TROOPERS METAL              |
| TROOPERS METAL              |
| TROOPERS METAL              |
| TROUBLE DATE                |
| TROUBLE DATE                |
| TRUMAN CRAZY                |
| TRUMAN CRAZY                |
| TRUMAN CRAZY                |
| TRUMAN CRAZY                |
| TURN STAR                   |
| TURN STAR                   |
| TUXEDO MILE                 |
| TUXEDO MILE                 |
| TUXEDO MILE                 |
| TYCOON GATHERING            |
| TYCOON GATHERING            |
| TYCOON GATHERING            |
| TYCOON GATHERING            |
| UNBREAKABLE KARATE          |
| UNBREAKABLE KARATE          |
| UNBREAKABLE KARATE          |
| UNCUT SUICIDES              |
| UNCUT SUICIDES              |
| UNDEFEATED DALMATIONS       |
| UNDEFEATED DALMATIONS       |
| UNDEFEATED DALMATIONS       |
| UNFORGIVEN ZOOLANDER        |
| UNFORGIVEN ZOOLANDER        |
| UNITED PILOT                |
| UNITED PILOT                |
| UNITED PILOT                |
| UPRISING UPTOWN             |
| UPRISING UPTOWN             |
| UPRISING UPTOWN             |
| UPRISING UPTOWN             |
| UPTOWN YOUNG                |
| UPTOWN YOUNG                |
| UPTOWN YOUNG                |
| USUAL UNTOUCHABLES          |
| USUAL UNTOUCHABLES          |
| USUAL UNTOUCHABLES          |
| USUAL UNTOUCHABLES          |
| VACATION BOONDOCK           |
| VACATION BOONDOCK           |
| VACATION BOONDOCK           |
| VALLEY PACKER               |
| VALLEY PACKER               |
| VAMPIRE WHALE               |
| VAMPIRE WHALE               |
| VAMPIRE WHALE               |
| VANISHING ROCKY             |
| VANISHING ROCKY             |
| VARSITY TRIP                |
| VARSITY TRIP                |
| VELVET TERMINATOR           |
| VELVET TERMINATOR           |
| VELVET TERMINATOR           |
| VELVET TERMINATOR           |
| VICTORY ACADEMY             |
| VICTORY ACADEMY             |
| VICTORY ACADEMY             |
```

Listar los nombres y apellidos de los empleados junto con las
direcciones de los almacenes en los que trabajan.

```sql

 SELECT e.nombre AS empleado_nombre, e.apellidos AS empleado_apellido, d.direccion 	AS almacen_direccion
 FROM empleado e
 JOIN almacen a ON e.id_almacen = a.id_almacen
 JOIN direccion d ON a.id_direccion = d.id_direccion;

+-----------------+-------------------+--------------------+
| empleado_nombre | empleado_apellido | almacen_direccion  |
+-----------------+-------------------+--------------------+
| Ada             | Byron             | 47 MySakila Drive  |
| Ringo           | Rooksby           | 47 MySakila Drive  |
| Mike            | Hillyer           | 28 MySQL Boulevard |
| Jon             | Stephens          | 28 MySQL Boulevard |
| Pepe            | Spilberg          | 28 MySQL Boulevard |
+-----------------+-------------------+--------------------+
```

Obtener una lista de pagos realizados, incluyendo el cliente, el
empleado que registró el pago y el alquiler correspondiente.

```sql
    SELECT p.id_pago, p.total, p.fecha_pago, c.nombre AS cliente_nombre, c.apellidos AS cliente_apellido, e.nombre AS empleado_nombre, e.apellidos AS empleado_apellido, r.id_alquiler
    FROM pago p
    JOIN cliente c ON p.id_cliente = c.id_cliente
    JOIN empleado e ON p.id_empleado = e.id_empleado
    LEFT JOIN alquiler r ON p.id_alquiler = r.id_alquiler;
    
     ke            | Hillyer           |        8965 |
|   16041 |  2.99 | 2005-07-31 04:57:07 | AUSTIN         | CINTRON          | Jon             | Stephens          |        9630 |
|   16042 |  2.99 | 2005-07-31 06:41:19 | AUSTIN         | CINTRON          | Jon             | Stephens          |        9679 |
|   16043 |  3.99 | 2005-08-17 00:05:05 | AUSTIN         | CINTRON          | Jon             | Stephens          |       11522 |
|   16044 |  1.99 | 2005-08-21 05:07:08 | AUSTIN         | CINTRON          | Mike            | Hillyer           |       14233 |
|   16045 |  4.99 | 2005-08-21 17:43:42 | AUSTIN         | CINTRON          | Mike            | Hillyer           |       14599 |
|   16046 |  1.99 | 2005-08-21 21:41:57 | AUSTIN         | CINTRON          | Mike            | Hillyer           |       14719 |
|   16047 |  8.99 | 2005-08-23 06:09:44 | AUSTIN         | CINTRON          | Jon             | Stephens          |       15590 |
|   16048 |  2.99 | 2005-08-23 11:08:46 | AUSTIN         | CINTRON          | Jon             | Stephens          |       15719 |
|   16049 |  2.99 | 2005-08-23 11:25:00 | AUSTIN         | CINTRON          | Jon             | Stephens          |       15725 |
+---------+-------+---------------------+----------------+------------------+-----------------+-------------------+-------------+
16049 rows in set (0,04 sec)
```

Listar las películas y los idiomas en los que están disponibles.

```sql
    SELECT p.titulo AS pelicula_titulo, l.nombre AS idioma_nombre
    FROM pelicula p
    JOIN idioma l ON p.id_idioma = l.id_idioma;
    
+-----------------------------+---------------+
| pelicula_titulo             | idioma_nombre |
+-----------------------------+---------------+
| ACADEMY DINOSAUR            | English       |
| ACE GOLDFINGER              | English       |
| ADAPTATION HOLES            | English       |
| AFFAIR PREJUDICE            | English       |
| AFRICAN EGG                 | English       |
| AGENT TRUMAN                | English       |
| AIRPLANE SIERRA             | English       |
| AIRPORT POLLOCK             | English       |
| ALABAMA DEVIL               | English       |
| ALADDIN CALENDAR            | English       |
| ALAMO VIDEOTAPE             | English       |
| ALASKA PHANTOM              | English       |
| ALI FOREVER                 | English       |
| ALICE FANTASIA              | English       |
| ALIEN CENTER                | English       |
| ALLEY EVOLUTION             | English       |
| ALONE TRIP                  | English       |
| ALTER VICTORY               | English       |
| AMADEUS HOLY                | English       |
| AMELIE HELLFIGHTERS         | English       |
| AMERICAN CIRCUS             | English       |
| AMISTAD MIDSUMMER           | English       |
| ANACONDA CONFESSIONS        | English       |
| ANALYZE HOOSIERS            | English       |
| ANGELS LIFE                 | English       |
| ANNIE IDENTITY              | English       |
| ANONYMOUS HUMAN             | English       |
| ANTHEM LUKE                 | English       |
| ANTITRUST TOMATOES          | English       |
| ANYTHING SAVANNAH           | English       |
| APACHE DIVINE               | English       |
| APOCALYPSE FLAMINGOS        | English       |
| APOLLO TEEN                 | English       |
| ARABIA DOGMA                | English       |
| ARACHNOPHOBIA ROLLERCOASTER | English       |
| ARGONAUTS TOWN              | English       |
| ARIZONA BANG                | English       |
| ARK RIDGEMONT               | English       |
| ARMAGEDDON LOST             | English       |
| ARMY FLINTSTONES            | English       |
| ARSENIC INDEPENDENCE        | English       |
| ARTIST COLDBLOODED          | English       |
| ATLANTIS CAUSE              | English       |
| ATTACKS HATE                | English       |
| ATTRACTION NEWTON           | English       |
| AUTUMN CROW                 | English       |
| BABY HALL                   | English       |
| BACKLASH UNDEFEATED         | English       |
| BADMAN DAWN                 | English       |
| BAKED CLEOPATRA             | English       |
| BALLOON HOMEWARD            | English       |
| BALLROOM MOCKINGBIRD        | English       |
| BANG KWAI                   | English       |
| BANGER PINOCCHIO            | English       |
| BARBARELLA STREETCAR        | English       |
| BAREFOOT MANCHURIAN         | English       |
| BASIC EASY                  | English       |
| BEACH HEARTBREAKERS         | English       |
| BEAR GRACELAND              | English       |
| BEAST HUNCHBACK             | English       |
| BEAUTY GREASE               | English       |
| BED HIGHBALL                | English       |
| BEDAZZLED MARRIED           | English       |
| BEETHOVEN EXORCIST          | English       |
| BEHAVIOR RUNAWAY            | English       |
| BENEATH RUSH                | English       |
| BERETS AGENT                | English       |
| BETRAYED REAR               | English       |
| BEVERLY OUTLAW              | English       |
| BIKINI BORROWERS            | English       |
| BILKO ANONYMOUS             | English       |
| BILL OTHERS                 | English       |
| BINGO TALENTED              | English       |
| BIRCH ANTITRUST             | English       |
| BIRD INDEPENDENCE           | English       |
| BIRDCAGE CASPER             | English       |
| BIRDS PERDITION             | English       |
| BLACKOUT PRIVATE            | English       |
| BLADE POLISH                | English       |
| BLANKET BEVERLY             | English       |
| BLINDNESS GUN               | English       |
| BLOOD ARGONAUTS             | English       |
| BLUES INSTINCT              | English       |
| BOILED DARES                | English       |
| BONNIE HOLOCAUST            | English       |
| BOOGIE AMELIE               | English       |
| BOONDOCK BALLROOM           | English       |
| BORN SPINAL                 | English       |
| BORROWERS BEDAZZLED         | English       |
| BOULEVARD MOB               | English       |
| BOUND CHEAPER               | English       |
| BOWFINGER GABLES            | English       |
| BRANNIGAN SUNRISE           | English       |
| BRAVEHEART HUMAN            | English       |
| BREAKFAST GOLDFINGER        | English       |
| BREAKING HOME               | English       |
| BRIDE INTRIGUE              | English       |
| BRIGHT ENCOUNTERS           | English       |
| BRINGING HYSTERICAL         | English       |
| BROOKLYN DESERT             | English       |
| BROTHERHOOD BLANKET         | English       |
| BUBBLE GROSSE               | English       |
| BUCKET BROTHERHOOD          | English       |
| BUGSY SONG                  | English       |
| BULL SHAWSHANK              | English       |
| BULWORTH COMMANDMENTS       | English       |
| BUNCH MINDS                 | English       |
| BUTCH PANTHER               | English       |
| BUTTERFLY CHOCOLAT          | English       |
| CABIN FLASH                 | English       |
| CADDYSHACK JEDI             | English       |
| CALENDAR GUNFIGHT           | English       |
| CALIFORNIA BIRDS            | English       |
| CAMELOT VACATION            | English       |
| CAMPUS REMEMBER             | English       |
| CANDIDATE PERDITION         | English       |
| CANDLES GRAPES              | English       |
| CANYON STOCK                | English       |
| CAPER MOTIONS               | English       |
| CARIBBEAN LIBERTY           | English       |
| CAROL TEXAS                 | English       |
| CARRIE BUNCH                | English       |
| CASABLANCA SUPER            | English       |
| CASPER DRAGONFLY            | English       |
| CASSIDY WYOMING             | English       |
| CASUALTIES ENCINO           | English       |
| CAT CONEHEADS               | English       |
| CATCH AMISTAD               | English       |
| CAUSE DATE                  | English       |
| CELEBRITY HORN              | English       |
| CENTER DINOSAUR             | English       |
| CHAINSAW UPTOWN             | English       |
| CHAMBER ITALIAN             | English       |
| CHAMPION FLATLINERS         | English       |
| CHANCE RESURRECTION         | English       |
| CHAPLIN LICENSE             | English       |
| CHARADE DUFFEL              | English       |
| CHARIOTS CONSPIRACY         | English       |
| CHASING FIGHT               | English       |
| CHEAPER CLYDE               | English       |
| CHICAGO NORTH               | English       |
| CHICKEN HELLFIGHTERS        | English       |
| CHILL LUCK                  | English       |
| CHINATOWN GLADIATOR         | English       |
| CHISUM BEHAVIOR             | English       |
| CHITTY LOCK                 | English       |
| CHOCOLAT HARRY              | English       |
| CHOCOLATE DUCK              | English       |
| CHRISTMAS MOONSHINE         | English       |
| CIDER DESIRE                | English       |
| CINCINATTI WHISPERER        | English       |
| CIRCUS YOUTH                | English       |
| CITIZEN SHREK               | English       |
| CLASH FREDDY                | English       |
| CLEOPATRA DEVIL             | English       |
| CLERKS ANGELS               | English       |
| CLOCKWORK PARADISE          | English       |
| CLONES PINOCCHIO            | English       |
| CLOSER BANG                 | English       |
```

Encontrar todos los empleados y los almacenes que gestionan.

```sql
    SELECT e.nombre AS empleado_nombre, e.apellidos AS empleado_apellido, a.id_almacen AS almacen_id
    FROM empleado e
    JOIN almacen a ON e.id_empleado = a.id_empleado_jefe;
    
+-----------------+-------------------+------------+
| empleado_nombre | empleado_apellido | almacen_id |
+-----------------+-------------------+------------+
| Jon             | Stephens          |          2 |
| Ringo           | Rooksby           |          1 |
+-----------------+-------------------+------------+
```

Obtener los títulos de las películas que nunca han sido
alquiladas.

```sql
    SELECT p.titulo 
    FROM pelicula p
    LEFT JOIN inventario i ON p.id_pelicula = i.id_pelicula
    LEFT JOIN alquiler r ON i.id_inventario = r.id_inventario
    WHERE r.id_alquiler IS NULL;
    
+------------------------+
| pelicula_titulo        |
+------------------------+
| ACADEMY DINOSAUR       |
| ALICE FANTASIA         |
| APOLLO TEEN            |
| ARGONAUTS TOWN         |
| ARK RIDGEMONT          |
| ARSENIC INDEPENDENCE   |
| BOONDOCK BALLROOM      |
| BUTCH PANTHER          |
| CATCH AMISTAD          |
| CHINATOWN GLADIATOR    |
| CHOCOLATE DUCK         |
| COMMANDMENTS EXPRESS   |
| CROSSING DIVORCE       |
| CROWDS TELEMARK        |
| CRYSTAL BREAKING       |
| DAZED PUNK             |
| DELIVERANCE MULHOLLAND |
| FIREHOUSE VIETNAM      |
| FLOATS GARDEN          |
| FRANKENSTEIN STRANGER  |
| GLADIATOR WESTWARD     |
| GUMP DATE              |
| HATE HANDICAP          |
| HOCUS FRIDA            |
| KENTUCKIAN GIANT       |
| KILL BROTHERHOOD       |
| MUPPET MILE            |
| ORDER BETRAYED         |
| PEARL DESTINY          |
| PERDITION FARGO        |
| PSYCHO SHRUNK          |
| RAIDERS ANTITRUST      |
| RAINBOW SHOCK          |
| ROOF CHAMPION          |
| SISTER FREDDY          |
| SKY MIRACLE            |
| SUICIDES SILENCE       |
| TADPOLE PARK           |
| TREASURE COMMAND       |
| VILLAIN DESPERATE      |
| VOLUME HOUSE           |
| WAKE JAWS              |
| WALLS ARTIST           |
+------------------------+
```

Listar los empleados que trabajan en el mismo almacén que el
empleado con id_empleado = 1.

```sql
    SELECT e.nombre AS empleado_nombre, e.apellidos AS empleado_apellido
    FROM empleado e
    WHERE e.id_almacen = (SELECT id_almacen FROM empleado WHERE id_empleado = 1);
        
+-----------------+-------------------+
| empleado_nombre | empleado_apellido |
+-----------------+-------------------+
| Mike            | Hillyer           |
| Jon             | Stephens          |
| Pepe            | Spilberg          |
+-----------------+-------------------+
```

Encontrar el nombre de las ciudades que no tienen ningún
cliente registrado.

```sql
    SELECT ci.nombre
    FROM ciudad ci
    LEFT JOIN direccion d ON ci.id_ciudad = d.id_ciudad
    LEFT JOIN cliente c ON d.id_direccion = c.id_direccion
    WHERE c.id_cliente IS NULL;
    
+----------------------------+
| ciudad_nombre              |
+----------------------------+
| A Corua (La Corua)         |
| Abha                       |
| Abu Dhabi                  |
| Acua                       |
| Adana                      |
| Addis Abeba                |
| Aden                       |
| Adoni                      |
| Ahmadnagar                 |
| Akishima                   |
| Akron                      |
| al-Ayn                     |
| al-Hawiya                  |
| al-Manama                  |
| al-Qadarif                 |
| al-Qatif                   |
| Allappuzha (Alleppey)      |
| Allende                    |
| Almirante Brown            |
| Alvorada                   |
| Ambattur                   |
| Amersfoort                 |
| Amroha                     |
| Angra dos Reis             |
| Anpolis                    |
| Antofagasta                |
| Aparecida de Goinia        |
| Apeldoorn                  |
| Araatuba                   |
| Arecibo                    |
| Arlington                  |
| Ashdod                     |
| Ashgabat                   |
| Ashqelon                   |
| Asuncin                    |
| Atinsk                     |
| Atlixco                    |
| Augusta-Richmond County    |
| Aurora                     |
| Avellaneda                 |
| Bag                        |
| Baha Blanca                |
| Baicheng                   |
| Baiyin                     |
| Baku                       |
| Balaiha                    |
| Balikesir                  |
| Balurghat                  |
| Bamenda                    |
| Bandar Seri Begawan        |
| Banjul                     |
| Barcelona                  |
| Basel                      |
| Bat Yam                    |
| Batman                     |
| Batna                      |
| Battambang                 |
| Baybay                     |
| Bayugan                    |
| Bchar                      |
| Beira                      |
| Bellevue                   |
| Belm                       |
| Benguela                   |
| Beni-Mellal                |
| Benin City                 |
| Bergamo                    |
| Berhampore (Baharampur)    |
| Bern                       |
| Bhavnagar                  |
| Bhilwara                   |
| Bhimavaram                 |
| Bhusawal                   |
| Bijapur                    |
| Bilbays                    |
| Binzhou                    |
| Birgunj                    |
| Bislig                     |
| Blumenau                   |
| Boa Vista                  |
| Boksburg                   |
| Botosani                   |
| Botshabelo                 |
| Bradford                   |
| Braslia                    |
| Bratislava                 |
| Brescia                    |
| Brest                      |
| Brindisi                   |
| Brockton                   |
| Bucuresti                  |
| Buenaventura               |
| Bydgoszcz                  |
| Cabuyao                    |
| Callao                     |
| Cam Ranh                   |
| Cape Coral                 |
| Caracas                    |
| Carmen                     |
| Cavite                     |
| Cayenne                    |
| Celaya                     |
| Chandrapur                 |
| Changhwa                   |
| Changzhou                  |
| Chapra                     |
| Charlotte Amalie           |
| Chatsworth                 |
| Cheju                      |
| Chiayi                     |
| Chungho                    |
```

Obtener los nombres y apellidos de los actores que han
participado en más de 10 películas.(having)

```sql
    SELECT a.nombre AS actor_nombre, a.apellidos AS actor_apellido
    FROM actor a
    JOIN pelicula_actor pa ON a.id_actor = pa.id_actor
    GROUP BY a.id_actor
    HAVING COUNT(pa.id_pelicula) > 10;
    
+--------------+----------------+
| actor_nombre | actor_apellido |
+--------------+----------------+
| PENELOPE     | GUINESS        |
| NICK         | WAHLBERG       |
| ED           | CHASE          |
| JENNIFER     | DAVIS          |
| JOHNNY       | LOLLOBRIGIDA   |
| BETTE        | NICHOLSON      |
| GRACE        | MOSTEL         |
| MATTHEW      | JOHANSSON      |
| JOE          | SWANK          |
| CHRISTIAN    | GABLE          |
| ZERO         | CAGE           |
| KARL         | BERRY          |
| UMA          | WOOD           |
| VIVIEN       | BERGEN         |
| CUBA         | OLIVIER        |
| FRED         | COSTNER        |
| HELEN        | VOIGHT         |
| DAN          | TORN           |
| BOB          | FAWCETT        |
| LUCILLE      | TRACY          |
| KIRSTEN      | PALTROW        |
| ELVIS        | MARX           |
| SANDRA       | KILMER         |
| CAMERON      | STREEP         |
| KEVIN        | BLOOM          |
| RIP          | CRAWFORD       |
| JULIA        | MCQUEEN        |
| WOODY        | HOFFMAN        |
| ALEC         | WAYNE          |
| SANDRA       | PECK           |
| SISSY        | SOBIESKI       |
| TIM          | HACKMAN        |
| MILLA        | PECK           |
| AUDREY       | OLIVIER        |
| JUDY         | DEAN           |
| BURT         | DUKAKIS        |
| VAL          | BOLGER         |
| TOM          | MCKELLEN       |
| GOLDIE       | BRODY          |
| JOHNNY       | CAGE           |
| JODIE        | DEGENERES      |
| TOM          | MIRANDA        |
| KIRK         | JOVOVICH       |
| NICK         | STALLONE       |
| REESE        | KILMER         |
| PARKER       | GOLDBERG       |
| JULIA        | BARRYMORE      |
| FRANCES      | DAY-LEWIS      |
| ANNE         | CRONYN         |
| NATALIE      | HOPKINS        |
| GARY         | PHOENIX        |
| CARMEN       | HUNT           |
| MENA         | TEMPLE         |
| PENELOPE     | PINKETT        |
| FAY          | KILMER         |
| DAN          | HARRIS         |
| JUDE         | CRUISE         |
| CHRISTIAN    | AKROYD         |
| DUSTIN       | TAUTOU         |
| HENRY        | BERRY          |
| CHRISTIAN    | NEESON         |
| JAYNE        | NEESON         |
| CAMERON      | WRAY           |
| RAY          | JOHANSSON      |
| ANGELA       | HUDSON         |
| MARY         | TANDY          |
| JESSICA      | BAILEY         |
| RIP          | WINSLET        |
| KENNETH      | PALTROW        |
| MICHELLE     | MCCONAUGHEY    |
| ADAM         | GRANT          |
| SEAN         | WILLIAMS       |
| GARY         | PENN           |
| MILLA        | KEITEL         |
| BURT         | POSEY          |
| ANGELINA     | ASTAIRE        |
| CARY         | MCCONAUGHEY    |
| GROUCHO      | SINATRA        |
| MAE          | HOFFMAN        |
| RALPH        | CRUZ           |
| SCARLETT     | DAMON          |
| WOODY        | JOLIE          |
| BEN          | WILLIS         |
| JAMES        | PITT           |
| MINNIE       | ZELLWEGER      |
| GREG         | CHAPLIN        |
| SPENCER      | PECK           |
| KENNETH      | PESCI          |
| CHARLIZE     | DENCH          |
| SEAN         | GUINESS        |
| CHRISTOPHER  | BERRY          |
| KIRSTEN      | AKROYD         |
| ELLEN        | PRESLEY        |
| KENNETH      | TORN           |
| DARYL        | WAHLBERG       |
| GENE         | WILLIS         |
| MEG          | HAWKE          |
| CHRIS        | BRIDGES        |
| JIM          | MOSTEL         |
| SPENCER      | DEPP           |
| SUSAN        | DAVIS          |
| WALTER       | TORN           |
| MATTHEW      | LEIGH          |
| PENELOPE     | CRONYN         |
| SIDNEY       | CROWE          |
| GROUCHO      | DUNST          |
| GINA         | DEGENERES      |
| WARREN       | NOLTE          |
| SYLVESTER    | DERN           |
| SUSAN        | DAVIS          |
| CAMERON      | ZELLWEGER      |
| RUSSELL      | BACALL         |
| MORGAN       | HOPKINS        |
| MORGAN       | MCDORMAND      |
| HARRISON     | BALE           |
| DAN          | STREEP         |
| RENEE        | TRACY          |
| CUBA         | ALLEN          |
| WARREN       | JACKMAN        |
| PENELOPE     | MONROE         |
| LIZA         | BERGMAN        |
| SALMA        | NOLTE          |
| JULIANNE     | DENCH          |
| SCARLETT     | BENING         |
| ALBERT       | NOLTE          |
| FRANCES      | TOMEI          |
| KEVIN        | GARLAND        |
| CATE         | MCQUEEN        |
| DARYL        | CRAWFORD       |
| GRETA        | KEITEL         |
| JANE         | JACKMAN        |
| ADAM         | HOPPER         |
| RICHARD      | PENN           |
| GENE         | HOPKINS        |
| RITA         | REYNOLDS       |
| ED           | MANSFIELD      |
| MORGAN       | WILLIAMS       |
| LUCILLE      | DEE            |
| EWAN         | GOODING        |
| WHOOPI       | HURT           |
| CATE         | HARRIS         |
| JADA         | RYDER          |
| RIVER        | DEAN           |
| ANGELA       | WITHERSPOON    |
| KIM          | ALLEN          |
| ALBERT       | JOHANSSON      |
| FAY          | WINSLET        |
| EMILY        | DEE            |
| RUSSELL      | TEMPLE         |
| JAYNE        | NOLTE          |
| GEOFFREY     | HESTON         |
| BEN          | HARRIS         |
| MINNIE       | KILMER         |
| MERYL        | GIBSON         |
| IAN          | TANDY          |
| FAY          | WOOD           |
| GRETA        | MALDEN         |
| VIVIEN       | BASINGER       |
| LAURA        | BRODY          |
| CHRIS        | DEPP           |
| HARVEY       | HOPE           |
| OPRAH        | KILMER         |
| CHRISTOPHER  | WEST           |
| HUMPHREY     | WILLIS         |
| AL           | GARLAND        |
| NICK         | DEGENERES      |
| LAURENCE     | BULLOCK        |
| WILL         | WILSON         |
| KENNETH      | HOFFMAN        |
| MENA         | HOPPER         |
| OLYMPIA      | PFEIFFER       |
| GROUCHO      | WILLIAMS       |
| ALAN         | DREYFUSS       |
| MICHAEL      | BENING         |
| WILLIAM      | HACKMAN        |
| JON          | CHASE          |
| GENE         | MCKELLEN       |
| LISA         | MONROE         |
| ED           | GUINESS        |
| JEFF         | SILVERSTONE    |
| MATTHEW      | CARREY         |
| DEBBIE       | AKROYD         |
| RUSSELL      | CLOSE          |
| HUMPHREY     | GARLAND        |
| MICHAEL      | BOLGER         |
| JULIA        | ZELLWEGER      |
| RENEE        | BALL           |
| ROCK         | DUKAKIS        |
| CUBA         | BIRCH          |
| AUDREY       | BAILEY         |
| GREGORY      | GOODING        |
| JOHN         | SUVARI         |
| BURT         | TEMPLE         |
| MERYL        | ALLEN          |
| JAYNE        | SILVERSTONE    |
| BELA         | WALKEN         |
| REESE        | WEST           |
| MARY         | KEITEL         |
| JULIA        | FAWCETT        |
| THORA        | TEMPLE         |
+--------------+----------------+
```

Encontrar los nombres y apellidos de los clientes que han
realizado un pago mayor a 100.

```sql
    SELECT c.nombre AS cliente_nombre, c.apellidos AS cliente_apellido
    FROM cliente c
    JOIN pago p ON c.id_cliente = p.id_cliente
    WHERE p.total > 100;
    
    
```

Listar los títulos de las películas lanzadas en el mismo año que
la película con id_pelicula = 2.

```sql

  	SELECT p2.titulo AS pelicula_titulo
    FROM pelicula p1
    JOIN pelicula p2 ON p1.anyo_lanzamiento = p2.anyo_lanzamiento
    WHERE p1.id_pelicula = 2 AND p2.id_pelicula != 2;
    
    
    +-----------------------------+
| pelicula_titulo             |
+-----------------------------+
| ACADEMY DINOSAUR            |
| ADAPTATION HOLES            |
| AFFAIR PREJUDICE            |
| AFRICAN EGG                 |
| AGENT TRUMAN                |
| AIRPLANE SIERRA             |
| AIRPORT POLLOCK             |
| ALABAMA DEVIL               |
| ALADDIN CALENDAR            |
| ALAMO VIDEOTAPE             |
| ALASKA PHANTOM              |
| ALI FOREVER                 |
| ALICE FANTASIA              |
| ALIEN CENTER                |
| ALLEY EVOLUTION             |
| ALONE TRIP                  |
| ALTER VICTORY               |
| AMADEUS HOLY                |
| AMELIE HELLFIGHTERS         |
| AMERICAN CIRCUS             |
| AMISTAD MIDSUMMER           |
| ANACONDA CONFESSIONS        |
| ANALYZE HOOSIERS            |
| ANGELS LIFE                 |
| ANNIE IDENTITY              |
| ANONYMOUS HUMAN             |
| ANTHEM LUKE                 |
| ANTITRUST TOMATOES          |
| ANYTHING SAVANNAH           |
| APACHE DIVINE               |
| APOCALYPSE FLAMINGOS        |
| APOLLO TEEN                 |
| ARABIA DOGMA                |
| ARACHNOPHOBIA ROLLERCOASTER |
| ARGONAUTS TOWN              |
| ARIZONA BANG                |
| ARK RIDGEMONT               |
| ARMAGEDDON LOST             |
| ARMY FLINTSTONES            |
| ARSENIC INDEPENDENCE        |
| ARTIST COLDBLOODED          |
| ATLANTIS CAUSE              |
| ATTACKS HATE                |
| ATTRACTION NEWTON           |
| AUTUMN CROW                 |
| BABY HALL                   |
| BACKLASH UNDEFEATED         |
| BADMAN DAWN                 |
| BAKED CLEOPATRA             |
| BALLOON HOMEWARD            |
| BALLROOM MOCKINGBIRD        |
| BANG KWAI                   |
| BANGER PINOCCHIO            |
| BARBARELLA STREETCAR        |
| BAREFOOT MANCHURIAN         |
| BASIC EASY                  |
| BEACH HEARTBREAKERS         |
| BEAR GRACELAND              |
| BEAST HUNCHBACK             |
| BEAUTY GREASE               |
| BED HIGHBALL                |
| BEDAZZLED MARRIED           |
| BEETHOVEN EXORCIST          |
| BEHAVIOR RUNAWAY            |
| BENEATH RUSH                |
| BERETS AGENT                |
| BETRAYED REAR               |
| BEVERLY OUTLAW              |
| BIKINI BORROWERS            |
| BILKO ANONYMOUS             |
| BILL OTHERS                 |
| BINGO TALENTED              |
| BIRCH ANTITRUST             |
| BIRD INDEPENDENCE           |
| BIRDCAGE CASPER             |
| BIRDS PERDITION             |
| BLACKOUT PRIVATE            |
| BLADE POLISH                |
| BLANKET BEVERLY             |
| BLINDNESS GUN               |
| BLOOD ARGONAUTS             |
| BLUES INSTINCT              |
| BOILED DARES                |
| BONNIE HOLOCAUST            |
| BOOGIE AMELIE               |
| BOONDOCK BALLROOM           |
| BORN SPINAL                 |
| BORROWERS BEDAZZLED         |
| BOULEVARD MOB               |
| BOUND CHEAPER               |
| BOWFINGER GABLES            |
| BRANNIGAN SUNRISE           |
| BRAVEHEART HUMAN            |
| BREAKFAST GOLDFINGER        |
| BREAKING HOME               |
| BRIDE INTRIGUE              |
| BRIGHT ENCOUNTERS           |
| BRINGING HYSTERICAL         |
| BROOKLYN DESERT             |
| BROTHERHOOD BLANKET         |
| BUBBLE GROSSE               |
| BUCKET BROTHERHOOD          |
| BUGSY SONG                  |
| BULL SHAWSHANK              |
| BULWORTH COMMANDMENTS       |
| BUNCH MINDS                 |
| BUTCH PANTHER               |
| BUTTERFLY CHOCOLAT          |
| CABIN FLASH                 |
| CADDYSHACK JEDI             |
| CALENDAR GUNFIGHT           |
| CALIFORNIA BIRDS            |
| CAMELOT VACATION            |
| CAMPUS REMEMBER             |
| CANDIDATE PERDITION         |
| CANDLES GRAPES              |
| CANYON STOCK                |
| CAPER MOTIONS               |
| CARIBBEAN LIBERTY           |
| CAROL TEXAS                 |
| CARRIE BUNCH                |
| CASABLANCA SUPER            |
| CASPER DRAGONFLY            |
| CASSIDY WYOMING             |
| CASUALTIES ENCINO           |
| CAT CONEHEADS               |
| CATCH AMISTAD               |
| CAUSE DATE                  |
| CELEBRITY HORN              |
| CENTER DINOSAUR             |
| CHAINSAW UPTOWN             |
| CHAMBER ITALIAN             |
| CHAMPION FLATLINERS         |
| CHANCE RESURRECTION         |
| CHAPLIN LICENSE             |
| CHARADE DUFFEL              |
| CHARIOTS CONSPIRACY         |
| CHASING FIGHT               |
| CHEAPER CLYDE               |
| CHICAGO NORTH               |
| CHICKEN HELLFIGHTERS        |
| CHILL LUCK                  |
| CHINATOWN GLADIATOR         |
| CHISUM BEHAVIOR             |
| CHITTY LOCK                 |
| CHOCOLAT HARRY              |
| CHOCOLATE DUCK              |
| CHRISTMAS MOONSHINE         |
| CIDER DESIRE                |
| CINCINATTI WHISPERER        |
| CIRCUS YOUTH                |
| CITIZEN SHREK               |
| CLASH FREDDY                |
| CLEOPATRA DEVIL             |
| CLERKS ANGELS               |
| CLOCKWORK PARADISE          |
| CLONES PINOCCHIO            |
| CLOSER BANG                 |
| CLUB GRAFFITI               |
| CLUE GRAIL                  |
| CLUELESS BUCKET             |
| CLYDE THEORY                |
| COAST RAINBOW               |
| COLDBLOODED DARLING         |
| COLOR PHILADELPHIA          |
| COMA HEAD                   |
| COMANCHEROS ENEMY           |
| COMFORTS RUSH               |
| COMMAND DARLING             |
| COMMANDMENTS EXPRESS        |
| CONEHEADS SMOOCHY           |
| CONFESSIONS MAGUIRE         |
| CONFIDENTIAL INTERVIEW      |
| CONFUSED CANDLES            |
| CONGENIALITY QUEST          |
| CONNECTICUT TRAMP           |
| CONNECTION MICROCOSMOS      |
| CONQUERER NUTS              |
| CONSPIRACY SPIRIT           |
| CONTACT ANONYMOUS           |
| CONTROL ANTHEM              |
| CONVERSATION DOWNHILL       |
| CORE SUIT                   |
| COWBOY DOOM                 |
| CRAFT OUTFIELD              |
| CRANES RESERVOIR            |
| CRAZY HOME                  |
| CREATURES SHAKESPEARE       |
| CREEPERS KANE               |
| CROOKED FROGMEN             |
| CROSSING DIVORCE            |
| CROSSROADS CASUALTIES       |
| CROW GREASE                 |
| CROWDS TELEMARK             |
| CRUELTY UNFORGIVEN          |
| CRUSADE HONEY               |
| CRYSTAL BREAKING            |
| CUPBOARD SINNERS            |
| CURTAIN VIDEOTAPE           |
| CYCLONE FAMILY              |
| DADDY PITTSBURGH            |
| DAISY MENAGERIE             |
| DALMATIONS SWEDEN           |
| DANCES NONE                 |
| DANCING FEVER               |
| DANGEROUS UPTOWN            |
| DARES PLUTO                 |
| DARKNESS WAR                |
| DARKO DORADO                |
| DARLING BREAKING            |
| DARN FORRESTER              |
| DATE SPEED                  |
| DAUGHTER MADIGAN            |
| DAWN POND                   |
| DAY UNFAITHFUL              |
| DAZED PUNK                  |
| DECEIVER BETRAYED           |
| DEEP CRUSADE                |
| DEER VIRGINIAN              |
| DELIVERANCE MULHOLLAND      |
| DESERT POSEIDON             |
| DESIRE ALIEN                |
| DESPERATE TRAINSPOTTING     |
| DESTINATION JERK            |
| DESTINY SATURDAY            |
| DETAILS PACKER              |
| DETECTIVE VISION            |
| DEVIL DESIRE                |
| DIARY PANIC                 |
| DINOSAUR SECRETARY          |
| DIRTY ACE                   |
| DISCIPLE MOTHER             |
| DISTURBING SCARFACE         |
| DIVIDE MONSTER              |
| DIVINE RESURRECTION         |
| DIVORCE SHINING             |
| DOCTOR GRAIL                |
| DOGMA FAMILY                |
| DOLLS RAGE                  |
| DONNIE ALLEY                |
| DOOM DANCING                |
| DOORS PRESIDENT             |
| DORADO NOTTING              |
| DOUBLE WRATH                |
| DOUBTFIRE LABYRINTH         |
| DOWNHILL ENOUGH             |
| DOZEN LION                  |
| DRACULA CRYSTAL             |
| DRAGON SQUAD                |
| DRAGONFLY STRANGERS         |
| DREAM PICKUP                |
| DRIFTER COMMANDMENTS        |
| DRIVER ANNIE                |
| DRIVING POLISH              |
| DROP WATERFRONT             |
| DRUMLINE CYCLONE            |
| DRUMS DYNAMITE              |
| DUCK RACER                  |
| DUDE BLINDNESS              |
| DUFFEL APOCALYPSE           |
| DUMBO LUST                  |
| DURHAM PANKY                |
| DWARFS ALTER                |
| DYING MAKER                 |
| DYNAMITE TARZAN             |
| EAGLES PANKY                |
| EARLY HOME                  |
| EARRING INSTINCT            |
| EARTH VISION                |
| EASY GLADIATOR              |
| EDGE KISSING                |
| EFFECT GLADIATOR            |
| EGG IGBY                    |
| EGYPT TENENBAUMS            |
| ELEMENT FREDDY              |
| ELEPHANT TROJAN             |
| ELF MURDER                  |
| ELIZABETH SHANE             |
| EMPIRE MALKOVICH            |
| ENCINO ELF                  |
| ENCOUNTERS CURTAIN          |
| ENDING CROWDS               |
| ENEMY ODDS                  |
| ENGLISH BULWORTH            |
| ENOUGH RAGING               |
| ENTRAPMENT SATISFACTION     |
| ESCAPE METROPOLIS           |
| EVE RESURRECTION            |
| EVERYONE CRAFT              |
| EVOLUTION ALTER             |
| EXCITEMENT EVE              |
| EXORCIST STING              |
| EXPECATIONS NATURAL         |
| EXPENDABLE STALLION         |
| EXPRESS LONELY              |
| EXTRAORDINARY CONQUERER     |
| EYES DRIVING                |
| FACTORY DRAGON              |
| FALCON VOLUME               |
| FAMILY SWEET                |
| FANTASIA PARK               |
| FANTASY TROOPERS            |
| FARGO GANDHI                |
| FATAL HAUNTED               |
| FEATHERS METAL              |
| FELLOWSHIP AUTUMN           |
| FERRIS MOTHER               |
| FEUD FROGMEN                |
| FEVER EMPIRE                |
| FICTION CHRISTMAS           |
| FIDDLER LOST                |
| FIDELITY DEVIL              |
| FIGHT JAWBREAKER            |
| FINDING ANACONDA            |
| FIRE WOLVES                 |
| FIREBALL PHILADELPHIA       |
| FIREHOUSE VIETNAM           |
| FISH OPUS                   |
| FLAMINGOS CONNECTICUT       |
| FLASH WARS                  |
| FLATLINERS KILLER           |
| FLIGHT LIES                 |
| FLINTSTONES HAPPINESS       |
| FLOATS GARDEN               |
| FLYING HOOK                 |
| FOOL MOCKINGBIRD            |
| FOREVER CANDIDATE           |
| FORREST SONS                |
| FORRESTER COMANCHEROS       |
| FORWARD TEMPLE              |
| FRANKENSTEIN STRANGER       |
| FREAKY POCUS                |
| FREDDY STORM                |
| FREEDOM CLEOPATRA           |
| FRENCH HOLIDAY              |
| FRIDA SLIPPER               |
| FRISCO FORREST              |
| FROGMEN BREAKING            |
| FRONTIER CABIN              |
| FROST HEAD                  |
| FUGITIVE MAGUIRE            |
| FULL FLATLINERS             |
| FURY MURDER                 |
| GABLES METROPOLIS           |
| GALAXY SWEETHEARTS          |
| GAMES BOWFINGER             |
| GANDHI KWAI                 |
| GANGS PRIDE                 |
| GARDEN ISLAND               |
| GASLIGHT CRUSADE            |
| GATHERING CALENDAR          |
| GENTLEMEN STAGE             |
| GHOST GROUNDHOG             |
| GHOSTBUSTERS ELF            |
| GIANT TROOPERS              |
| GILBERT PELICAN             |
| GILMORE BOILED              |
| GLADIATOR WESTWARD          |
| GLASS DYING                 |
| GLEAMING JAWBREAKER         |
| GLORY TRACY                 |
| GO PURPLE                   |
| GODFATHER DIARY             |
| GOLD RIVER                  |
| GOLDFINGER SENSIBILITY      |
| GOLDMINE TYCOON             |
| GONE TROUBLE                |
| GOODFELLAS SALUTE           |
| GORGEOUS BINGO              |
| GOSFORD DONNIE              |
| GRACELAND DYNAMITE          |
| GRADUATE LORD               |
| GRAFFITI LOVE               |
| GRAIL FRANKENSTEIN          |
| GRAPES FURY                 |
| GREASE YOUTH                |
| GREATEST NORTH              |
| GREEDY ROOTS                |
| GREEK EVERYONE              |
| GRINCH MASSAGE              |
| GRIT CLOCKWORK              |
| GROOVE FICTION              |
| GROSSE WONDERFUL            |
| GROUNDHOG UNCUT             |
| GUMP DATE                   |
| GUN BONNIE                  |
| GUNFIGHT MOON               |
| GUNFIGHTER MUSSOLINI        |
| GUYS FALCON                 |
| HALF OUTFIELD               |
| HALL CASSIDY                |
| HALLOWEEN NUTS              |
| HAMLET WISDOM               |
| HANDICAP BOONDOCK           |
| HANGING DEEP                |
| HANKY OCTOBER               |
| HANOVER GALAXY              |
| HAPPINESS UNITED            |
| HARDLY ROBBERS              |
| HAROLD FRENCH               |
| HARPER DYING                |
| HARRY IDAHO                 |
| HATE HANDICAP               |
| HAUNTED ANTITRUST           |
| HAUNTING PIANIST            |
| HAWK CHILL                  |
| HEAD STRANGER               |
| HEARTBREAKERS BRIGHT        |
| HEAVEN FREEDOM              |
| HEAVENLY GUN                |
| HEAVYWEIGHTS BEAST          |
| HEDWIG ALTER                |
| HELLFIGHTERS SIERRA         |
| HIGH ENCINO                 |
| HIGHBALL POTTER             |
| HILLS NEIGHBORS             |
| HOBBIT ALIEN                |
| HOCUS FRIDA                 |
| HOLES BRANNIGAN             |
| HOLIDAY GAMES               |
| HOLLOW JEOPARDY             |
| HOLLYWOOD ANONYMOUS         |
| HOLOCAUST HIGHBALL          |
| HOLY TADPOLE                |
| HOME PITY                   |
| HOMEWARD CIDER              |
| HOMICIDE PEACH              |
| HONEY TIES                  |
| HOOK CHARIOTS               |
| HOOSIERS BIRDCAGE           |
| HOPE TOOTSIE                |
| HORN WORKING                |
| HORROR REIGN                |
| HOTEL HAPPINESS             |
| HOURS RAGE                  |
| HOUSE DYNAMITE              |
| HUMAN GRAFFITI              |
| HUNCHBACK IMPOSSIBLE        |
| HUNGER ROOF                 |
| HUNTER ALTER                |
| HUNTING MUSKETEERS          |
| HURRICANE AFFAIR            |
| HUSTLER PARTY               |
| HYDE DOCTOR                 |
| HYSTERICAL GRAIL            |
| ICE CROSSING                |
| IDAHO LOVE                  |
| IDENTITY LOVER              |
| IDOLS SNATCHERS             |
| IGBY MAKER                  |
| ILLUSION AMELIE             |
| IMAGE PRINCESS              |
| IMPACT ALADDIN              |
| IMPOSSIBLE PREJUDICE        |
| INCH JET                    |
| INDEPENDENCE HOTEL          |
| INDIAN LOVE                 |
| INFORMER DOUBLE             |
| INNOCENT USUAL              |
| INSECTS STONE               |
| INSIDER ARIZONA             |
| INSTINCT AIRPORT            |
| INTENTIONS EMPIRE           |
| INTERVIEW LIAISONS          |
| INTOLERABLE INTENTIONS      |
| INTRIGUE WORST              |
| INVASION CYCLONE            |
| IRON MOON                   |
| ISHTAR ROCKETEER            |
| ISLAND EXORCIST             |
| ITALIAN AFRICAN             |
| JACKET FRISCO               |
| JADE BUNCH                  |
| JAPANESE RUN                |
| JASON TRAP                  |
| JAWBREAKER BROOKLYN         |
| JAWS HARRY                  |
| JEDI BENEATH                |
| JEEPERS WEDDING             |
| JEKYLL FROGMEN              |
| JEOPARDY ENCINO             |
| JERICHO MULAN               |
| JERK PAYCHECK               |
| JERSEY SASSY                |
| JET NEIGHBORS               |
| JINGLE SAGEBRUSH            |
| JOON NORTHWEST              |
| JUGGLER HARDLY              |
| JUMANJI BLADE               |
| JUMPING WRATH               |
| JUNGLE CLOSER               |
| KANE EXORCIST               |
| KARATE MOON                 |
| KENTUCKIAN GIANT            |
| KICK SAVANNAH               |
| KILL BROTHERHOOD            |
| KILLER INNOCENT             |
| KING EVOLUTION              |
| KISS GLORY                  |
| KISSING DOLLS               |
| KNOCK WARLOCK               |
| KRAMER CHOCOLATE            |
| KWAI HOMEWARD               |
| LABYRINTH LEAGUE            |
| LADY STAGE                  |
| LADYBUGS ARMAGEDDON         |
| LAMBS CINCINATTI            |
| LANGUAGE COWBOY             |
| LAWLESS VISION              |
| LAWRENCE LOVE               |
| LEAGUE HELLFIGHTERS         |
| LEATHERNECKS DWARFS         |
| LEBOWSKI SOLDIERS           |
| LEGALLY SECRETARY           |
| LEGEND JEDI                 |
| LESSON CLEOPATRA            |
| LIAISONS SWEET              |
| LIBERTY MAGNIFICENT         |
| LICENSE WEEKEND             |
| LIES TREATMENT              |
| LIFE TWISTED                |
| LIGHTS DEER                 |
| LION UNCUT                  |
| LOATHING LEGALLY            |
| LOCK REAR                   |
| LOLA AGENT                  |
| LOLITA WORLD                |
| LONELY ELEPHANT             |
| LORD ARIZONA                |
| LOSE INCH                   |
| LOSER HUSTLER               |
| LOST BIRD                   |
| LOUISIANA HARRY             |
| LOVE SUICIDES               |
| LOVELY JINGLE               |
| LOVER TRUMAN                |
| LOVERBOY ATTACKS            |
| LUCK OPUS                   |
| LUCKY FLYING                |
| LUKE MUMMY                  |
| LUST LOCK                   |
| MADIGAN DORADO              |
| MADISON TRAP                |
| MADNESS ATTACKS             |
| MADRE GABLES                |
| MAGIC MALLRATS              |
| MAGNIFICENT CHITTY          |
| MAGNOLIA FORRESTER          |
| MAGUIRE APACHE              |
| MAIDEN HOME                 |
| MAJESTIC FLOATS             |
| MAKER GABLES                |
| MALKOVICH PET               |
| MALLRATS UNITED             |
| MALTESE HOPE                |
| MANCHURIAN CURTAIN          |
| MANNEQUIN WORST             |
| MARRIED GO                  |
| MARS ROMAN                  |
| MASK PEACH                  |
| MASKED BUBBLE               |
| MASSACRE USUAL              |
| MASSAGE IMAGE               |
| MATRIX SNOWMAN              |
| MAUDE MOD                   |
| MEET CHOCOLATE              |
| MEMENTO ZOOLANDER           |
| MENAGERIE RUSHMORE          |
| MERMAID INSECTS             |
| METAL ARMAGEDDON            |
| METROPOLIS COMA             |
| MICROCOSMOS PARADISE        |
| MIDNIGHT WESTWARD           |
| MIDSUMMER GROUNDHOG         |
| MIGHTY LUCK                 |
| MILE MULAN                  |
| MILLION ACE                 |
| MINDS TRUMAN                |
| MINE TITANS                 |
| MINORITY KISS               |
| MIRACLE VIRTUAL             |
| MISSION ZOOLANDER           |
| MIXED DOORS                 |
| MOB DUFFEL                  |
| MOCKINGBIRD HOLLYWOOD       |
| MOD SECRETARY               |
| MODEL FISH                  |
| MODERN DORADO               |
| MONEY HAROLD                |
| MONSOON CAUSE               |
| MONSTER SPARTACUS           |
| MONTEREY LABYRINTH          |
| MONTEZUMA COMMAND           |
| MOON BUNCH                  |
| MOONSHINE CABIN             |
| MOONWALKER FOOL             |
| MOSQUITO ARMAGEDDON         |
| MOTHER OLEANDER             |
| MOTIONS DETAILS             |
| MOULIN WAKE                 |
| MOURNING PURPLE             |
| MOVIE SHAKESPEARE           |
| MULAN MOON                  |
| MULHOLLAND BEAST            |
| MUMMY CREATURES             |
| MUPPET MILE                 |
| MURDER ANTITRUST            |
| MUSCLE BRIGHT               |
| MUSIC BOONDOCK              |
| MUSKETEERS WAIT             |
| MUSSOLINI SPOILERS          |
| MYSTIC TRUMAN               |
| NAME DETECTIVE              |
| NASH CHOCOLAT               |
| NATIONAL STORY              |
| NATURAL STOCK               |
| NECKLACE OUTBREAK           |
| NEIGHBORS CHARADE           |
| NEMO CAMPUS                 |
| NETWORK PEAK                |
| NEWSIES STORY               |
| NEWTON LABYRINTH            |
| NIGHTMARE CHILL             |
| NONE SPIKING                |
| NOON PAPI                   |
| NORTH TEQUILA               |
| NORTHWEST POLISH            |
| NOTORIOUS REUNION           |
| NOTTING SPEAKEASY           |
| NOVOCAINE FLIGHT            |
| NUTS TIES                   |
| OCTOBER SUBMARINE           |
| ODDS BOOGIE                 |
| OKLAHOMA JUMANJI            |
| OLEANDER CLUE               |
| OPEN AFRICAN                |
| OPERATION OPERATION         |
| OPPOSITE NECKLACE           |
| OPUS ICE                    |
| ORANGE GRAPES               |
| ORDER BETRAYED              |
| ORIENT CLOSER               |
| OSCAR GOLD                  |
| OTHERS SOUP                 |
| OUTBREAK DIVINE             |
| OUTFIELD MASSACRE           |
| OUTLAW HANKY                |
| OZ LIAISONS                 |
| PACIFIC AMISTAD             |
| PACKER MADIGAN              |
| PAJAMA JAWBREAKER           |
| PANIC CLUB                  |
| PANKY SUBMARINE             |
| PANTHER REDS                |
| PAPI NECKLACE               |
| PARADISE SABRINA            |
| PARIS WEEKEND               |
| PARK CITIZEN                |
| PARTY KNOCK                 |
| PAST SUICIDES               |
| PATHS CONTROL               |
| PATIENT SISTER              |
| PATRIOT ROMAN               |
| PATTON INTERVIEW            |
| PAYCHECK WAIT               |
| PEACH INNOCENT              |
| PEAK FOREVER                |
| PEARL DESTINY               |
| PELICAN COMFORTS            |
| PERDITION FARGO             |
| PERFECT GROOVE              |
| PERSONAL LADYBUGS           |
| PET HAUNTING                |
| PHANTOM GLORY               |
| PHILADELPHIA WIFE           |
| PIANIST OUTFIELD            |
| PICKUP DRIVING              |
| PILOT HOOSIERS              |
| PINOCCHIO SIMON             |
| PIRATES ROXANNE             |
| PITTSBURGH HUNCHBACK        |
| PITY BOUND                  |
| PIZZA JUMANJI               |
| PLATOON INSTINCT            |
| PLUTO OLEANDER              |
| POCUS PULP                  |
| POLISH BROOKLYN             |
| POLLOCK DELIVERANCE         |
| POND SEATTLE                |
| POSEIDON FOREVER            |
| POTLUCK MIXED               |
| POTTER CONNECTICUT          |
| PREJUDICE OLEANDER          |
| PRESIDENT BANG              |
| PRIDE ALAMO                 |
| PRIMARY GLASS               |
| PRINCESS GIANT              |
| PRIVATE DROP                |
| PRIX UNDEFEATED             |
| PSYCHO SHRUNK               |
| PULP BEVERLY                |
| PUNK DIVORCE                |
| PURE RUNNER                 |
| PURPLE MOVIE                |
| QUEEN LUKE                  |
| QUEST MUSSOLINI             |
| QUILLS BULL                 |
| RACER EGG                   |
| RAGE GAMES                  |
| RAGING AIRPLANE             |
| RAIDERS ANTITRUST           |
| RAINBOW SHOCK               |
| RANDOM GO                   |
| RANGE MOONWALKER            |
| REAP UNFAITHFUL             |
| REAR TRADING                |
| REBEL AIRPORT               |
| RECORDS ZORRO               |
| REDEMPTION COMFORTS         |
| REDS POCUS                  |
| REEF SALUTE                 |
| REIGN GENTLEMEN             |
| REMEMBER DIARY              |
| REQUIEM TYCOON              |
| RESERVOIR ADAPTATION        |
| RESURRECTION SILVERADO      |
| REUNION WITCHES             |
| RIDER CADDYSHACK            |
| RIDGEMONT SUBMARINE         |
| RIGHT CRANES                |
| RINGS HEARTBREAKERS         |
| RIVER OUTLAW                |
| ROAD ROXANNE                |
| ROBBERS JOON                |
| ROBBERY BRIGHT              |
| ROCK INSTINCT               |
| ROCKETEER MOTHER            |
| ROCKY WAR                   |
| ROLLERCOASTER BRINGING      |
| ROMAN PUNK                  |
| ROOF CHAMPION               |
| ROOM ROMAN                  |
| ROOTS REMEMBER              |
| ROSES TREASURE              |
| ROUGE SQUAD                 |
| ROXANNE REBEL               |
| RUGRATS SHAKESPEARE         |
| RULES HUMAN                 |
| RUN PACIFIC                 |
| RUNAWAY TENENBAUMS          |
| RUNNER MADIGAN              |
| RUSH GOODFELLAS             |
| RUSHMORE MERMAID            |
| SABRINA MIDNIGHT            |
| SADDLE ANTITRUST            |
| SAGEBRUSH CLUELESS          |
| SAINTS BRIDE                |
| SALUTE APOLLO               |
| SAMURAI LION                |
| SANTA PARIS                 |
| SASSY PACKER                |
| SATISFACTION CONFIDENTIAL   |
| SATURDAY LAMBS              |
| SATURN NAME                 |
| SAVANNAH TOWN               |
| SCALAWAG DUCK               |
| SCARFACE BANG               |
| SCHOOL JACKET               |
| SCISSORHANDS SLUMS          |
| SCORPION APOLLO             |
| SEA VIRGIN                  |
| SEABISCUIT PUNK             |
| SEARCHERS WAIT              |
| SEATTLE EXPECATIONS         |
| SECRET GROUNDHOG            |
| SECRETARY ROUGE             |
| SECRETS PARADISE            |
| SENSE GREEK                 |
| SENSIBILITY REAR            |
| SEVEN SWARM                 |
| SHAKESPEARE SADDLE          |
| SHANE DARKNESS              |
| SHANGHAI TYCOON             |
| SHAWSHANK BUBBLE            |
| SHEPHERD MIDSUMMER          |
| SHINING ROSES               |
| SHIP WONDERLAND             |
| SHOCK CABIN                 |
| SHOOTIST SUPERFLY           |
| SHOW LORD                   |
| SHREK LICENSE               |
| SHRUNK DIVINE               |
| SIDE ARK                    |
| SIEGE MADRE                 |
| SIERRA DIVIDE               |
| SILENCE KANE                |
| SILVERADO GOLDFINGER        |
| SIMON NORTH                 |
| SINNERS ATLANTIS            |
| SISTER FREDDY               |
| SKY MIRACLE                 |
| SLACKER LIAISONS            |
| SLEEPING SUSPECTS           |
| SLEEPLESS MONSOON           |
| SLEEPY JAPANESE             |
| SLEUTH ORIENT               |
| SLING LUKE                  |
| SLIPPER FIDELITY            |
| SLUMS DUCK                  |
| SMILE EARRING               |
| SMOKING BARBARELLA          |
| SMOOCHY CONTROL             |
| SNATCH SLIPPER              |
| SNATCHERS MONTEZUMA         |
| SNOWMAN ROLLERCOASTER       |
| SOLDIERS EVOLUTION          |
| SOMETHING DUCK              |
| SONG HEDWIG                 |
| SONS INTERVIEW              |
| SORORITY QUEEN              |
| SOUP WISDOM                 |
| SOUTH WAIT                  |
| SPARTACUS CHEAPER           |
| SPEAKEASY DATE              |
| SPEED SUIT                  |
| SPICE SORORITY              |
| SPIKING ELEMENT             |
| SPINAL ROCKY                |
| SPIRIT FLINTSTONES          |
| SPIRITED CASUALTIES         |
| SPLASH GUMP                 |
| SPLENDOR PATTON             |
| SPOILERS HELLFIGHTERS       |
| SPY MILE                    |
| SQUAD FISH                  |
| STAGE WORLD                 |
| STAGECOACH ARMAGEDDON       |
| STALLION SUNDANCE           |
| STAMPEDE DISTURBING         |
| STAR OPERATION              |
| STATE WASTELAND             |
| STEEL SANTA                 |
| STEERS ARMAGEDDON           |
| STEPMOM DREAM               |
| STING PERSONAL              |
| STOCK GLASS                 |
| STONE FIRE                  |
| STORM HAPPINESS             |
| STORY SIDE                  |
| STRAIGHT HOURS              |
| STRANGELOVE DESIRE          |
| STRANGER STRANGERS          |
| STRANGERS GRAFFITI          |
| STREAK RIDGEMONT            |
| STREETCAR INTENTIONS        |
| STRICTLY SCARFACE           |
| SUBMARINE BED               |
| SUGAR WONKA                 |
| SUICIDES SILENCE            |
| SUIT WALLS                  |
| SUMMER SCARFACE             |
| SUN CONFESSIONS             |
| SUNDANCE INVASION           |
| SUNRISE LEAGUE              |
| SUNSET RACER                |
| SUPER WYOMING               |
| SUPERFLY TRIP               |
| SUSPECTS QUILLS             |
| SWARM GOLD                  |
| SWEDEN SHINING              |
| SWEET BROTHERHOOD           |
| SWEETHEARTS SUSPECTS        |
| TADPOLE PARK                |
| TALENTED HOMICIDE           |
| TARZAN VIDEOTAPE            |
| TAXI KICK                   |
| TEEN APOLLO                 |
| TELEGRAPH VOYAGE            |
| TELEMARK HEARTBREAKERS      |
| TEMPLE ATTRACTION           |
| TENENBAUMS COMMAND          |
| TEQUILA PAST                |
| TERMINATOR CLUB             |
| TEXAS WATCH                 |
| THEORY MERMAID              |
| THIEF PELICAN               |
| THIN SAGEBRUSH              |
| TIES HUNGER                 |
| TIGHTS DAWN                 |
| TIMBERLAND SKY              |
| TITANIC BOONDOCK            |
| TITANS JERK                 |
| TOMATOES HELLFIGHTERS       |
| TOMORROW HUSTLER            |
| TOOTSIE PILOT               |
| TORQUE BOUND                |
| TOURIST PELICAN             |
| TOWERS HURRICANE            |
| TOWN ARK                    |
| TRACY CIDER                 |
| TRADING PINOCCHIO           |
| TRAFFIC HOBBIT              |
| TRAIN BUNCH                 |
| TRAINSPOTTING STRANGERS     |
| TRAMP OTHERS                |
| TRANSLATION SUMMER          |
| TRAP GUYS                   |
| TREASURE COMMAND            |
| TREATMENT JEKYLL            |
| TRIP NEWTON                 |
| TROJAN TOMORROW             |
| TROOPERS METAL              |
| TROUBLE DATE                |
| TRUMAN CRAZY                |
| TURN STAR                   |
| TUXEDO MILE                 |
| TWISTED PIRATES             |
| TYCOON GATHERING            |
| UNBREAKABLE KARATE          |
| UNCUT SUICIDES              |
| UNDEFEATED DALMATIONS       |
| UNFAITHFUL KILL             |
| UNFORGIVEN ZOOLANDER        |
| UNITED PILOT                |
| UNTOUCHABLES SUNRISE        |
| UPRISING UPTOWN             |
| UPTOWN YOUNG                |
| USUAL UNTOUCHABLES          |
| VACATION BOONDOCK           |
| VALENTINE VANISHING         |
| VALLEY PACKER               |
| VAMPIRE WHALE               |
| VANILLA DAY                 |
| VANISHED GARDEN             |
| VANISHING ROCKY             |
| VARSITY TRIP                |
| VELVET TERMINATOR           |
| VERTIGO NORTHWEST           |
| VICTORY ACADEMY             |
| VIDEOTAPE ARSENIC           |
| VIETNAM SMOOCHY             |
| VILLAIN DESPERATE           |
| VIRGIN DAISY                |
| VIRGINIAN PLUTO             |
| VIRTUAL SPOILERS            |
| VISION TORQUE               |
| VOICE PEACH                 |
| VOLCANO TEXAS               |
| VOLUME HOUSE                |
| VOYAGE LEGALLY              |
| WAGON JAWS                  |
| WAIT CIDER                  |
| WAKE JAWS                   |
| WALLS ARTIST                |
| WANDA CHAMBER               |
| WAR NOTTING                 |
| WARDROBE PHANTOM            |
| WARLOCK WEREWOLF            |
| WARS PLUTO                  |
| WASH HEAVENLY               |
| WASTELAND DIVINE            |
| WATCH TRACY                 |
| WATERFRONT DELIVERANCE      |
| WATERSHIP FRONTIER          |
| WEDDING APOLLO              |
| WEEKEND PERSONAL            |
| WEREWOLF LOLA               |
| WEST LION                   |
| WESTWARD SEABISCUIT         |
| WHALE BIKINI                |
| WHISPERER GIANT             |
| WIFE TURN                   |
| WILD APOLLO                 |
| WILLOW TRACY                |
| WIND PHANTOM                |
| WINDOW SIDE                 |
| WISDOM WORKER               |
| WITCHES PANIC               |
| WIZARD COLDBLOODED          |
| WOLVES DESIRE               |
| WOMEN DORADO                |
| WON DARES                   |
| WONDERFUL DROP              |
| WONDERLAND CHRISTMAS        |
| WONKA SEA                   |
| WORDS HUNTER                |
| WORKER TARZAN               |
| WORKING MICROCOSMOS         |
| WORLD LEATHERNECKS          |
| WORST BANGER                |
| WRATH MILE                  |
| WRONG BEHAVIOR              |
| WYOMING STORM               |
| YENTL IDAHO                 |
| YOUNG LANGUAGE              |
| YOUTH KICK                  |
| ZHIVAGO CORE                |
| ZOOLANDER FICTION           |
| ZORRO ARK                   |
+-----------------------------+
```





# UNION DE TABLA HUERFANA



```sql
ALTER TABLE pelicula
ADD COLUMN film_id SMALLINT NOT NULL;

ALTER TABLE pelicula
ADD COLUMN CONSTRAINT fk_film_pel FOREIGN KEY (film_id) REFERENCES film_text(film_id);
```

