# Evidencia Fotoaparátov
Pokračovanie word dokumentu, nakolko vo worde sa naozaj zle pracuje s kódom.

<!-- ## Zadanie
Navrhnite databázu vhodnú pre evidenciu fotoaparátov. Bude evidovať pobočky,  fotoaparáty, objektívy a príslušenstvo k fotoaparátom. Fotoaparáty majú rôzne parametre, rovnako ako aj objektívy.  Treba ukladať aj aké produkty sú na akej pobočke.

![Diagram databázy evidencie fotoaparátov](images\DB_RD.jpg) -->

&nbsp;

## 3. Naplnenie tabuliek dátami
``` sql
INSERT INTO ZnackaFotoaparatu(Nazov)
VALUES
('nikon'),
('canon'),
('sony'),
('olympus'),
('panasonic'),
('fujifilm'),
('leica'),
('pentax'),
('hasselblad'),
('sigma'),
('kodak'),
('polaroid'),
('ricoh');
```

``` sql
INSERT INTO TypFotoaparatu(Nazov)
VALUES
('zrkadlovka'),
('bezzrkadlovka'),
('kompakt'),
('instantný'),
('ultrazoom'),
('analóg');
```

``` sql
INSERT INTO Senzor(Nazov, CropFactor)
VALUES
('Full frame', 1.00),
('APS-H', 1.29),
('APS-C', 1.50),
('Foveon', 1.73),
('Micro 4/3', 2.00),
('CX', 2.70),
('2/3"', 3.93),
('1/1.7"', 4.55),
('1/2.3"', 5.62);
```

``` sql
INSERT INTO TypObjektivu(Nazov)
VALUES
('širokouhlý'),
('teleobjektív'),
('rybie oko'),
('makro'),
('potrétny'),
('zoom'),
('tilt-shift'),
('špeciálny');
```

``` sql
INSERT INTO Bajonet(Nazov, ZnackaID)
VALUES
('F', 1),
('F (AF-P)', 1),
('Z', 1),
('EF', 2),
('RF', 2),
('EF-S', 2),
('EF-M', 2),
('PL', 2),
('E', 3),
('FE', 3),
('X', 6),
('G', 6),
('M', 7),
('S', 7),
('T/L', 7),
('654', 8),
('K', 8),
('H', 9),
('X', 9);
```

``` sql
INSERT INTO Pobocka(Nazov)
VALUES
('trenčín'),
('trnava'),
('bratislava'),
('zlín'),
('nitra'),
('poprad'),
('košice');
```

``` sql
INSERT INTO Prislusenstvo(Nazov, Popis)
VALUES
('Vanguard Vesta TB 235AB', 'Nenápadná, kompaktní a lehká sestava cestovního stativu s kulovou hlavou. Navržena pro maximální přenositelnost stále poskytuje stabilní oporu pro většinu DSLR a CSC fotoaparátů. Nohy stativu jsou děleny na pět sekcí. Kulová hlava VESTA T-51 je kompatibilní se systémem rychloupínacích destiček Arca-Swiss. Sestava nabízí celkovou nosnost 4,5 kg. Maximální pracovní výšku 142,2 cm (transportní 37,6 cm). Minimální výška pro makro / fotografování z podhledu je 27,4 cm. Váha 122 g.'),
('Manfrotto MK 055XPRO3-3W SET', 'Spojením stativu 055XPRO3 a třícestné hlavy X-PRO 3W vznikne model Manfrotto MK 055XPRO3-3W, který je určen pro každého amatéra i profesionála. Model Manfrotto MK 055XPRO3-3W nabízí výbornou stabilizaci fotoaparátu, minimalizuje tak působení okolních vibrací a zajišťuje tím dokonale ostré záběry.'),
('Vanguard Alta Pro 263AB 100', 'Vanguard Alta Pro 263AB 100 je kvalitní hliníkový stativ s možností vyosení středové tyče až o 180° a možností nastavení nohou v úhlu 25, 50 a 80°. Stativ je vybaven kulovou hlavou SBH-100 s rychloupínací destičkou QS-39. Maximální výška je 173 cm a složený má 71,5 cm. Nosnost 8kg. Váha 2440 gramů.'),
('Joby GorillaPod 1K Kit', 'GorillaPod 1K je přímou náhradou stativu GorillaPod Hybrid, nejprodávanějšího a nejoblíbenějšího modelu z 1. generace GorillaPod. Nosností 1.000 g se GorillaPod 1K řadí mezi stativy GorillaPod 500 a GorillaPod 3K (dříve SLR-Zoom).'),
('Peak Design Travel Backpack', 'Peak Design Travel Backpack 45L univerzální cestovní batoh pro DSLR i CSC se 4-5 objektivy, rozdělovací panel se zipem umožňuje rozdělení hlavního prostoru na 2 oddíly, vnitřní uspořádání si můžete přizpůsobit doplňkovými obaly, které nejsou součástí balení. Vnější povrch je vyrobený z nylonové tkaniny 400D, která je odolná proti vlivům počasí.'),
('Peak Design Everyday Backpack v2', 'Nová generace již legendárních Everyday batohů Peak Design. Batoh, který s Vámi bude prožívat dobrodružství ve městě i v přírodě. Poradí si s fotovýbavou, notebookem i dronem a svými vychytávkami Vás bude překvapovat ještě dlouho po koupi.'),
('Shimoda Action X70', 'Shimoda Action X70 - outdoorový batoh pro náročného dobrodruha, který vyžaduje něco extra. Starter Kit je rozšířený o Core Unit Extra Large DV. Nastavitelná výška uchycení ramenních popruhů umožňuje každému maximální pohodlí, popruhy jsou vyměnitelné za jiné typy, rozšiřitelný rolovací horní uzávěr pomůže přibalit více oblečení, polstrovaná kapsa na až 15" notebook, popruhy na lyže, kapsy na láhev a stativ, přístup k vybavení ze zádové strany, boční přístup k vybavení, bederní pás je odjímatelný, kapsa na telefon a příslušenství na popruzích, dva odolné držáky nahoře a na boku, spodní panel je odolný vůči vodě a mechanickému poškození, Action X70 je vhodný pro bezzrcadlovky i zrcadlovky.'),
('Shimoda Explore V2', 'Shimoda Explore V2 30 Backpack je ideálním fotobatohem pro každého cestovatele. Díky svým rozměrům hravě splní parametry pro příruční zavadlo do letadla. Batohy Explore V2 jsou vyrobeny ze špičkových materiálů, které chrání techniku před poškozením. Vnější materiály (Ripstop Nylon 420d a 210d pokryty vrstvou pryskyřice) jsou voděodpudivé a zároveň odolné proti fyzickému poškození. Ramenní popruhy jsou ergonomicky tvarované pro co největší pohodlí a zároveň jsou vyrobeny z perforované pěny pro lepší větrání.'),
('Lexar SDXC 64GB 1066x Professional Class 10 UHS-I U3 (V30)', 'Lexar SDXC 64GB 1066x Professional Class 10 UHS-I U3 (V30) - karta vhodná pro fotografie ve vysokém rozlišení nebo pro rychlé sekvenční snímání sportovní fotografie a wild-life. Zároveň je rychlostně vhodná pro záznam videa od FullHD 1080p přes 3D video až po 4K video.'),
('SanDisk SDXC 64GB Extreme Pro 170 MB/s Class 10 UHS-I U3 V30', 'SanDisk SDXC 64GB Extreme Pro 170 MB/s Class 10 UHS-I U3 V30 - extrémně rychlá karta zvyšuje laťku v oblasti rychlosti a výkonu, vylepšuje celkovou integritu dat a spolehlivost karty při čtení a zápisu. Je vhodná pro video vysoké kvality 4K Ultra HD a Full HD video vyšších snímkových frekvencí a datových toků. Součástí je klasický vestavěný přepínač ochrany proti zápisu zamezuje náhodné ztrátě dat.'),
('Sony SDXC Tough SF-M 128GB V60 U3 UHS-II', 'Paměťová karta Sony SDXC Tough SF-M 128GB V60 U3 UHS-II disponuje kapacitou 128GB a využívá sběrnic UHS -II pro podporu pokročilých funkcí DSLR jako je například rychlé fotografování. Karta je vhodná také pro video záběry (8K, 4K XAVC S, AVCHD, 3D HFR a FULL HD). Maximální rychlost čtení dosahuje až 277 MB/s, maximální rychlost zápisu je až 150 MB/s.'),
('Sony SDXC SF-E 128GB Class 10 UHS-II', 'SD karta standardu SDXC UHS-II, kapacita 128 GB, čtecí rychlost až 270 MB/s, zápis 120 MB/s. Class 10. Vhodná pro 4K záznam.'),
('Lexar SDXC 128GB 633x Professional Class 10 UHS-I U1', 'Lexar SDXC 128GB 633x Professional Class 10 UHS-I U1 je rychlá paměťová karta vhodná pro sekvenční snímání fotografií a natáčení FullHD / 3D / 4K videa. Rychlost čtení je 95 MB/s.'),
('DJI RSC 2', 'Jedná se o unikátní stabilizátor pro CSC a DSLR fotoaparáty. Mezi jeho přednosti patří důmyslná skládací konstrukce, která je nejen kompaktních rozměrů, ale i velmi nízké váhy (po složení je RSC 2 menší než formát A5). Spolehlivě pracuje s objektivy do ohniskových vzdáleností 100 mm. Díky tzv. SuperSmoth zvládne i kompenzaci mikropohybů.'),
('Zhiyun Weebill S', 'ZHIYUN Weebill S je určen pro profesionální filmování a monitorování pro bezzrcadlové fotoaparáty a DSLR zrcadlovky. Novinkou u stabilizátoru Weebill S je o 300% vylepšený točivý moment motorů a o 50% zvýšení odezvy. Jedinečný ergonomický režim Sling umožňuje snadno přepínat mezi úhly snímání pomocí sady rychlého nastavení TransMount.'),
('DJI OM 5 šedý', 'DJI OM 5 je všestranný pomocník, který vám dovolí využít kompletní potenciál chytrého telefonu. Pořizujte bezchybná selfie, užijte si plynulá a stabilní videa, automatické sledování objektů a spoustu dalšího. Nová funkce ShotGuides dokonce poskytuje kreativní tipy, díky kterým dokážete zachytit oslňující záběry kdekoliv. Připravte se, s DJI OM 5 zvládnete každý záběr.');
```

``` sql
INSERT INTO Fotoaparat(Nazov, Hmotnost, RokVyroby, SerialNumber, TypFotoaparatuID, SenzorID, ZnackaID)
VALUES
('Canon EOS 2000D', 475, '2018/02/25', 2973795, 1, 3, 2),
('Canon EOS 850D', 515, '2020/02/12', 9497968, 1, 3, 2),
('Canon EOS R6', 680, '2020/07/09', 4289499, 2, 1, 2),
('Canon EOS R', 660, '2018/10/25', 8478936, 2, 1, 2),
('Nikon D3500', 365, '2018/08/30', 6937498, 1, 3, 1),
('Nikon D780', 840, '2020/01/06', 4786684, 1, 1, 1),
('Nikon D5600', 465, '2016/11/24', 6352925, 1, 3, 1),
('Nikon Z50', 450, '2019/10/10', 5942685, 2, 3, 1),
('Sony Alpha A6000', 344, '2014/02/12', 9469588, 2, 3, 3),
('Sony Alpha A6400', 403, '2019/01/17', 9658827, 2, 3, 3),
('Sony Alpha A7 III', 650, '2018/04/10', 9634653, 2, 1, 3),
('Sony CyberShot DSC-RX100 III', 290, '2014/06/01', 7955673, 3, 6, 3),
('Olympus OM-D E-M1 Mark III', 580, '2020/02/28', 8735666, 2, 5, 4),
('Olympus TG-6', 253, '2019/07/25', 3527274, 3, 9, 4),
('Fujifilm X-T4', 526, '2020/04/28', 7959354, 2, 3, 6),
('Fujifilm FinePix X100V', 478, '2020/02/04', 3667222, 3, 3, 6),
('Fujifilm Instax mini 9', 307, '2017/04/10', 5577789, 4, 9, 6),
('Leica D-LUX 7', 403, '2021/03/11', 7836973, 3, 5, 7),
('Leica S', 1260, '2012/12/16', 8798888, 1, 1, 7),
('Pentax K-1 Mark II', 925, '2018/02/17', 9955244, 1, 1, 8),
('Pentax K-3 Mark III', 820, '2021/04/23', 3554543, 1, 3, 8),
('Panasonic Lumix DMC-TZ200', 340, '2018/03/12', 7837656, 5, 6, 5);
```

``` sql
INSERT INTO Objektiv(Nazov, MinOhnisko, MaxOhnisko, MinSvetelnost, MaxSvetelnost, Hmotnost, BajonetID, TypObjektivuID)
VALUES
('Sony FE 28-70 mm f/3,5-5,6 OSS', 28, 70, 3.5, 5.6, 295, 9, 6),
('Nikon 70-300 mm f/4,5–6,3 G AF-P DX ED VR', 70, 300, 4.5, 6.3, 415, 2, 2),
('Nikon 18-140 mm f/3,5-5,6 G ED VR', 18, 140, 3.5, 5.6, 490, 1, 6),
('Nikon 18-55 mm f/3,5-5,6 G AF-P DX  VR', 18, 55, 3.5, 5.6, 205, 2, 5),
('Sigma 24-70 mm f/2,8 DG DN Art', 24, 70, 2.8, 2.8, 835, 9, 5),
('Sony FE 200-600 mm f/5,6-6,3 G OSS - zpětná sleva 2 500 Kč', 200, 600, 5.6, 6.3, 2115, 9, 2),
('Sigma 18-35 mm f/1,8 DC HSM Art', 18, 35, 1.8, 1.8, 810, 6, 3),
('Sony 18-105 mm f/4,0 G OSS SEL', 18, 105, 4.0, 4.0, 427, 9, 6),
('Samyang AF 24-70 mm f/2,8', 24, 70, 2.8, 2.8, 1027, 10, 5),
('Tamron 18-300 mm f/3,5-6,3 Di III-A VC VXD', 18, 300, 3.5, 6.3, 620, 9, 2),
('Sigma 100-400 mm f/5-6.3 DG DN OS Contemporary', 100, 400, 5.0, 6.3, 1140, 9, 2),
('Fujifilm GF 32-64 mm f/4 R LM WR', 32, 64, 4.0, 4.0, 875, 12, 5),
('Fujifilm XF 16-80 mm f/4,0 R OIS WR', 16, 80, 4.0, 4.0, 440, 11, 5),
('Hasselblad HC 50-110 mm f/3,5-4,5', 50, 110, 3.5, 4.5, 1650, 18, 6),
('Hasselblad HCD 35-90 mm f/4,0-5,6', 35, 90, 4.0, 5.6, 1410, 18, 6),
('Hasselblad XCD 35-75 mm f/3,5-4,5', 35, 75, 3.5, 4.5, 1115, 19, 5),
('Leica 30-90 mm f/3,5-5,6 ASPH VARIO ELMAR-S', 30, 90, 3.5, 5.6, 1275, 14, 6),
('Pentax DA 18-270 mm f/3,5-6,3 ED SDM', 18, 270, 3.5, 6.3, 453, 17, 6),
('Pentax DA 18-50 mm f/4 -5,6L DC WR RE', 18, 50, 4.0, 5.6, 158, 17, 6);
```

``` sql
INSERT INTO Fotoaparat_na_pobocke(PobockaID, FotoaparatID)
VALUES
(3, 18),
(4, 26),
(3, 32),
(3, 36),
(4, 36),
(2, 22),
(3, 21),
(6, 32),
(1, 25),
(2, 24),
(1, 21),
(5, 22),
(4, 21),
(5, 27),
(3, 36),
(5, 34),
(2, 34),
(4, 34),
(4, 24),
(1, 36),
(6, 29),
(3, 30),
(3, 21),
(5, 31),
(1, 20),
(6, 31),
(5, 36),
(6, 18),
(3, 31),
(5, 34);
```

``` sql
INSERT INTO Objektiv_na_pobocke(PobockaID, ObjektivID)
VALUES
(3, 18),
(3, 15),
(6, 9),
(1, 18),
(3, 7),
(2, 15),
(6, 2),
(1, 13),
(1, 16),
(1, 4),
(5, 3),
(6, 1),
(5, 2),
(6, 14),
(6, 3),
(6, 9),
(6, 6),
(6, 1),
(1, 9),
(2, 10),
(1, 13),
(2, 4),
(3, 7),
(6, 13),
(4, 2),
(3, 7),
(6, 8),
(1, 13),
(4, 17),
(1, 9);
```

``` sql
INSERT INTO Prislusenstvo_na_pobocke(PobockaID, PrislusenstvoID)
VALUES
(1, 14),
(3, 13),
(6, 2),
(3, 15),
(6, 7),
(2, 4),
(1, 1),
(5, 10),
(4, 1),
(6, 4),
(1, 8),
(2, 12),
(6, 5),
(2, 13),
(4, 9),
(4, 8),
(2, 8),
(5, 3),
(3, 3),
(1, 10),
(6, 11),
(2, 14),
(2, 14),
(3, 6),
(1, 5),
(5, 7),
(1, 7),
(6, 10),
(6, 2),
(5, 6);
```
&nbsp;

## 5. Dotazy
``` sql
-- 1. Vypis vsetky fotaky s Full frame senzorom.

SELECT
    *
FROM
    Fotoaparat
WHERE
    SenzorID = (SELECT SenzorID FROM Senzor WHERE Nazov = 'Full frame');
```
![Query No.1](https://github.com/AstroTitanus/evidencia_fotoaparatov/blob/main/images/Q1.png?raw=True)


&nbsp;
``` sql
-- 2. Vypis vsetky objektivy pre fotaky znacky Sony | toto je mozne aj cez jeden join a jeden vnoreny dotaz

SELECT
    o.Nazov,
    b.Nazov as Bajonet,
    z.Nazov as Znacka
FROM
    Objektiv as o
    JOIN Bajonet as b ON o.BajonetID = b.BajonetID
    JOIN ZnackaFotoaparatu as z ON b.ZnackaID = z.znackaID
WHERE
    z.Nazov = 'sony';
```
![Query No.2](https://github.com/AstroTitanus/evidencia_fotoaparatov/blob/main/images/Q2.png?raw=True)


&nbsp;
``` sql
-- 3. Vypis vsetky dostupne fotaky na pobocke trencin

SELECT
    f.Nazov
FROM
    Fotoaparat_na_pobocke as fnp
    JOIN Fotoaparat as f ON fnp.FotoaparatID = f.FotoaparatID
WHERE
    PobockaID = (SELECT PobockaID FROM Pobocka WHERE Nazov = 'trenčín');
```
![Query No.3](https://github.com/AstroTitanus/evidencia_fotoaparatov/blob/main/images/Q3.png?raw=True)


&nbsp;
``` sql
-- 4. Vypis vsetky zrkadlovky a zorad ich od najnovsej po najstarsiu

SELECT
    *
FROM
    Fotoaparat
WHERE
    TypFotoaparatuID = (SELECT TypFotoaparatuID FROM TypFotoaparatu WHERE Nazov = 'zrkadlovka')
ORDER BY
    RokVyroby DESC;
```
![Query No.4](https://github.com/AstroTitanus/evidencia_fotoaparatov/blob/main/images/Q4.png?raw=True)


&nbsp;
``` sql
-- 5. Vypis kolko bezzrkadloviek je na pobecka zlin

SELECT
    COUNT(1) as pocet_bezzrkadloviek
FROM
    Fotoaparat_na_pobocke as fnp
    JOIN Fotoaparat as f ON fnp.FotoaparatID = f.FotoaparatID
WHERE
    fnp.PobockaID = (SELECT PobockaID FROM Pobocka WHERE Nazov = 'zlín')
    AND
    f.TypFotoaparatuID = (SELECT TypFotoaparatuID FROM TypFotoaparatu WHERE Nazov = 'bezzrkadlovka');
```
![Query No.5](https://github.com/AstroTitanus/evidencia_fotoaparatov/blob/main/images/Q5.png?raw=True)


&nbsp;
``` sql
-- 6. Vypis ktora pobocka ma kolko objektivov

SELECT
	UPPER(LEFT(p.Nazov,1))+LOWER(SUBSTRING(p.Nazov,2,LEN(p.Nazov))) as Capitalized_nazov,
    COUNT(onp.PobockaID) as pocet_objektivov
FROM
    Objektiv_na_pobocke as onp
    JOIN Pobocka as p ON onp.PobockaID = p.PobockaID
GROUP BY
	onp.PobockaID,
	p.Nazov;
```
![Query No.6](https://github.com/AstroTitanus/evidencia_fotoaparatov/blob/main/images/Q6.png?raw=True)


&nbsp;
``` sql
-- 7. Vypis pobocku, ktora ma na sklade najviac veci | How do I do this with joins?

SELECT TOP 1 a.PobockaID, a.item_count + b.item_count + c.item_count as total_count FROM

(
    SELECT p.PobockaID, COUNT(p.pobockaID) as item_count FROM Pobocka as p
    JOIN Prislusenstvo_na_pobocke as pnp ON p.PobockaID = pnp.PobockaID
    GROUP BY p.PobockaID
) as a

JOIN

(
    SELECT p.PobockaID, COUNT(p.pobockaID) as item_count FROM Pobocka as p
    JOIN Objektiv_na_pobocke as onp ON p.PobockaID = onp.PobockaID
    GROUP BY p.PobockaID
) as b ON a.PobockaID = b.PobockaID

JOIN

(
    SELECT p.PobockaID, COUNT(p.pobockaID) as item_count FROM Pobocka as p
    JOIN Fotoaparat_na_pobocke as fnp ON p.PobockaID = fnp.PobockaID
    GROUP BY p.PobockaID
) as c ON b.PobockaID = c.PobockaID

ORDER BY total_count DESC;
```
![Query No.7](https://github.com/AstroTitanus/evidencia_fotoaparatov/blob/main/images/Q7.png?raw=True)


&nbsp;
``` sql
-- 8. Pocet fotakov pri jednotlivych znackach

SELECT
    zf.Nazov,
    COUNT(zf.Nazov) as pocet
FROM
    Fotoaparat as f
    JOIN ZnackaFotoaparatu as zf ON f.ZnackaID = zf.ZnackaID
    JOIN TypFotoaparatu as tf ON f.TypFotoaparatuID = tf.TypFotoaparatuID
GROUP BY
    zf.Nazov;
```
![Query No.8](https://github.com/AstroTitanus/evidencia_fotoaparatov/blob/main/images/Q8.png?raw=True)


&nbsp;
``` sql
-- 9. Kolko objektivov isteho typu je na predajni bratislava 

SELECT
    typo.Nazov,
    COUNT(typo.Nazov) as pocet
FROM
    Objektiv_na_pobocke as onp
    JOIN Objektiv as o ON onp.ObjektivID = o.ObjektivID
    JOIN TypObjektivu as typo ON o.TypObjektivuID = typo.TypObjektivuID
WHERE
    onp.PobockaID = (SELECT PobockaID FROM Pobocka WHERE Nazov = 'bratislava')
GROUP BY
    typo.Nazov;
```
![Query No.9](https://github.com/AstroTitanus/evidencia_fotoaparatov/blob/main/images/Q9.png?raw=True)


&nbsp;
``` sql
-- 10. Pridaj fotoaparat na predajnu

INSERT INTO Fotoaparat_na_pobocke(PobockaID, FotoaparatID)
VALUES (3, 18);
```


&nbsp;
``` sql
-- 11. Pridaj stlpec 'Hmotnost' do tabulky 'Prislusenstvo'

ALTER TABLE Prislusenstvo
ADD Hmotnost INT NULL;
```


&nbsp;
``` sql
-- 12. Zmen hmotnost prvym piatim zaznamom v prislusenstve

UPDATE TOP (5) Prislusenstvo
SET Hmotnost = 100

SELECT * FROM Prislusenstvo
```
![Query No.12](https://github.com/AstroTitanus/evidencia_fotoaparatov/blob/main/images/Q12.png?raw=True)


&nbsp;
``` sql
-- 13. Zmaz vsetky zaznamu prislusenstva na pobocke, ktorych prislusenstvo nemaja hmotnost.

DELETE pnp
FROM
    Prislusenstvo_na_pobocke as pnp
    JOIN Prislusenstvo as p ON pnp.PrislusenstvoID = p.PrislusenstvoID
WHERE
    p.Hmotnost IS NULL
```


&nbsp;
``` sql
-- 14. Vyber prislusenstvo s najdlhsim popisom

SELECT
    TOP 1 PrislusenstvoID,
    Nazov,
    Popis,
    LEN(p.Popis) as popis_len
FROM
    Prislusenstvo as p
Group BY
    PrislusenstvoID,
    Nazov,
    Popis
ORDER BY
    popis_len DESC
```
![Query No.14](https://github.com/AstroTitanus/evidencia_fotoaparatov/blob/main/images/Q14.png?raw=True)


&nbsp;
``` sql
-- 15. Vyber vsetky objektivy kompatibilne s fotakmi na jednej predajni

SELECT DISTINCT * FROM 
(
	SELECT o.Nazov, zf.ZnackaID FROM Objektiv_na_pobocke as onp
	JOIN Objektiv as o ON onp.ObjektivID = o.ObjektivID
	JOIN Bajonet as b ON o.BajonetID = b.BajonetID
	JOIN ZnackaFotoaparatu as zf ON b.ZnackaID = zf.ZnackaID
	WHERE onp.PobockaID = (SELECT PobockaID FROM Pobocka WHERE Nazov = 'bratislava')
) as a
JOIN
(
	SELECT f.Nazov, zf.ZnackaID FROM Fotoaparat_na_pobocke as fnp
	JOIN Fotoaparat as f ON fnp.FotoaparatID = f.FotoaparatID
	JOIN ZnackaFotoaparatu as zf ON f.ZnackaID = zf.ZnackaID
	WHERE fnp.PobockaID = (SELECT PobockaID FROM Pobocka WHERE Nazov = 'bratislava')
) as b ON a.ZnackaID = b.ZnackaID

-- -------------------------------- --
-- Druha varianta? 
SELECT
    DISTINCT o.Nazov,
    zf.ZnackaID
FROM
    Objektiv_na_pobocke as onp
    JOIN Objektiv as o ON onp.ObjektivID = o.ObjektivID
    JOIN Bajonet as b ON o.BajonetID = b.BajonetID
    JOIN ZnackaFotoaparatu as zf ON b.ZnackaID = zf.ZnackaID
    JOIN Fotoaparat as f ON zf.ZnackaID = f.ZnackaID
    JOIN Fotoaparat_na_pobocke as fnp ON f.FotoaparatID = fnp.FotoaparatID
WHERE
    onp.PobockaID = (SELECT PobockaID FROM Pobocka WHERE Nazov = 'bratislava')
    AND fnp.PobockaID = (SELECT PobockaID FROM Pobocka WHERE Nazov = 'bratislava')
```
![Query No.15](https://github.com/AstroTitanus/evidencia_fotoaparatov/blob/main/images/Q15.png?raw=True)