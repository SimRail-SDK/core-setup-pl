# SimRail Core SDK Setup - Poland

This is the *Core SDK Setup* for the Polish map in SimRail.

This module is meant to be used with the [*Core SDK*](https://github.com/simrail-sdk/core "View on GitHub") ([`@simrail-sdk/core`](https://github.com/simrail-sdk/core "View on GitHub")).

You only need to install this if you:
- Use TypeScript and want strict typing for:
    - Line numbers.
    - Server codes.
    - Station codes.
    - Train numbers.
- Use JavaScript and want to obtain:
    - Server codes.
    - Station codes.

If you are looking for the *SDK Setup* for Poland, ~~check out~~ *wait for* the module [`@simrail-sdk/sdk-setup-pl`](https://github.com/simrail-sdk/sdk-setup-pl "View on GitHub").

<br/>
<br/>


## Content index

- [Usage details][usage-details]

    - [Installation][installation]

    - [Examples][examples]

        - [Usage with the Core SDK][usage-with-the-core-sdk]

- [API reference][api-reference]

- [About this module][about-this-module]

    - [Module dependencies][module-dependencies]

        - [Module package dependencies][module-package-dependencies]

        - [Internal module dependencies][internal-module-dependencies]

    - [Module code statistics][module-code-statistics]
<br/>
<br/>


## [Usage details][usage-details]

[usage-details]: #usage-details "View Usage details"

### [Installation][installation]

[installation]: #installation "View Installation"

Using NPM:

`$ npm i @simrail-sdk/core-setup-pl`

or

`$ npm i github:simrail-sdk/core-setup-pl#VERSION`

Where `VERSION` specifies the version to install.
<br/>
<br/>


### [Examples][examples]

[examples]: #examples "View Examples"

#### [Usage with the Core SDK][usage-with-the-core-sdk]

[usage-with-the-core-sdk]: #usage-with-the-core-sdk "View Usage with the Core SDK"

```TypeScript
import { Sdk } from "@simrail-sdk/core";
import { Server, Station, Types } from "@simrail-sdk/core-setup-pl";

// Inject `Types` into the `Sdk` instance to enable strict type checking.
const sdk = new Sdk<Types>(...);

const en1 = sdk.server(Server.Code.EN1);
const en2 = sdk.server("en2");

const będzin     = sdk.station("en1", Station.Code.B);
const düsseldorf = sdk.station("en1", "Dü"); // <-- Fails because Düsseldorf doesn't exist.
const katowice   = sdk.station("en1", "KO");

const train4144 = sdk.train("en1", "4144");
const train4145 = sdk.train("en1", "4145"); // <-- Fails because 4145 doesn't exist.

// Obtaining a list of server/station codes:
const serverCodes  = Object.values(Server.Code);
const stationCodes = Object.values(Station.Code);

```
<br/>
<br/>


## [API reference][api-reference]

[api-reference]: #api-reference "View API reference"

<span style="color: #ff3300;">**NOTE**</span>: The API reference section doesn't account for `namespace`s, this unfortunately means the documentation below is not entirely complete. Please investigate the TypeScript definition files for the full API.

- [`enum Code`][api-reference-index.ts~Code]

    - [`member Code.B`][api-reference-index.ts~Code.B]

    - [`member Code.BR`][api-reference-index.ts~Code.BR]

    - [`member Code.Bo`][api-reference-index.ts~Code.Bo]

    - [`member Code.DG`][api-reference-index.ts~Code.DG]

    - [`member Code.DGHK`][api-reference-index.ts~Code.DGHK]

    - [`member Code.DW`][api-reference-index.ts~Code.DW]

    - [`member Code.DZ`][api-reference-index.ts~Code.DZ]

    - [`member Code.Dra`][api-reference-index.ts~Code.Dra]

    - [`member Code.GW`][api-reference-index.ts~Code.GW]

    - [`member Code.Gr`][api-reference-index.ts~Code.Gr]

    - [`member Code.Id`][api-reference-index.ts~Code.Id]

    - [`member Code.Ju`][api-reference-index.ts~Code.Ju]

    - [`member Code.KO`][api-reference-index.ts~Code.KO]

    - [`member Code.KZ`][api-reference-index.ts~Code.KZ]

    - [`member Code.Kn`][api-reference-index.ts~Code.Kn]

    - [`member Code.Kr`][api-reference-index.ts~Code.Kr]

    - [`member Code.Kz`][api-reference-index.ts~Code.Kz]

    - [`member Code.LA`][api-reference-index.ts~Code.LA]

    - [`member Code.LB`][api-reference-index.ts~Code.LB]

    - [`member Code.LC`][api-reference-index.ts~Code.LC]

    - [`member Code.Ol`][api-reference-index.ts~Code.Ol]

    - [`member Code.Op`][api-reference-index.ts~Code.Op]

    - [`member Code.Pi`][api-reference-index.ts~Code.Pi]

    - [`member Code.Pr`][api-reference-index.ts~Code.Pr]

    - [`member Code.Ps`][api-reference-index.ts~Code.Ps]

    - [`member Code.SG`][api-reference-index.ts~Code.SG]

    - [`member Code.SKz`][api-reference-index.ts~Code.SKz]

    - [`member Code.Se`][api-reference-index.ts~Code.Se]

    - [`member Code.Sl`][api-reference-index.ts~Code.Sl]

    - [`member Code.Spl1`][api-reference-index.ts~Code.Spl1]

    - [`member Code.St`][api-reference-index.ts~Code.St]

    - [`member Code.Tl`][api-reference-index.ts~Code.Tl]

    - [`member Code.WP`][api-reference-index.ts~Code.WP]

    - [`member Code.Zw`][api-reference-index.ts~Code.Zw]

- [`enum Number`][api-reference-index.ts~Number]

    - [`member Number.L1`][api-reference-index.ts~Number.L1]

    - [`member Number.L12`][api-reference-index.ts~Number.L12]

    - [`member Number.L130`][api-reference-index.ts~Number.L130]

    - [`member Number.L131`][api-reference-index.ts~Number.L131]

    - [`member Number.L132`][api-reference-index.ts~Number.L132]

    - [`member Number.L133`][api-reference-index.ts~Number.L133]

    - [`member Number.L134`][api-reference-index.ts~Number.L134]

    - [`member Number.L137`][api-reference-index.ts~Number.L137]

    - [`member Number.L138`][api-reference-index.ts~Number.L138]

    - [`member Number.L139`][api-reference-index.ts~Number.L139]

    - [`member Number.L140`][api-reference-index.ts~Number.L140]

    - [`member Number.L141`][api-reference-index.ts~Number.L141]

    - [`member Number.L142`][api-reference-index.ts~Number.L142]

    - [`member Number.L143`][api-reference-index.ts~Number.L143]

    - [`member Number.L144`][api-reference-index.ts~Number.L144]

    - [`member Number.L149`][api-reference-index.ts~Number.L149]

    - [`member Number.L15`][api-reference-index.ts~Number.L15]

    - [`member Number.L151`][api-reference-index.ts~Number.L151]

    - [`member Number.L154`][api-reference-index.ts~Number.L154]

    - [`member Number.L155`][api-reference-index.ts~Number.L155]

    - [`member Number.L158`][api-reference-index.ts~Number.L158]

    - [`member Number.L16`][api-reference-index.ts~Number.L16]

    - [`member Number.L160`][api-reference-index.ts~Number.L160]

    - [`member Number.L162`][api-reference-index.ts~Number.L162]

    - [`member Number.L163`][api-reference-index.ts~Number.L163]

    - [`member Number.L164`][api-reference-index.ts~Number.L164]

    - [`member Number.L17`][api-reference-index.ts~Number.L17]

    - [`member Number.L171`][api-reference-index.ts~Number.L171]

    - [`member Number.L179`][api-reference-index.ts~Number.L179]

    - [`member Number.L18`][api-reference-index.ts~Number.L18]

    - [`member Number.L186`][api-reference-index.ts~Number.L186]

    - [`member Number.L19`][api-reference-index.ts~Number.L19]

    - [`member Number.L2`][api-reference-index.ts~Number.L2]

    - [`member Number.L20`][api-reference-index.ts~Number.L20]

    - [`member Number.L22`][api-reference-index.ts~Number.L22]

    - [`member Number.L25`][api-reference-index.ts~Number.L25]

    - [`member Number.L272`][api-reference-index.ts~Number.L272]

    - [`member Number.L276`][api-reference-index.ts~Number.L276]

    - [`member Number.L280`][api-reference-index.ts~Number.L280]

    - [`member Number.L3`][api-reference-index.ts~Number.L3]

    - [`member Number.L301`][api-reference-index.ts~Number.L301]

    - [`member Number.L4`][api-reference-index.ts~Number.L4]

    - [`member Number.L447`][api-reference-index.ts~Number.L447]

    - [`member Number.L45`][api-reference-index.ts~Number.L45]

    - [`member Number.L479`][api-reference-index.ts~Number.L479]

    - [`member Number.L501`][api-reference-index.ts~Number.L501]

    - [`member Number.L509`][api-reference-index.ts~Number.L509]

    - [`member Number.L529`][api-reference-index.ts~Number.L529]

    - [`member Number.L540`][api-reference-index.ts~Number.L540]

    - [`member Number.L546`][api-reference-index.ts~Number.L546]

    - [`member Number.L570`][api-reference-index.ts~Number.L570]

    - [`member Number.L571`][api-reference-index.ts~Number.L571]

    - [`member Number.L572`][api-reference-index.ts~Number.L572]

    - [`member Number.L573`][api-reference-index.ts~Number.L573]

    - [`member Number.L574`][api-reference-index.ts~Number.L574]

    - [`member Number.L6`][api-reference-index.ts~Number.L6]

    - [`member Number.L607`][api-reference-index.ts~Number.L607]

    - [`member Number.L61`][api-reference-index.ts~Number.L61]

    - [`member Number.L62`][api-reference-index.ts~Number.L62]

    - [`member Number.L64`][api-reference-index.ts~Number.L64]

    - [`member Number.L651`][api-reference-index.ts~Number.L651]

    - [`member Number.L652`][api-reference-index.ts~Number.L652]

    - [`member Number.L657`][api-reference-index.ts~Number.L657]

    - [`member Number.L660`][api-reference-index.ts~Number.L660]

    - [`member Number.L661`][api-reference-index.ts~Number.L661]

    - [`member Number.L663`][api-reference-index.ts~Number.L663]

    - [`member Number.L668`][api-reference-index.ts~Number.L668]

    - [`member Number.L687`][api-reference-index.ts~Number.L687]

    - [`member Number.L696`][api-reference-index.ts~Number.L696]

    - [`member Number.L703`][api-reference-index.ts~Number.L703]

    - [`member Number.L713`][api-reference-index.ts~Number.L713]

    - [`member Number.L717`][api-reference-index.ts~Number.L717]

    - [`member Number.L73`][api-reference-index.ts~Number.L73]

    - [`member Number.L8`][api-reference-index.ts~Number.L8]

    - [`member Number.L836`][api-reference-index.ts~Number.L836]

    - [`member Number.L839`][api-reference-index.ts~Number.L839]

    - [`member Number.L898`][api-reference-index.ts~Number.L898]

    - [`member Number.L9`][api-reference-index.ts~Number.L9]

    - [`member Number.L95`][api-reference-index.ts~Number.L95]

- [`interface Types`][api-reference-index.ts~Types]

    - [`property Types.lineNumbers`][api-reference-index.ts~Types.lineNumbers]

    - [`property Types.serverCodes`][api-reference-index.ts~Types.serverCodes]

    - [`property Types.stationCodes`][api-reference-index.ts~Types.stationCodes]

    - [`property Types.trainNumbers`][api-reference-index.ts~Types.trainNumbers]

- [`type Number`][api-reference-index.ts~Number]

<br/>
<br/>
<br/>

[api-reference-@simrail-sdk/core-setup-pl]: @simrail-sdk/core-setup-pl "View module \"@simrail-sdk/core-setup-pl\""
[api-reference-index]: index "View module \"index\""
[api-reference-index.d.ts]: index.d.ts "View module \"index.d.ts\""
[api-reference-index.ts]: index.ts "View module \"index.ts\""

### [`enum Code`][api-reference-index.ts~Code]&nbsp;&nbsp;&nbsp;[&uarr;][api-reference]

[api-reference-index.ts~Code]: #enum-code&nbsp;&nbsp;&nbsp;&uarr; "View enum Code"

Specifies the code of a dispatch station.

**Since**: `0.1.0`

**Definition**:&nbsp;&nbsp;[index.ts:56][api-reference-index.ts]

<br/>
<br/>

#### [`member Code.B`][api-reference-index.ts~Code.B]&nbsp;&nbsp;&nbsp;[&uarr;][api-reference]

[api-reference-index.ts~Code.B]: #member-codeb&nbsp;&nbsp;&nbsp;&uarr; "View member Code.B"

Będzin

**Type**:&nbsp;&nbsp;<code>`"B"`</code>

**Since**: `0.1.0`

**Definition**:&nbsp;&nbsp;[index.ts:58][api-reference-index.ts]

<br/>

<br/>

#### [`member Code.BR`][api-reference-index.ts~Code.BR]&nbsp;&nbsp;&nbsp;[&uarr;][api-reference]

[api-reference-index.ts~Code.BR]: #member-codebr&nbsp;&nbsp;&nbsp;&uarr; "View member Code.BR"

Biała Rawska

**Type**:&nbsp;&nbsp;<code>`"BR"`</code>

**Since**: `0.1.0`

**Definition**:&nbsp;&nbsp;[index.ts:60][api-reference-index.ts]

<br/>

<br/>

#### [`member Code.Bo`][api-reference-index.ts~Code.Bo]&nbsp;&nbsp;&nbsp;[&uarr;][api-reference]

[api-reference-index.ts~Code.Bo]: #member-codebo&nbsp;&nbsp;&nbsp;&uarr; "View member Code.Bo"

Bukowno

**Type**:&nbsp;&nbsp;<code>`"Bo"`</code>

**Since**: `0.1.0`

**Definition**:&nbsp;&nbsp;[index.ts:62][api-reference-index.ts]

<br/>

<br/>

#### [`member Code.DG`][api-reference-index.ts~Code.DG]&nbsp;&nbsp;&nbsp;[&uarr;][api-reference]

[api-reference-index.ts~Code.DG]: #member-codedg&nbsp;&nbsp;&nbsp;&uarr; "View member Code.DG"

Dąbrowa Górnicza

**Type**:&nbsp;&nbsp;<code>`"DG"`</code>

**Since**: `0.1.0`

**Definition**:&nbsp;&nbsp;[index.ts:64][api-reference-index.ts]

<br/>

<br/>

#### [`member Code.DGHK`][api-reference-index.ts~Code.DGHK]&nbsp;&nbsp;&nbsp;[&uarr;][api-reference]

[api-reference-index.ts~Code.DGHK]: #member-codedghk&nbsp;&nbsp;&nbsp;&uarr; "View member Code.DGHK"

Dąbrowa Górnicza Huta Katowice

**Type**:&nbsp;&nbsp;<code>`"DGHK"`</code>

**Since**: `0.1.0`

**Definition**:&nbsp;&nbsp;[index.ts:66][api-reference-index.ts]

<br/>

<br/>

#### [`member Code.DW`][api-reference-index.ts~Code.DW]&nbsp;&nbsp;&nbsp;[&uarr;][api-reference]

[api-reference-index.ts~Code.DW]: #member-codedw&nbsp;&nbsp;&nbsp;&uarr; "View member Code.DW"

Dąbrowa Górnicza Wschodnia

**Type**:&nbsp;&nbsp;<code>`"DW"`</code>

**Since**: `0.1.0`

**Definition**:&nbsp;&nbsp;[index.ts:68][api-reference-index.ts]

<br/>

<br/>

#### [`member Code.DZ`][api-reference-index.ts~Code.DZ]&nbsp;&nbsp;&nbsp;[&uarr;][api-reference]

[api-reference-index.ts~Code.DZ]: #member-codedz&nbsp;&nbsp;&nbsp;&uarr; "View member Code.DZ"

Dąbrowa Górnicza Ząbkowice

**Type**:&nbsp;&nbsp;<code>`"DZ"`</code>

**Since**: `0.1.0`

**Definition**:&nbsp;&nbsp;[index.ts:70][api-reference-index.ts]

<br/>

<br/>

#### [`member Code.Dra`][api-reference-index.ts~Code.Dra]&nbsp;&nbsp;&nbsp;[&uarr;][api-reference]

[api-reference-index.ts~Code.Dra]: #member-codedra&nbsp;&nbsp;&nbsp;&uarr; "View member Code.Dra"

Dorota

**Type**:&nbsp;&nbsp;<code>`"Dra"`</code>

**Since**: `0.1.0`

**Definition**:&nbsp;&nbsp;[index.ts:72][api-reference-index.ts]

<br/>

<br/>

#### [`member Code.GW`][api-reference-index.ts~Code.GW]&nbsp;&nbsp;&nbsp;[&uarr;][api-reference]

[api-reference-index.ts~Code.GW]: #member-codegw&nbsp;&nbsp;&nbsp;&uarr; "View member Code.GW"

Góra Włodowska

**Type**:&nbsp;&nbsp;<code>`"GW"`</code>

**Since**: `0.1.0`

**Definition**:&nbsp;&nbsp;[index.ts:74][api-reference-index.ts]

<br/>

<br/>

#### [`member Code.Gr`][api-reference-index.ts~Code.Gr]&nbsp;&nbsp;&nbsp;[&uarr;][api-reference]

[api-reference-index.ts~Code.Gr]: #member-codegr&nbsp;&nbsp;&nbsp;&uarr; "View member Code.Gr"

Grodzisk Mazowiecki

**Type**:&nbsp;&nbsp;<code>`"Gr"`</code>

**Since**: `0.1.0`

**Definition**:&nbsp;&nbsp;[index.ts:76][api-reference-index.ts]

<br/>

<br/>

#### [`member Code.Id`][api-reference-index.ts~Code.Id]&nbsp;&nbsp;&nbsp;[&uarr;][api-reference]

[api-reference-index.ts~Code.Id]: #member-codeid&nbsp;&nbsp;&nbsp;&uarr; "View member Code.Id"

Idzikowice

**Type**:&nbsp;&nbsp;<code>`"Id"`</code>

**Since**: `0.1.0`

**Definition**:&nbsp;&nbsp;[index.ts:78][api-reference-index.ts]

<br/>

<br/>

#### [`member Code.Ju`][api-reference-index.ts~Code.Ju]&nbsp;&nbsp;&nbsp;[&uarr;][api-reference]

[api-reference-index.ts~Code.Ju]: #member-codeju&nbsp;&nbsp;&nbsp;&uarr; "View member Code.Ju"

Juliusz

**Type**:&nbsp;&nbsp;<code>`"Ju"`</code>

**Since**: `0.1.0`

**Definition**:&nbsp;&nbsp;[index.ts:80][api-reference-index.ts]

<br/>

<br/>

#### [`member Code.KO`][api-reference-index.ts~Code.KO]&nbsp;&nbsp;&nbsp;[&uarr;][api-reference]

[api-reference-index.ts~Code.KO]: #member-codeko&nbsp;&nbsp;&nbsp;&uarr; "View member Code.KO"

Katowice

**Type**:&nbsp;&nbsp;<code>`"KO"`</code>

**Since**: `0.1.0`

**Definition**:&nbsp;&nbsp;[index.ts:82][api-reference-index.ts]

<br/>

<br/>

#### [`member Code.KZ`][api-reference-index.ts~Code.KZ]&nbsp;&nbsp;&nbsp;[&uarr;][api-reference]

[api-reference-index.ts~Code.KZ]: #member-codekz&nbsp;&nbsp;&nbsp;&uarr; "View member Code.KZ"

Katowice Zawodzie

**Type**:&nbsp;&nbsp;<code>`"KZ"`</code>

**Since**: `0.1.0`

**Definition**:&nbsp;&nbsp;[index.ts:84][api-reference-index.ts]

<br/>

<br/>

#### [`member Code.Kn`][api-reference-index.ts~Code.Kn]&nbsp;&nbsp;&nbsp;[&uarr;][api-reference]

[api-reference-index.ts~Code.Kn]: #member-codekn&nbsp;&nbsp;&nbsp;&uarr; "View member Code.Kn"

Knapówka

**Type**:&nbsp;&nbsp;<code>`"Kn"`</code>

**Since**: `0.1.0`

**Definition**:&nbsp;&nbsp;[index.ts:86][api-reference-index.ts]

<br/>

<br/>

#### [`member Code.Kr`][api-reference-index.ts~Code.Kr]&nbsp;&nbsp;&nbsp;[&uarr;][api-reference]

[api-reference-index.ts~Code.Kr]: #member-codekr&nbsp;&nbsp;&nbsp;&uarr; "View member Code.Kr"

Korytów

**Type**:&nbsp;&nbsp;<code>`"Kr"`</code>

**Since**: `0.1.0`

**Definition**:&nbsp;&nbsp;[index.ts:88][api-reference-index.ts]

<br/>

<br/>

#### [`member Code.Kz`][api-reference-index.ts~Code.Kz]&nbsp;&nbsp;&nbsp;[&uarr;][api-reference]

[api-reference-index.ts~Code.Kz]: #member-codekz&nbsp;&nbsp;&nbsp;&uarr; "View member Code.Kz"

Kozłów

**Type**:&nbsp;&nbsp;<code>`"Kz"`</code>

**Since**: `0.1.0`

**Definition**:&nbsp;&nbsp;[index.ts:90][api-reference-index.ts]

<br/>

<br/>

#### [`member Code.LA`][api-reference-index.ts~Code.LA]&nbsp;&nbsp;&nbsp;[&uarr;][api-reference]

[api-reference-index.ts~Code.LA]: #member-codela&nbsp;&nbsp;&nbsp;&uarr; "View member Code.LA"

Łazy Ła

**Type**:&nbsp;&nbsp;<code>`"LA"`</code>

**Since**: `0.1.0`

**Definition**:&nbsp;&nbsp;[index.ts:92][api-reference-index.ts]

<br/>

<br/>

#### [`member Code.LB`][api-reference-index.ts~Code.LB]&nbsp;&nbsp;&nbsp;[&uarr;][api-reference]

[api-reference-index.ts~Code.LB]: #member-codelb&nbsp;&nbsp;&nbsp;&uarr; "View member Code.LB"

Łazy

**Type**:&nbsp;&nbsp;<code>`"LB"`</code>

**Since**: `0.1.0`

**Definition**:&nbsp;&nbsp;[index.ts:94][api-reference-index.ts]

<br/>

<br/>

#### [`member Code.LC`][api-reference-index.ts~Code.LC]&nbsp;&nbsp;&nbsp;[&uarr;][api-reference]

[api-reference-index.ts~Code.LC]: #member-codelc&nbsp;&nbsp;&nbsp;&uarr; "View member Code.LC"

Łazy Łc

**Type**:&nbsp;&nbsp;<code>`"LC"`</code>

**Since**: `0.1.0`

**Definition**:&nbsp;&nbsp;[index.ts:96][api-reference-index.ts]

<br/>

<br/>

#### [`member Code.Ol`][api-reference-index.ts~Code.Ol]&nbsp;&nbsp;&nbsp;[&uarr;][api-reference]

[api-reference-index.ts~Code.Ol]: #member-codeol&nbsp;&nbsp;&nbsp;&uarr; "View member Code.Ol"

Olszamowice

**Type**:&nbsp;&nbsp;<code>`"Ol"`</code>

**Since**: `0.1.0`

**Definition**:&nbsp;&nbsp;[index.ts:98][api-reference-index.ts]

<br/>

<br/>

#### [`member Code.Op`][api-reference-index.ts~Code.Op]&nbsp;&nbsp;&nbsp;[&uarr;][api-reference]

[api-reference-index.ts~Code.Op]: #member-codeop&nbsp;&nbsp;&nbsp;&uarr; "View member Code.Op"

Opoczno Południe

**Type**:&nbsp;&nbsp;<code>`"Op"`</code>

**Since**: `0.1.0`

**Definition**:&nbsp;&nbsp;[index.ts:100][api-reference-index.ts]

<br/>

<br/>

#### [`member Code.Pi`][api-reference-index.ts~Code.Pi]&nbsp;&nbsp;&nbsp;[&uarr;][api-reference]

[api-reference-index.ts~Code.Pi]: #member-codepi&nbsp;&nbsp;&nbsp;&uarr; "View member Code.Pi"

Pilichowice

**Type**:&nbsp;&nbsp;<code>`"Pi"`</code>

**Since**: `0.1.0`

**Definition**:&nbsp;&nbsp;[index.ts:102][api-reference-index.ts]

<br/>

<br/>

#### [`member Code.Pr`][api-reference-index.ts~Code.Pr]&nbsp;&nbsp;&nbsp;[&uarr;][api-reference]

[api-reference-index.ts~Code.Pr]: #member-codepr&nbsp;&nbsp;&nbsp;&uarr; "View member Code.Pr"

Pruszków

**Type**:&nbsp;&nbsp;<code>`"Pr"`</code>

**Since**: `0.1.0`

**Definition**:&nbsp;&nbsp;[index.ts:104][api-reference-index.ts]

<br/>

<br/>

#### [`member Code.Ps`][api-reference-index.ts~Code.Ps]&nbsp;&nbsp;&nbsp;[&uarr;][api-reference]

[api-reference-index.ts~Code.Ps]: #member-codeps&nbsp;&nbsp;&nbsp;&uarr; "View member Code.Ps"

Psary

**Type**:&nbsp;&nbsp;<code>`"Ps"`</code>

**Since**: `0.1.0`

**Definition**:&nbsp;&nbsp;[index.ts:106][api-reference-index.ts]

<br/>

<br/>

#### [`member Code.SG`][api-reference-index.ts~Code.SG]&nbsp;&nbsp;&nbsp;[&uarr;][api-reference]

[api-reference-index.ts~Code.SG]: #member-codesg&nbsp;&nbsp;&nbsp;&uarr; "View member Code.SG"

Sosnowiec Główny

**Type**:&nbsp;&nbsp;<code>`"SG"`</code>

**Since**: `0.1.0`

**Definition**:&nbsp;&nbsp;[index.ts:108][api-reference-index.ts]

<br/>

<br/>

#### [`member Code.SKz`][api-reference-index.ts~Code.SKz]&nbsp;&nbsp;&nbsp;[&uarr;][api-reference]

[api-reference-index.ts~Code.SKz]: #member-codeskz&nbsp;&nbsp;&nbsp;&uarr; "View member Code.SKz"

Sosnowiec Kazimierz

**Type**:&nbsp;&nbsp;<code>`"SKz"`</code>

**Since**: `0.1.0`

**Definition**:&nbsp;&nbsp;[index.ts:110][api-reference-index.ts]

<br/>

<br/>

#### [`member Code.Se`][api-reference-index.ts~Code.Se]&nbsp;&nbsp;&nbsp;[&uarr;][api-reference]

[api-reference-index.ts~Code.Se]: #member-codese&nbsp;&nbsp;&nbsp;&uarr; "View member Code.Se"

Szeligi

**Type**:&nbsp;&nbsp;<code>`"Se"`</code>

**Since**: `0.1.0`

**Definition**:&nbsp;&nbsp;[index.ts:112][api-reference-index.ts]

<br/>

<br/>

#### [`member Code.Sl`][api-reference-index.ts~Code.Sl]&nbsp;&nbsp;&nbsp;[&uarr;][api-reference]

[api-reference-index.ts~Code.Sl]: #member-codesl&nbsp;&nbsp;&nbsp;&uarr; "View member Code.Sl"

Sławków

**Type**:&nbsp;&nbsp;<code>`"Sl"`</code>

**Since**: `0.1.0`

**Definition**:&nbsp;&nbsp;[index.ts:114][api-reference-index.ts]

<br/>

<br/>

#### [`member Code.Spl1`][api-reference-index.ts~Code.Spl1]&nbsp;&nbsp;&nbsp;[&uarr;][api-reference]

[api-reference-index.ts~Code.Spl1]: #member-codespl1&nbsp;&nbsp;&nbsp;&uarr; "View member Code.Spl1"

Sosnowiec Południowy

**Type**:&nbsp;&nbsp;<code>`"Spl1"`</code>

**Since**: `0.1.0`

**Definition**:&nbsp;&nbsp;[index.ts:116][api-reference-index.ts]

<br/>

<br/>

#### [`member Code.St`][api-reference-index.ts~Code.St]&nbsp;&nbsp;&nbsp;[&uarr;][api-reference]

[api-reference-index.ts~Code.St]: #member-codest&nbsp;&nbsp;&nbsp;&uarr; "View member Code.St"

Strzałki

**Type**:&nbsp;&nbsp;<code>`"St"`</code>

**Since**: `0.1.0`

**Definition**:&nbsp;&nbsp;[index.ts:118][api-reference-index.ts]

<br/>

<br/>

#### [`member Code.Tl`][api-reference-index.ts~Code.Tl]&nbsp;&nbsp;&nbsp;[&uarr;][api-reference]

[api-reference-index.ts~Code.Tl]: #member-codetl&nbsp;&nbsp;&nbsp;&uarr; "View member Code.Tl"

Tunel

**Type**:&nbsp;&nbsp;<code>`"Tl"`</code>

**Since**: `0.1.0`

**Definition**:&nbsp;&nbsp;[index.ts:120][api-reference-index.ts]

<br/>

<br/>

#### [`member Code.WP`][api-reference-index.ts~Code.WP]&nbsp;&nbsp;&nbsp;[&uarr;][api-reference]

[api-reference-index.ts~Code.WP]: #member-codewp&nbsp;&nbsp;&nbsp;&uarr; "View member Code.WP"

Włoszczowa Północ

**Type**:&nbsp;&nbsp;<code>`"WP"`</code>

**Since**: `0.1.0`

**Definition**:&nbsp;&nbsp;[index.ts:122][api-reference-index.ts]

<br/>

<br/>

#### [`member Code.Zw`][api-reference-index.ts~Code.Zw]&nbsp;&nbsp;&nbsp;[&uarr;][api-reference]

[api-reference-index.ts~Code.Zw]: #member-codezw&nbsp;&nbsp;&nbsp;&uarr; "View member Code.Zw"

Zawiercie

**Type**:&nbsp;&nbsp;<code>`"Zw"`</code>

**Since**: `0.1.0`

**Definition**:&nbsp;&nbsp;[index.ts:124][api-reference-index.ts]

<br/>

<br/>

<br/>

### [`enum Number`][api-reference-index.ts~Number]&nbsp;&nbsp;&nbsp;[&uarr;][api-reference]

[api-reference-index.ts~Number]: #enum-number&nbsp;&nbsp;&nbsp;&uarr; "View enum Number"

Specifies a line number.

**Since**: `0.1.0`

**Definition**:&nbsp;&nbsp;[index.ts:131][api-reference-index.ts]

<br/>
<br/>

#### [`member Number.L1`][api-reference-index.ts~Number.L1]&nbsp;&nbsp;&nbsp;[&uarr;][api-reference]

[api-reference-index.ts~Number.L1]: #member-numberl1&nbsp;&nbsp;&nbsp;&uarr; "View member Number.L1"

**Type**:&nbsp;&nbsp;<code>`1`</code>

**Since**: `0.1.0`

**Definition**:&nbsp;&nbsp;[index.ts:132][api-reference-index.ts]

<br/>

<br/>

#### [`member Number.L12`][api-reference-index.ts~Number.L12]&nbsp;&nbsp;&nbsp;[&uarr;][api-reference]

[api-reference-index.ts~Number.L12]: #member-numberl12&nbsp;&nbsp;&nbsp;&uarr; "View member Number.L12"

**Type**:&nbsp;&nbsp;<code>`12`</code>

**Since**: `0.1.0`

**Definition**:&nbsp;&nbsp;[index.ts:139][api-reference-index.ts]

<br/>

<br/>

#### [`member Number.L130`][api-reference-index.ts~Number.L130]&nbsp;&nbsp;&nbsp;[&uarr;][api-reference]

[api-reference-index.ts~Number.L130]: #member-numberl130&nbsp;&nbsp;&nbsp;&uarr; "View member Number.L130"

**Type**:&nbsp;&nbsp;<code>`130`</code>

**Since**: `0.1.0`

**Definition**:&nbsp;&nbsp;[index.ts:154][api-reference-index.ts]

<br/>

<br/>

#### [`member Number.L131`][api-reference-index.ts~Number.L131]&nbsp;&nbsp;&nbsp;[&uarr;][api-reference]

[api-reference-index.ts~Number.L131]: #member-numberl131&nbsp;&nbsp;&nbsp;&uarr; "View member Number.L131"

**Type**:&nbsp;&nbsp;<code>`131`</code>

**Since**: `0.1.0`

**Definition**:&nbsp;&nbsp;[index.ts:155][api-reference-index.ts]

<br/>

<br/>

#### [`member Number.L132`][api-reference-index.ts~Number.L132]&nbsp;&nbsp;&nbsp;[&uarr;][api-reference]

[api-reference-index.ts~Number.L132]: #member-numberl132&nbsp;&nbsp;&nbsp;&uarr; "View member Number.L132"

**Type**:&nbsp;&nbsp;<code>`132`</code>

**Since**: `0.1.0`

**Definition**:&nbsp;&nbsp;[index.ts:156][api-reference-index.ts]

<br/>

<br/>

#### [`member Number.L133`][api-reference-index.ts~Number.L133]&nbsp;&nbsp;&nbsp;[&uarr;][api-reference]

[api-reference-index.ts~Number.L133]: #member-numberl133&nbsp;&nbsp;&nbsp;&uarr; "View member Number.L133"

**Type**:&nbsp;&nbsp;<code>`133`</code>

**Since**: `0.1.0`

**Definition**:&nbsp;&nbsp;[index.ts:157][api-reference-index.ts]

<br/>

<br/>

#### [`member Number.L134`][api-reference-index.ts~Number.L134]&nbsp;&nbsp;&nbsp;[&uarr;][api-reference]

[api-reference-index.ts~Number.L134]: #member-numberl134&nbsp;&nbsp;&nbsp;&uarr; "View member Number.L134"

**Type**:&nbsp;&nbsp;<code>`134`</code>

**Since**: `0.1.0`

**Definition**:&nbsp;&nbsp;[index.ts:158][api-reference-index.ts]

<br/>

<br/>

#### [`member Number.L137`][api-reference-index.ts~Number.L137]&nbsp;&nbsp;&nbsp;[&uarr;][api-reference]

[api-reference-index.ts~Number.L137]: #member-numberl137&nbsp;&nbsp;&nbsp;&uarr; "View member Number.L137"

**Type**:&nbsp;&nbsp;<code>`137`</code>

**Since**: `0.1.0`

**Definition**:&nbsp;&nbsp;[index.ts:159][api-reference-index.ts]

<br/>

<br/>

#### [`member Number.L138`][api-reference-index.ts~Number.L138]&nbsp;&nbsp;&nbsp;[&uarr;][api-reference]

[api-reference-index.ts~Number.L138]: #member-numberl138&nbsp;&nbsp;&nbsp;&uarr; "View member Number.L138"

**Type**:&nbsp;&nbsp;<code>`138`</code>

**Since**: `0.1.0`

**Definition**:&nbsp;&nbsp;[index.ts:160][api-reference-index.ts]

<br/>

<br/>

#### [`member Number.L139`][api-reference-index.ts~Number.L139]&nbsp;&nbsp;&nbsp;[&uarr;][api-reference]

[api-reference-index.ts~Number.L139]: #member-numberl139&nbsp;&nbsp;&nbsp;&uarr; "View member Number.L139"

**Type**:&nbsp;&nbsp;<code>`139`</code>

**Since**: `0.1.0`

**Definition**:&nbsp;&nbsp;[index.ts:161][api-reference-index.ts]

<br/>

<br/>

#### [`member Number.L140`][api-reference-index.ts~Number.L140]&nbsp;&nbsp;&nbsp;[&uarr;][api-reference]

[api-reference-index.ts~Number.L140]: #member-numberl140&nbsp;&nbsp;&nbsp;&uarr; "View member Number.L140"

**Type**:&nbsp;&nbsp;<code>`140`</code>

**Since**: `0.1.0`

**Definition**:&nbsp;&nbsp;[index.ts:162][api-reference-index.ts]

<br/>

<br/>

#### [`member Number.L141`][api-reference-index.ts~Number.L141]&nbsp;&nbsp;&nbsp;[&uarr;][api-reference]

[api-reference-index.ts~Number.L141]: #member-numberl141&nbsp;&nbsp;&nbsp;&uarr; "View member Number.L141"

**Type**:&nbsp;&nbsp;<code>`141`</code>

**Since**: `0.1.0`

**Definition**:&nbsp;&nbsp;[index.ts:163][api-reference-index.ts]

<br/>

<br/>

#### [`member Number.L142`][api-reference-index.ts~Number.L142]&nbsp;&nbsp;&nbsp;[&uarr;][api-reference]

[api-reference-index.ts~Number.L142]: #member-numberl142&nbsp;&nbsp;&nbsp;&uarr; "View member Number.L142"

**Type**:&nbsp;&nbsp;<code>`142`</code>

**Since**: `0.1.0`

**Definition**:&nbsp;&nbsp;[index.ts:164][api-reference-index.ts]

<br/>

<br/>

#### [`member Number.L143`][api-reference-index.ts~Number.L143]&nbsp;&nbsp;&nbsp;[&uarr;][api-reference]

[api-reference-index.ts~Number.L143]: #member-numberl143&nbsp;&nbsp;&nbsp;&uarr; "View member Number.L143"

**Type**:&nbsp;&nbsp;<code>`143`</code>

**Since**: `0.1.0`

**Definition**:&nbsp;&nbsp;[index.ts:165][api-reference-index.ts]

<br/>

<br/>

#### [`member Number.L144`][api-reference-index.ts~Number.L144]&nbsp;&nbsp;&nbsp;[&uarr;][api-reference]

[api-reference-index.ts~Number.L144]: #member-numberl144&nbsp;&nbsp;&nbsp;&uarr; "View member Number.L144"

**Type**:&nbsp;&nbsp;<code>`144`</code>

**Since**: `0.1.0`

**Definition**:&nbsp;&nbsp;[index.ts:166][api-reference-index.ts]

<br/>

<br/>

#### [`member Number.L149`][api-reference-index.ts~Number.L149]&nbsp;&nbsp;&nbsp;[&uarr;][api-reference]

[api-reference-index.ts~Number.L149]: #member-numberl149&nbsp;&nbsp;&nbsp;&uarr; "View member Number.L149"

**Type**:&nbsp;&nbsp;<code>`149`</code>

**Since**: `0.1.0`

**Definition**:&nbsp;&nbsp;[index.ts:167][api-reference-index.ts]

<br/>

<br/>

#### [`member Number.L15`][api-reference-index.ts~Number.L15]&nbsp;&nbsp;&nbsp;[&uarr;][api-reference]

[api-reference-index.ts~Number.L15]: #member-numberl15&nbsp;&nbsp;&nbsp;&uarr; "View member Number.L15"

**Type**:&nbsp;&nbsp;<code>`15`</code>

**Since**: `0.1.0`

**Definition**:&nbsp;&nbsp;[index.ts:140][api-reference-index.ts]

<br/>

<br/>

#### [`member Number.L151`][api-reference-index.ts~Number.L151]&nbsp;&nbsp;&nbsp;[&uarr;][api-reference]

[api-reference-index.ts~Number.L151]: #member-numberl151&nbsp;&nbsp;&nbsp;&uarr; "View member Number.L151"

**Type**:&nbsp;&nbsp;<code>`151`</code>

**Since**: `0.1.0`

**Definition**:&nbsp;&nbsp;[index.ts:168][api-reference-index.ts]

<br/>

<br/>

#### [`member Number.L154`][api-reference-index.ts~Number.L154]&nbsp;&nbsp;&nbsp;[&uarr;][api-reference]

[api-reference-index.ts~Number.L154]: #member-numberl154&nbsp;&nbsp;&nbsp;&uarr; "View member Number.L154"

**Type**:&nbsp;&nbsp;<code>`154`</code>

**Since**: `0.1.0`

**Definition**:&nbsp;&nbsp;[index.ts:169][api-reference-index.ts]

<br/>

<br/>

#### [`member Number.L155`][api-reference-index.ts~Number.L155]&nbsp;&nbsp;&nbsp;[&uarr;][api-reference]

[api-reference-index.ts~Number.L155]: #member-numberl155&nbsp;&nbsp;&nbsp;&uarr; "View member Number.L155"

**Type**:&nbsp;&nbsp;<code>`155`</code>

**Since**: `0.1.0`

**Definition**:&nbsp;&nbsp;[index.ts:170][api-reference-index.ts]

<br/>

<br/>

#### [`member Number.L158`][api-reference-index.ts~Number.L158]&nbsp;&nbsp;&nbsp;[&uarr;][api-reference]

[api-reference-index.ts~Number.L158]: #member-numberl158&nbsp;&nbsp;&nbsp;&uarr; "View member Number.L158"

**Type**:&nbsp;&nbsp;<code>`158`</code>

**Since**: `0.1.0`

**Definition**:&nbsp;&nbsp;[index.ts:171][api-reference-index.ts]

<br/>

<br/>

#### [`member Number.L16`][api-reference-index.ts~Number.L16]&nbsp;&nbsp;&nbsp;[&uarr;][api-reference]

[api-reference-index.ts~Number.L16]: #member-numberl16&nbsp;&nbsp;&nbsp;&uarr; "View member Number.L16"

**Type**:&nbsp;&nbsp;<code>`16`</code>

**Since**: `0.1.0`

**Definition**:&nbsp;&nbsp;[index.ts:141][api-reference-index.ts]

<br/>

<br/>

#### [`member Number.L160`][api-reference-index.ts~Number.L160]&nbsp;&nbsp;&nbsp;[&uarr;][api-reference]

[api-reference-index.ts~Number.L160]: #member-numberl160&nbsp;&nbsp;&nbsp;&uarr; "View member Number.L160"

**Type**:&nbsp;&nbsp;<code>`160`</code>

**Since**: `0.1.0`

**Definition**:&nbsp;&nbsp;[index.ts:172][api-reference-index.ts]

<br/>

<br/>

#### [`member Number.L162`][api-reference-index.ts~Number.L162]&nbsp;&nbsp;&nbsp;[&uarr;][api-reference]

[api-reference-index.ts~Number.L162]: #member-numberl162&nbsp;&nbsp;&nbsp;&uarr; "View member Number.L162"

**Type**:&nbsp;&nbsp;<code>`162`</code>

**Since**: `0.1.0`

**Definition**:&nbsp;&nbsp;[index.ts:173][api-reference-index.ts]

<br/>

<br/>

#### [`member Number.L163`][api-reference-index.ts~Number.L163]&nbsp;&nbsp;&nbsp;[&uarr;][api-reference]

[api-reference-index.ts~Number.L163]: #member-numberl163&nbsp;&nbsp;&nbsp;&uarr; "View member Number.L163"

**Type**:&nbsp;&nbsp;<code>`163`</code>

**Since**: `0.1.0`

**Definition**:&nbsp;&nbsp;[index.ts:174][api-reference-index.ts]

<br/>

<br/>

#### [`member Number.L164`][api-reference-index.ts~Number.L164]&nbsp;&nbsp;&nbsp;[&uarr;][api-reference]

[api-reference-index.ts~Number.L164]: #member-numberl164&nbsp;&nbsp;&nbsp;&uarr; "View member Number.L164"

**Type**:&nbsp;&nbsp;<code>`164`</code>

**Since**: `0.1.0`

**Definition**:&nbsp;&nbsp;[index.ts:175][api-reference-index.ts]

<br/>

<br/>

#### [`member Number.L17`][api-reference-index.ts~Number.L17]&nbsp;&nbsp;&nbsp;[&uarr;][api-reference]

[api-reference-index.ts~Number.L17]: #member-numberl17&nbsp;&nbsp;&nbsp;&uarr; "View member Number.L17"

**Type**:&nbsp;&nbsp;<code>`17`</code>

**Since**: `0.1.0`

**Definition**:&nbsp;&nbsp;[index.ts:142][api-reference-index.ts]

<br/>

<br/>

#### [`member Number.L171`][api-reference-index.ts~Number.L171]&nbsp;&nbsp;&nbsp;[&uarr;][api-reference]

[api-reference-index.ts~Number.L171]: #member-numberl171&nbsp;&nbsp;&nbsp;&uarr; "View member Number.L171"

**Type**:&nbsp;&nbsp;<code>`171`</code>

**Since**: `0.1.0`

**Definition**:&nbsp;&nbsp;[index.ts:176][api-reference-index.ts]

<br/>

<br/>

#### [`member Number.L179`][api-reference-index.ts~Number.L179]&nbsp;&nbsp;&nbsp;[&uarr;][api-reference]

[api-reference-index.ts~Number.L179]: #member-numberl179&nbsp;&nbsp;&nbsp;&uarr; "View member Number.L179"

**Type**:&nbsp;&nbsp;<code>`179`</code>

**Since**: `0.1.0`

**Definition**:&nbsp;&nbsp;[index.ts:177][api-reference-index.ts]

<br/>

<br/>

#### [`member Number.L18`][api-reference-index.ts~Number.L18]&nbsp;&nbsp;&nbsp;[&uarr;][api-reference]

[api-reference-index.ts~Number.L18]: #member-numberl18&nbsp;&nbsp;&nbsp;&uarr; "View member Number.L18"

**Type**:&nbsp;&nbsp;<code>`18`</code>

**Since**: `0.1.0`

**Definition**:&nbsp;&nbsp;[index.ts:143][api-reference-index.ts]

<br/>

<br/>

#### [`member Number.L186`][api-reference-index.ts~Number.L186]&nbsp;&nbsp;&nbsp;[&uarr;][api-reference]

[api-reference-index.ts~Number.L186]: #member-numberl186&nbsp;&nbsp;&nbsp;&uarr; "View member Number.L186"

**Type**:&nbsp;&nbsp;<code>`186`</code>

**Since**: `0.1.0`

**Definition**:&nbsp;&nbsp;[index.ts:178][api-reference-index.ts]

<br/>

<br/>

#### [`member Number.L19`][api-reference-index.ts~Number.L19]&nbsp;&nbsp;&nbsp;[&uarr;][api-reference]

[api-reference-index.ts~Number.L19]: #member-numberl19&nbsp;&nbsp;&nbsp;&uarr; "View member Number.L19"

**Type**:&nbsp;&nbsp;<code>`19`</code>

**Since**: `0.1.0`

**Definition**:&nbsp;&nbsp;[index.ts:144][api-reference-index.ts]

<br/>

<br/>

#### [`member Number.L2`][api-reference-index.ts~Number.L2]&nbsp;&nbsp;&nbsp;[&uarr;][api-reference]

[api-reference-index.ts~Number.L2]: #member-numberl2&nbsp;&nbsp;&nbsp;&uarr; "View member Number.L2"

**Type**:&nbsp;&nbsp;<code>`2`</code>

**Since**: `0.1.0`

**Definition**:&nbsp;&nbsp;[index.ts:133][api-reference-index.ts]

<br/>

<br/>

#### [`member Number.L20`][api-reference-index.ts~Number.L20]&nbsp;&nbsp;&nbsp;[&uarr;][api-reference]

[api-reference-index.ts~Number.L20]: #member-numberl20&nbsp;&nbsp;&nbsp;&uarr; "View member Number.L20"

**Type**:&nbsp;&nbsp;<code>`20`</code>

**Since**: `0.1.0`

**Definition**:&nbsp;&nbsp;[index.ts:145][api-reference-index.ts]

<br/>

<br/>

#### [`member Number.L22`][api-reference-index.ts~Number.L22]&nbsp;&nbsp;&nbsp;[&uarr;][api-reference]

[api-reference-index.ts~Number.L22]: #member-numberl22&nbsp;&nbsp;&nbsp;&uarr; "View member Number.L22"

**Type**:&nbsp;&nbsp;<code>`22`</code>

**Since**: `0.1.0`

**Definition**:&nbsp;&nbsp;[index.ts:146][api-reference-index.ts]

<br/>

<br/>

#### [`member Number.L25`][api-reference-index.ts~Number.L25]&nbsp;&nbsp;&nbsp;[&uarr;][api-reference]

[api-reference-index.ts~Number.L25]: #member-numberl25&nbsp;&nbsp;&nbsp;&uarr; "View member Number.L25"

**Type**:&nbsp;&nbsp;<code>`25`</code>

**Since**: `0.1.0`

**Definition**:&nbsp;&nbsp;[index.ts:147][api-reference-index.ts]

<br/>

<br/>

#### [`member Number.L272`][api-reference-index.ts~Number.L272]&nbsp;&nbsp;&nbsp;[&uarr;][api-reference]

[api-reference-index.ts~Number.L272]: #member-numberl272&nbsp;&nbsp;&nbsp;&uarr; "View member Number.L272"

**Type**:&nbsp;&nbsp;<code>`272`</code>

**Since**: `0.1.0`

**Definition**:&nbsp;&nbsp;[index.ts:179][api-reference-index.ts]

<br/>

<br/>

#### [`member Number.L276`][api-reference-index.ts~Number.L276]&nbsp;&nbsp;&nbsp;[&uarr;][api-reference]

[api-reference-index.ts~Number.L276]: #member-numberl276&nbsp;&nbsp;&nbsp;&uarr; "View member Number.L276"

**Type**:&nbsp;&nbsp;<code>`276`</code>

**Since**: `0.1.0`

**Definition**:&nbsp;&nbsp;[index.ts:180][api-reference-index.ts]

<br/>

<br/>

#### [`member Number.L280`][api-reference-index.ts~Number.L280]&nbsp;&nbsp;&nbsp;[&uarr;][api-reference]

[api-reference-index.ts~Number.L280]: #member-numberl280&nbsp;&nbsp;&nbsp;&uarr; "View member Number.L280"

**Type**:&nbsp;&nbsp;<code>`280`</code>

**Since**: `0.1.0`

**Definition**:&nbsp;&nbsp;[index.ts:181][api-reference-index.ts]

<br/>

<br/>

#### [`member Number.L3`][api-reference-index.ts~Number.L3]&nbsp;&nbsp;&nbsp;[&uarr;][api-reference]

[api-reference-index.ts~Number.L3]: #member-numberl3&nbsp;&nbsp;&nbsp;&uarr; "View member Number.L3"

**Type**:&nbsp;&nbsp;<code>`3`</code>

**Since**: `0.1.0`

**Definition**:&nbsp;&nbsp;[index.ts:134][api-reference-index.ts]

<br/>

<br/>

#### [`member Number.L301`][api-reference-index.ts~Number.L301]&nbsp;&nbsp;&nbsp;[&uarr;][api-reference]

[api-reference-index.ts~Number.L301]: #member-numberl301&nbsp;&nbsp;&nbsp;&uarr; "View member Number.L301"

**Type**:&nbsp;&nbsp;<code>`301`</code>

**Since**: `0.1.0`

**Definition**:&nbsp;&nbsp;[index.ts:182][api-reference-index.ts]

<br/>

<br/>

#### [`member Number.L4`][api-reference-index.ts~Number.L4]&nbsp;&nbsp;&nbsp;[&uarr;][api-reference]

[api-reference-index.ts~Number.L4]: #member-numberl4&nbsp;&nbsp;&nbsp;&uarr; "View member Number.L4"

**Type**:&nbsp;&nbsp;<code>`4`</code>

**Since**: `0.1.0`

**Definition**:&nbsp;&nbsp;[index.ts:135][api-reference-index.ts]

<br/>

<br/>

#### [`member Number.L447`][api-reference-index.ts~Number.L447]&nbsp;&nbsp;&nbsp;[&uarr;][api-reference]

[api-reference-index.ts~Number.L447]: #member-numberl447&nbsp;&nbsp;&nbsp;&uarr; "View member Number.L447"

**Type**:&nbsp;&nbsp;<code>`447`</code>

**Since**: `0.1.0`

**Definition**:&nbsp;&nbsp;[index.ts:183][api-reference-index.ts]

<br/>

<br/>

#### [`member Number.L45`][api-reference-index.ts~Number.L45]&nbsp;&nbsp;&nbsp;[&uarr;][api-reference]

[api-reference-index.ts~Number.L45]: #member-numberl45&nbsp;&nbsp;&nbsp;&uarr; "View member Number.L45"

**Type**:&nbsp;&nbsp;<code>`45`</code>

**Since**: `0.1.0`

**Definition**:&nbsp;&nbsp;[index.ts:148][api-reference-index.ts]

<br/>

<br/>

#### [`member Number.L479`][api-reference-index.ts~Number.L479]&nbsp;&nbsp;&nbsp;[&uarr;][api-reference]

[api-reference-index.ts~Number.L479]: #member-numberl479&nbsp;&nbsp;&nbsp;&uarr; "View member Number.L479"

**Type**:&nbsp;&nbsp;<code>`479`</code>

**Since**: `0.1.0`

**Definition**:&nbsp;&nbsp;[index.ts:184][api-reference-index.ts]

<br/>

<br/>

#### [`member Number.L501`][api-reference-index.ts~Number.L501]&nbsp;&nbsp;&nbsp;[&uarr;][api-reference]

[api-reference-index.ts~Number.L501]: #member-numberl501&nbsp;&nbsp;&nbsp;&uarr; "View member Number.L501"

**Type**:&nbsp;&nbsp;<code>`501`</code>

**Since**: `0.1.0`

**Definition**:&nbsp;&nbsp;[index.ts:185][api-reference-index.ts]

<br/>

<br/>

#### [`member Number.L509`][api-reference-index.ts~Number.L509]&nbsp;&nbsp;&nbsp;[&uarr;][api-reference]

[api-reference-index.ts~Number.L509]: #member-numberl509&nbsp;&nbsp;&nbsp;&uarr; "View member Number.L509"

**Type**:&nbsp;&nbsp;<code>`509`</code>

**Since**: `0.1.0`

**Definition**:&nbsp;&nbsp;[index.ts:186][api-reference-index.ts]

<br/>

<br/>

#### [`member Number.L529`][api-reference-index.ts~Number.L529]&nbsp;&nbsp;&nbsp;[&uarr;][api-reference]

[api-reference-index.ts~Number.L529]: #member-numberl529&nbsp;&nbsp;&nbsp;&uarr; "View member Number.L529"

**Type**:&nbsp;&nbsp;<code>`529`</code>

**Since**: `0.1.0`

**Definition**:&nbsp;&nbsp;[index.ts:187][api-reference-index.ts]

<br/>

<br/>

#### [`member Number.L540`][api-reference-index.ts~Number.L540]&nbsp;&nbsp;&nbsp;[&uarr;][api-reference]

[api-reference-index.ts~Number.L540]: #member-numberl540&nbsp;&nbsp;&nbsp;&uarr; "View member Number.L540"

**Type**:&nbsp;&nbsp;<code>`540`</code>

**Since**: `0.1.0`

**Definition**:&nbsp;&nbsp;[index.ts:188][api-reference-index.ts]

<br/>

<br/>

#### [`member Number.L546`][api-reference-index.ts~Number.L546]&nbsp;&nbsp;&nbsp;[&uarr;][api-reference]

[api-reference-index.ts~Number.L546]: #member-numberl546&nbsp;&nbsp;&nbsp;&uarr; "View member Number.L546"

**Type**:&nbsp;&nbsp;<code>`546`</code>

**Since**: `0.1.0`

**Definition**:&nbsp;&nbsp;[index.ts:189][api-reference-index.ts]

<br/>

<br/>

#### [`member Number.L570`][api-reference-index.ts~Number.L570]&nbsp;&nbsp;&nbsp;[&uarr;][api-reference]

[api-reference-index.ts~Number.L570]: #member-numberl570&nbsp;&nbsp;&nbsp;&uarr; "View member Number.L570"

**Type**:&nbsp;&nbsp;<code>`570`</code>

**Since**: `0.1.0`

**Definition**:&nbsp;&nbsp;[index.ts:190][api-reference-index.ts]

<br/>

<br/>

#### [`member Number.L571`][api-reference-index.ts~Number.L571]&nbsp;&nbsp;&nbsp;[&uarr;][api-reference]

[api-reference-index.ts~Number.L571]: #member-numberl571&nbsp;&nbsp;&nbsp;&uarr; "View member Number.L571"

**Type**:&nbsp;&nbsp;<code>`571`</code>

**Since**: `0.1.0`

**Definition**:&nbsp;&nbsp;[index.ts:191][api-reference-index.ts]

<br/>

<br/>

#### [`member Number.L572`][api-reference-index.ts~Number.L572]&nbsp;&nbsp;&nbsp;[&uarr;][api-reference]

[api-reference-index.ts~Number.L572]: #member-numberl572&nbsp;&nbsp;&nbsp;&uarr; "View member Number.L572"

**Type**:&nbsp;&nbsp;<code>`572`</code>

**Since**: `0.1.0`

**Definition**:&nbsp;&nbsp;[index.ts:192][api-reference-index.ts]

<br/>

<br/>

#### [`member Number.L573`][api-reference-index.ts~Number.L573]&nbsp;&nbsp;&nbsp;[&uarr;][api-reference]

[api-reference-index.ts~Number.L573]: #member-numberl573&nbsp;&nbsp;&nbsp;&uarr; "View member Number.L573"

**Type**:&nbsp;&nbsp;<code>`573`</code>

**Since**: `0.1.0`

**Definition**:&nbsp;&nbsp;[index.ts:193][api-reference-index.ts]

<br/>

<br/>

#### [`member Number.L574`][api-reference-index.ts~Number.L574]&nbsp;&nbsp;&nbsp;[&uarr;][api-reference]

[api-reference-index.ts~Number.L574]: #member-numberl574&nbsp;&nbsp;&nbsp;&uarr; "View member Number.L574"

**Type**:&nbsp;&nbsp;<code>`574`</code>

**Since**: `0.1.0`

**Definition**:&nbsp;&nbsp;[index.ts:194][api-reference-index.ts]

<br/>

<br/>

#### [`member Number.L6`][api-reference-index.ts~Number.L6]&nbsp;&nbsp;&nbsp;[&uarr;][api-reference]

[api-reference-index.ts~Number.L6]: #member-numberl6&nbsp;&nbsp;&nbsp;&uarr; "View member Number.L6"

**Type**:&nbsp;&nbsp;<code>`6`</code>

**Since**: `0.1.0`

**Definition**:&nbsp;&nbsp;[index.ts:136][api-reference-index.ts]

<br/>

<br/>

#### [`member Number.L607`][api-reference-index.ts~Number.L607]&nbsp;&nbsp;&nbsp;[&uarr;][api-reference]

[api-reference-index.ts~Number.L607]: #member-numberl607&nbsp;&nbsp;&nbsp;&uarr; "View member Number.L607"

**Type**:&nbsp;&nbsp;<code>`607`</code>

**Since**: `0.1.0`

**Definition**:&nbsp;&nbsp;[index.ts:195][api-reference-index.ts]

<br/>

<br/>

#### [`member Number.L61`][api-reference-index.ts~Number.L61]&nbsp;&nbsp;&nbsp;[&uarr;][api-reference]

[api-reference-index.ts~Number.L61]: #member-numberl61&nbsp;&nbsp;&nbsp;&uarr; "View member Number.L61"

**Type**:&nbsp;&nbsp;<code>`61`</code>

**Since**: `0.1.0`

**Definition**:&nbsp;&nbsp;[index.ts:149][api-reference-index.ts]

<br/>

<br/>

#### [`member Number.L62`][api-reference-index.ts~Number.L62]&nbsp;&nbsp;&nbsp;[&uarr;][api-reference]

[api-reference-index.ts~Number.L62]: #member-numberl62&nbsp;&nbsp;&nbsp;&uarr; "View member Number.L62"

**Type**:&nbsp;&nbsp;<code>`62`</code>

**Since**: `0.1.0`

**Definition**:&nbsp;&nbsp;[index.ts:150][api-reference-index.ts]

<br/>

<br/>

#### [`member Number.L64`][api-reference-index.ts~Number.L64]&nbsp;&nbsp;&nbsp;[&uarr;][api-reference]

[api-reference-index.ts~Number.L64]: #member-numberl64&nbsp;&nbsp;&nbsp;&uarr; "View member Number.L64"

**Type**:&nbsp;&nbsp;<code>`64`</code>

**Since**: `0.1.0`

**Definition**:&nbsp;&nbsp;[index.ts:151][api-reference-index.ts]

<br/>

<br/>

#### [`member Number.L651`][api-reference-index.ts~Number.L651]&nbsp;&nbsp;&nbsp;[&uarr;][api-reference]

[api-reference-index.ts~Number.L651]: #member-numberl651&nbsp;&nbsp;&nbsp;&uarr; "View member Number.L651"

**Type**:&nbsp;&nbsp;<code>`651`</code>

**Since**: `0.1.0`

**Definition**:&nbsp;&nbsp;[index.ts:196][api-reference-index.ts]

<br/>

<br/>

#### [`member Number.L652`][api-reference-index.ts~Number.L652]&nbsp;&nbsp;&nbsp;[&uarr;][api-reference]

[api-reference-index.ts~Number.L652]: #member-numberl652&nbsp;&nbsp;&nbsp;&uarr; "View member Number.L652"

**Type**:&nbsp;&nbsp;<code>`652`</code>

**Since**: `0.1.0`

**Definition**:&nbsp;&nbsp;[index.ts:197][api-reference-index.ts]

<br/>

<br/>

#### [`member Number.L657`][api-reference-index.ts~Number.L657]&nbsp;&nbsp;&nbsp;[&uarr;][api-reference]

[api-reference-index.ts~Number.L657]: #member-numberl657&nbsp;&nbsp;&nbsp;&uarr; "View member Number.L657"

**Type**:&nbsp;&nbsp;<code>`657`</code>

**Since**: `0.1.0`

**Definition**:&nbsp;&nbsp;[index.ts:198][api-reference-index.ts]

<br/>

<br/>

#### [`member Number.L660`][api-reference-index.ts~Number.L660]&nbsp;&nbsp;&nbsp;[&uarr;][api-reference]

[api-reference-index.ts~Number.L660]: #member-numberl660&nbsp;&nbsp;&nbsp;&uarr; "View member Number.L660"

**Type**:&nbsp;&nbsp;<code>`660`</code>

**Since**: `0.1.0`

**Definition**:&nbsp;&nbsp;[index.ts:199][api-reference-index.ts]

<br/>

<br/>

#### [`member Number.L661`][api-reference-index.ts~Number.L661]&nbsp;&nbsp;&nbsp;[&uarr;][api-reference]

[api-reference-index.ts~Number.L661]: #member-numberl661&nbsp;&nbsp;&nbsp;&uarr; "View member Number.L661"

**Type**:&nbsp;&nbsp;<code>`661`</code>

**Since**: `0.1.0`

**Definition**:&nbsp;&nbsp;[index.ts:200][api-reference-index.ts]

<br/>

<br/>

#### [`member Number.L663`][api-reference-index.ts~Number.L663]&nbsp;&nbsp;&nbsp;[&uarr;][api-reference]

[api-reference-index.ts~Number.L663]: #member-numberl663&nbsp;&nbsp;&nbsp;&uarr; "View member Number.L663"

**Type**:&nbsp;&nbsp;<code>`663`</code>

**Since**: `0.1.0`

**Definition**:&nbsp;&nbsp;[index.ts:201][api-reference-index.ts]

<br/>

<br/>

#### [`member Number.L668`][api-reference-index.ts~Number.L668]&nbsp;&nbsp;&nbsp;[&uarr;][api-reference]

[api-reference-index.ts~Number.L668]: #member-numberl668&nbsp;&nbsp;&nbsp;&uarr; "View member Number.L668"

**Type**:&nbsp;&nbsp;<code>`668`</code>

**Since**: `0.1.0`

**Definition**:&nbsp;&nbsp;[index.ts:202][api-reference-index.ts]

<br/>

<br/>

#### [`member Number.L687`][api-reference-index.ts~Number.L687]&nbsp;&nbsp;&nbsp;[&uarr;][api-reference]

[api-reference-index.ts~Number.L687]: #member-numberl687&nbsp;&nbsp;&nbsp;&uarr; "View member Number.L687"

**Type**:&nbsp;&nbsp;<code>`687`</code>

**Since**: `0.1.0`

**Definition**:&nbsp;&nbsp;[index.ts:203][api-reference-index.ts]

<br/>

<br/>

#### [`member Number.L696`][api-reference-index.ts~Number.L696]&nbsp;&nbsp;&nbsp;[&uarr;][api-reference]

[api-reference-index.ts~Number.L696]: #member-numberl696&nbsp;&nbsp;&nbsp;&uarr; "View member Number.L696"

**Type**:&nbsp;&nbsp;<code>`696`</code>

**Since**: `0.1.0`

**Definition**:&nbsp;&nbsp;[index.ts:204][api-reference-index.ts]

<br/>

<br/>

#### [`member Number.L703`][api-reference-index.ts~Number.L703]&nbsp;&nbsp;&nbsp;[&uarr;][api-reference]

[api-reference-index.ts~Number.L703]: #member-numberl703&nbsp;&nbsp;&nbsp;&uarr; "View member Number.L703"

**Type**:&nbsp;&nbsp;<code>`703`</code>

**Since**: `0.1.0`

**Definition**:&nbsp;&nbsp;[index.ts:205][api-reference-index.ts]

<br/>

<br/>

#### [`member Number.L713`][api-reference-index.ts~Number.L713]&nbsp;&nbsp;&nbsp;[&uarr;][api-reference]

[api-reference-index.ts~Number.L713]: #member-numberl713&nbsp;&nbsp;&nbsp;&uarr; "View member Number.L713"

**Type**:&nbsp;&nbsp;<code>`713`</code>

**Since**: `0.1.0`

**Definition**:&nbsp;&nbsp;[index.ts:206][api-reference-index.ts]

<br/>

<br/>

#### [`member Number.L717`][api-reference-index.ts~Number.L717]&nbsp;&nbsp;&nbsp;[&uarr;][api-reference]

[api-reference-index.ts~Number.L717]: #member-numberl717&nbsp;&nbsp;&nbsp;&uarr; "View member Number.L717"

**Type**:&nbsp;&nbsp;<code>`717`</code>

**Since**: `0.1.0`

**Definition**:&nbsp;&nbsp;[index.ts:207][api-reference-index.ts]

<br/>

<br/>

#### [`member Number.L73`][api-reference-index.ts~Number.L73]&nbsp;&nbsp;&nbsp;[&uarr;][api-reference]

[api-reference-index.ts~Number.L73]: #member-numberl73&nbsp;&nbsp;&nbsp;&uarr; "View member Number.L73"

**Type**:&nbsp;&nbsp;<code>`73`</code>

**Since**: `0.1.0`

**Definition**:&nbsp;&nbsp;[index.ts:152][api-reference-index.ts]

<br/>

<br/>

#### [`member Number.L8`][api-reference-index.ts~Number.L8]&nbsp;&nbsp;&nbsp;[&uarr;][api-reference]

[api-reference-index.ts~Number.L8]: #member-numberl8&nbsp;&nbsp;&nbsp;&uarr; "View member Number.L8"

**Type**:&nbsp;&nbsp;<code>`8`</code>

**Since**: `0.1.0`

**Definition**:&nbsp;&nbsp;[index.ts:137][api-reference-index.ts]

<br/>

<br/>

#### [`member Number.L836`][api-reference-index.ts~Number.L836]&nbsp;&nbsp;&nbsp;[&uarr;][api-reference]

[api-reference-index.ts~Number.L836]: #member-numberl836&nbsp;&nbsp;&nbsp;&uarr; "View member Number.L836"

**Type**:&nbsp;&nbsp;<code>`836`</code>

**Since**: `0.1.0`

**Definition**:&nbsp;&nbsp;[index.ts:208][api-reference-index.ts]

<br/>

<br/>

#### [`member Number.L839`][api-reference-index.ts~Number.L839]&nbsp;&nbsp;&nbsp;[&uarr;][api-reference]

[api-reference-index.ts~Number.L839]: #member-numberl839&nbsp;&nbsp;&nbsp;&uarr; "View member Number.L839"

**Type**:&nbsp;&nbsp;<code>`839`</code>

**Since**: `0.1.0`

**Definition**:&nbsp;&nbsp;[index.ts:209][api-reference-index.ts]

<br/>

<br/>

#### [`member Number.L898`][api-reference-index.ts~Number.L898]&nbsp;&nbsp;&nbsp;[&uarr;][api-reference]

[api-reference-index.ts~Number.L898]: #member-numberl898&nbsp;&nbsp;&nbsp;&uarr; "View member Number.L898"

**Type**:&nbsp;&nbsp;<code>`898`</code>

**Since**: `0.1.0`

**Definition**:&nbsp;&nbsp;[index.ts:210][api-reference-index.ts]

<br/>

<br/>

#### [`member Number.L9`][api-reference-index.ts~Number.L9]&nbsp;&nbsp;&nbsp;[&uarr;][api-reference]

[api-reference-index.ts~Number.L9]: #member-numberl9&nbsp;&nbsp;&nbsp;&uarr; "View member Number.L9"

**Type**:&nbsp;&nbsp;<code>`9`</code>

**Since**: `0.1.0`

**Definition**:&nbsp;&nbsp;[index.ts:138][api-reference-index.ts]

<br/>

<br/>

#### [`member Number.L95`][api-reference-index.ts~Number.L95]&nbsp;&nbsp;&nbsp;[&uarr;][api-reference]

[api-reference-index.ts~Number.L95]: #member-numberl95&nbsp;&nbsp;&nbsp;&uarr; "View member Number.L95"

**Type**:&nbsp;&nbsp;<code>`95`</code>

**Since**: `0.1.0`

**Definition**:&nbsp;&nbsp;[index.ts:153][api-reference-index.ts]

<br/>

<br/>

<br/>

### [`interface Types`][api-reference-index.ts~Types]&nbsp;&nbsp;&nbsp;[&uarr;][api-reference]

[api-reference-index.ts~Types]: #interface-types&nbsp;&nbsp;&nbsp;&uarr; "View interface Types"

Specifies a type definition for a Setup.

**Since**: `0.1.0`

**Definition**:&nbsp;&nbsp;[index.ts:355][api-reference-index.ts]

<br/>
<br/>

#### [`property Types.lineNumbers`][api-reference-index.ts~Types.lineNumbers]&nbsp;&nbsp;&nbsp;[&uarr;][api-reference]

[api-reference-index.ts~Types.lineNumbers]: #property-typeslinenumbers&nbsp;&nbsp;&nbsp;&uarr; "View property Types.lineNumbers"

**Type**:&nbsp;&nbsp;<code><u>[`Number`][api-reference-index.ts~Number]</u></code>

**Since**: `0.1.0`

**Definition**:&nbsp;&nbsp;[index.ts:356][api-reference-index.ts]

<br/>

<br/>

#### [`property Types.serverCodes`][api-reference-index.ts~Types.serverCodes]&nbsp;&nbsp;&nbsp;[&uarr;][api-reference]

[api-reference-index.ts~Types.serverCodes]: #property-typesservercodes&nbsp;&nbsp;&nbsp;&uarr; "View property Types.serverCodes"

**Type**:&nbsp;&nbsp;<code><u>[`Code`][api-reference-index.ts~Code]</u> &#124; `"cn1"` &#124; `"cz1"` &#124; `"de1"` &#124; `"de3"` &#124; `"de4"` &#124; `"en1"` &#124; `"en2"` &#124; `"en3"` &#124; `"es1"` &#124; `"eu3"` &#124; `"fr1"` &#124; `"pl2"` &#124; `"pl3"` &#124; `"pl4"` &#124; `"pl8"` &#124; `"ua1"`</code>

**Since**: `0.1.0`

**Definition**:&nbsp;&nbsp;[index.ts:357][api-reference-index.ts]

<br/>

<br/>

#### [`property Types.stationCodes`][api-reference-index.ts~Types.stationCodes]&nbsp;&nbsp;&nbsp;[&uarr;][api-reference]

[api-reference-index.ts~Types.stationCodes]: #property-typesstationcodes&nbsp;&nbsp;&nbsp;&uarr; "View property Types.stationCodes"

**Type**:&nbsp;&nbsp;<code><u>[`Code`][api-reference-index.ts~Code]</u> &#124; `"B"` &#124; `"BR"` &#124; `"Bo"` &#124; `"DG"` &#124; `"DGHK"` &#124; `"DW"` &#124; `"DZ"` &#124; `"Dra"` &#124; `"GW"` &#124; `"Gr"` &#124; `"Id"` &#124; `"Ju"` &#124; `"KO"` &#124; `"KZ"` &#124; `"Kn"` &#124; `"Kr"` &#124; `"Kz"` &#124; `"LA"` &#124; `"LB"` &#124; `"LC"` &#124; `"Ol"` &#124; `"Op"` &#124; `"Pi"` &#124; `"Pr"` &#124; `"Ps"` &#124; `"SG"` &#124; `"SKz"` &#124; `"Se"` &#124; `"Sl"` &#124; `"Spl1"` &#124; `"St"` &#124; `"Tl"` &#124; `"WP"` &#124; `"Zw"`</code>

**Since**: `0.1.0`

**Definition**:&nbsp;&nbsp;[index.ts:358][api-reference-index.ts]

<br/>

<br/>

#### [`property Types.trainNumbers`][api-reference-index.ts~Types.trainNumbers]&nbsp;&nbsp;&nbsp;[&uarr;][api-reference]

[api-reference-index.ts~Types.trainNumbers]: #property-typestrainnumbers&nbsp;&nbsp;&nbsp;&uarr; "View property Types.trainNumbers"

**Type**:&nbsp;&nbsp;<code><u>[`Number`][api-reference-index.ts~Number]</u></code>

**Since**: `0.1.0`

**Definition**:&nbsp;&nbsp;[index.ts:359][api-reference-index.ts]

<br/>

<br/>

<br/>

### [`type Number`][api-reference-index.ts~Number]&nbsp;&nbsp;&nbsp;[&uarr;][api-reference]

[api-reference-index.ts~Number]: #type-number&nbsp;&nbsp;&nbsp;&uarr; "View type Number"

Specifies a train number.

**Type**:&nbsp;&nbsp;<code>`"1309"` &#124; `"1311"` &#124; `"1313"` &#124; `"1315"` &#124; `"1317"` &#124; `"1319"` &#124; `"1321"` &#124; `"1323"` &#124; `"1325"` &#124; `"1327"` &#124; `"1329"` &#124; `"1331"` &#124; `"1333"` &#124; `"1335"` &#124; `"1337"` &#124; `"1339"` &#124; `"1341"` &#124; `"1343"` &#124; `"1345"` &#124; `"1409"` &#124; `"1411"` &#124; `"1413"` &#124; `"1415"` &#124; `"1417"` &#124; `"1419"` &#124; `"1421"` &#124; `"1423"` &#124; `"1425"` &#124; `"1427"` &#124; `"1429"` &#124; `"1431"` &#124; `"1433"` &#124; `"1435"` &#124; `"1437"` &#124; `"1439"` &#124; `"1441"` &#124; `"1443"` &#124; `"1445"` &#124; `"1609"` &#124; `"1611"` &#124; `"1613"` &#124; `"1615"` &#124; `"1617"` &#124; `"1619"` &#124; `"1621"` &#124; `"1623"` &#124; `"1625"` &#124; `"1627"` &#124; `"1629"` &#124; `"1631"` &#124; `"1633"` &#124; `"1635"` &#124; `"1637"` &#124; `"1639"` &#124; `"1641"` &#124; `"1643"` &#124; `"1645"` &#124; `"1909"` &#124; `"1911"` &#124; `"1913"` &#124; `"1915"` &#124; `"1917"` &#124; `"1919"` &#124; `"1921"` &#124; `"1923"` &#124; `"1925"` &#124; `"1927"` &#124; `"1929"` &#124; `"1931"` &#124; `"1933"` &#124; `"1935"` &#124; `"1937"` &#124; `"1939"` &#124; `"1941"` &#124; `"1943"` &#124; `"1945"` &#124; `"1947"` &#124; `"3106"` &#124; `"3108"` &#124; `"3110"` &#124; `"3112"` &#124; `"3114"` &#124; `"3116"` &#124; `"3118"` &#124; `"3120"` &#124; `"3122"` &#124; `"3124"` &#124; `"3126"` &#124; `"3128"` &#124; `"3130"` &#124; `"3132"` &#124; `"3134"` &#124; `"3136"` &#124; `"3138"` &#124; `"3140"` &#124; `"3142"` &#124; `"3144"` &#124; `"3146"` &#124; `"4108"` &#124; `"4110"` &#124; `"4112"` &#124; `"4114"` &#124; `"4116"` &#124; `"4118"` &#124; `"4120"` &#124; `"4122"` &#124; `"4124"` &#124; `"4126"` &#124; `"4128"` &#124; `"4130"` &#124; `"4132"` &#124; `"4134"` &#124; `"4136"` &#124; `"4138"` &#124; `"4140"` &#124; `"4142"` &#124; `"4144"` &#124; `"6102"` &#124; `"6104"` &#124; `"6106"` &#124; `"6108"` &#124; `"6110"` &#124; `"6112"` &#124; `"6114"` &#124; `"6116"` &#124; `"6118"` &#124; `"6120"` &#124; `"6122"` &#124; `"6124"` &#124; `"6126"` &#124; `"6128"` &#124; `"6130"` &#124; `"6132"` &#124; `"6134"` &#124; `"6136"` &#124; `"6138"` &#124; `"6140"` &#124; `"6142"` &#124; `"6144"` &#124; `"9106"` &#124; `"9108"` &#124; `"9110"` &#124; `"9112"` &#124; `"9114"` &#124; `"9116"` &#124; `"9118"` &#124; `"9120"` &#124; `"9122"` &#124; `"9124"` &#124; `"9126"` &#124; `"9128"` &#124; `"9130"` &#124; `"9132"` &#124; `"9134"` &#124; `"9136"` &#124; `"9138"` &#124; `"9140"` &#124; `"9142"` &#124; `"9144"` &#124; `"9146"` &#124; `"13109"` &#124; `"13111"` &#124; `"13113"` &#124; `"13115"` &#124; `"13117"` &#124; `"13119"` &#124; `"13121"` &#124; `"13123"` &#124; `"13125"` &#124; `"13127"` &#124; `"13129"` &#124; `"13131"` &#124; `"13133"` &#124; `"13135"` &#124; `"13137"` &#124; `"13139"` &#124; `"13141"` &#124; `"13143"` &#124; `"13145"` &#124; `"13251"` &#124; `"13253"` &#124; `"13255"` &#124; `"13257"` &#124; `"14109"` &#124; `"14111"` &#124; `"14113"` &#124; `"14115"` &#124; `"14117"` &#124; `"14119"` &#124; `"14121"` &#124; `"14123"` &#124; `"14125"` &#124; `"14127"` &#124; `"14129"` &#124; `"14131"` &#124; `"14133"` &#124; `"14135"` &#124; `"14137"` &#124; `"14139"` &#124; `"14141"` &#124; `"14143"` &#124; `"14145"` &#124; `"14147"` &#124; `"16109"` &#124; `"16111"` &#124; `"16113"` &#124; `"16115"` &#124; `"16117"` &#124; `"16119"` &#124; `"16121"` &#124; `"16123"` &#124; `"16125"` &#124; `"16127"` &#124; `"16129"` &#124; `"16131"` &#124; `"16133"` &#124; `"16135"` &#124; `"16137"` &#124; `"16139"` &#124; `"16141"` &#124; `"16143"` &#124; `"16145"` &#124; `"16147"` &#124; `"19301"` &#124; `"19317"` &#124; `"19319"` &#124; `"19321"` &#124; `"19323"` &#124; `"19325"` &#124; `"19327"` &#124; `"19329"` &#124; `"19331"` &#124; `"19333"` &#124; `"19335"` &#124; `"19337"` &#124; `"19339"` &#124; `"19341"` &#124; `"19343"` &#124; `"19345"` &#124; `"19347"` &#124; `"19349"` &#124; `"19351"` &#124; `"19353"` &#124; `"19355"` &#124; `"19357"` &#124; `"19359"` &#124; `"19361"` &#124; `"19363"` &#124; `"19365"` &#124; `"19367"` &#124; `"19369"` &#124; `"19371"` &#124; `"19373"` &#124; `"19375"` &#124; `"19377"` &#124; `"19379"` &#124; `"19381"` &#124; `"19383"` &#124; `"19385"` &#124; `"19387"` &#124; `"19389"` &#124; `"19391"` &#124; `"19393"` &#124; `"19395"` &#124; `"19903"` &#124; `"19917"` &#124; `"19919"` &#124; `"19921"` &#124; `"19923"` &#124; `"19925"` &#124; `"19927"` &#124; `"19929"` &#124; `"19931"` &#124; `"19933"` &#124; `"19935"` &#124; `"19937"` &#124; `"19939"` &#124; `"19941"` &#124; `"19943"` &#124; `"19945"` &#124; `"19947"` &#124; `"19949"` &#124; `"19951"` &#124; `"19953"` &#124; `"19955"` &#124; `"19957"` &#124; `"19959"` &#124; `"19961"` &#124; `"19963"` &#124; `"19965"` &#124; `"19967"` &#124; `"19969"` &#124; `"19971"` &#124; `"19973"` &#124; `"19975"` &#124; `"19977"` &#124; `"19979"` &#124; `"19981"` &#124; `"19983"` &#124; `"19985"` &#124; `"19987"` &#124; `"19989"` &#124; `"19991"` &#124; `"19993"` &#124; `"19995"` &#124; `"19997"` &#124; `"24107"` &#124; `"24109"` &#124; `"24111"` &#124; `"24113"` &#124; `"24115"` &#124; `"24117"` &#124; `"24119"` &#124; `"24121"` &#124; `"24123"` &#124; `"24125"` &#124; `"24127"` &#124; `"24129"` &#124; `"24131"` &#124; `"24133"` &#124; `"24135"` &#124; `"24137"` &#124; `"24139"` &#124; `"24141"` &#124; `"24143"` &#124; `"24145"` &#124; `"24147"` &#124; `"24157"` &#124; `"24159"` &#124; `"24161"` &#124; `"24163"` &#124; `"24165"` &#124; `"24167"` &#124; `"24169"` &#124; `"24171"` &#124; `"24173"` &#124; `"24175"` &#124; `"24177"` &#124; `"24179"` &#124; `"24181"` &#124; `"24183"` &#124; `"24185"` &#124; `"24187"` &#124; `"24189"` &#124; `"24191"` &#124; `"24193"` &#124; `"24927"` &#124; `"24929"` &#124; `"24931"` &#124; `"24933"` &#124; `"24935"` &#124; `"24937"` &#124; `"24939"` &#124; `"24941"` &#124; `"24943"` &#124; `"24945"` &#124; `"24947"` &#124; `"24949"` &#124; `"24951"` &#124; `"24953"` &#124; `"24955"` &#124; `"24957"` &#124; `"24959"` &#124; `"24961"` &#124; `"24963"` &#124; `"24965"` &#124; `"31108"` &#124; `"31110"` &#124; `"31112"` &#124; `"31114"` &#124; `"31116"` &#124; `"31118"` &#124; `"31120"` &#124; `"31122"` &#124; `"31124"` &#124; `"31126"` &#124; `"31128"` &#124; `"31130"` &#124; `"31132"` &#124; `"31134"` &#124; `"31136"` &#124; `"31138"` &#124; `"31140"` &#124; `"31142"` &#124; `"31144"` &#124; `"31250"` &#124; `"31252"` &#124; `"31254"` &#124; `"31256"` &#124; `"37106"` &#124; `"37108"` &#124; `"37110"` &#124; `"37112"` &#124; `"37114"` &#124; `"37116"` &#124; `"37118"` &#124; `"37120"` &#124; `"37122"` &#124; `"37124"` &#124; `"37126"` &#124; `"37128"` &#124; `"37130"` &#124; `"37132"` &#124; `"37134"` &#124; `"37136"` &#124; `"37138"` &#124; `"37140"` &#124; `"37142"` &#124; `"37144"` &#124; `"37146"` &#124; `"40101"` &#124; `"40107"` &#124; `"40109"` &#124; `"40111"` &#124; `"40113"` &#124; `"40115"` &#124; `"40117"` &#124; `"40119"` &#124; `"40121"` &#124; `"40123"` &#124; `"40125"` &#124; `"40127"` &#124; `"40129"` &#124; `"40131"` &#124; `"40133"` &#124; `"40135"` &#124; `"40137"` &#124; `"40139"` &#124; `"40141"` &#124; `"40143"` &#124; `"40145"` &#124; `"40147"` &#124; `"40156"` &#124; `"40158"` &#124; `"40160"` &#124; `"40162"` &#124; `"40164"` &#124; `"40166"` &#124; `"40168"` &#124; `"40170"` &#124; `"40172"` &#124; `"40174"` &#124; `"40176"` &#124; `"40178"` &#124; `"40180"` &#124; `"40182"` &#124; `"40184"` &#124; `"40186"` &#124; `"40188"` &#124; `"40190"` &#124; `"40192"` &#124; `"40194"` &#124; `"40196"` &#124; `"40601"` &#124; `"40609"` &#124; `"40611"` &#124; `"40613"` &#124; `"40615"` &#124; `"40617"` &#124; `"40619"` &#124; `"40621"` &#124; `"40623"` &#124; `"40625"` &#124; `"40627"` &#124; `"40629"` &#124; `"40631"` &#124; `"40633"` &#124; `"40635"` &#124; `"40637"` &#124; `"40639"` &#124; `"40641"` &#124; `"40643"` &#124; `"40645"` &#124; `"40647"` &#124; `"40658"` &#124; `"40660"` &#124; `"40662"` &#124; `"40664"` &#124; `"40666"` &#124; `"40668"` &#124; `"40670"` &#124; `"40672"` &#124; `"40674"` &#124; `"40676"` &#124; `"40678"` &#124; `"40680"` &#124; `"40682"` &#124; `"40684"` &#124; `"40686"` &#124; `"40688"` &#124; `"40690"` &#124; `"40692"` &#124; `"40694"` &#124; `"40696"` &#124; `"41104"` &#124; `"41106"` &#124; `"41108"` &#124; `"41110"` &#124; `"41112"` &#124; `"41114"` &#124; `"41116"` &#124; `"41118"` &#124; `"41120"` &#124; `"41122"` &#124; `"41124"` &#124; `"41126"` &#124; `"41128"` &#124; `"41130"` &#124; `"41132"` &#124; `"41134"` &#124; `"41136"` &#124; `"41138"` &#124; `"41140"` &#124; `"41142"` &#124; `"42108"` &#124; `"42110"` &#124; `"42112"` &#124; `"42114"` &#124; `"42116"` &#124; `"42118"` &#124; `"42120"` &#124; `"42122"` &#124; `"42124"` &#124; `"42126"` &#124; `"42128"` &#124; `"42130"` &#124; `"42132"` &#124; `"42134"` &#124; `"42136"` &#124; `"42138"` &#124; `"42140"` &#124; `"42142"` &#124; `"42144"` &#124; `"42158"` &#124; `"42160"` &#124; `"42162"` &#124; `"42164"` &#124; `"42166"` &#124; `"42168"` &#124; `"42170"` &#124; `"42172"` &#124; `"42174"` &#124; `"42176"` &#124; `"42178"` &#124; `"42180"` &#124; `"42182"` &#124; `"42184"` &#124; `"42186"` &#124; `"42188"` &#124; `"42190"` &#124; `"42192"` &#124; `"42194"` &#124; `"42928"` &#124; `"42930"` &#124; `"42932"` &#124; `"42934"` &#124; `"42936"` &#124; `"42938"` &#124; `"42940"` &#124; `"42942"` &#124; `"42944"` &#124; `"42946"` &#124; `"42948"` &#124; `"42950"` &#124; `"42952"` &#124; `"42954"` &#124; `"42956"` &#124; `"42958"` &#124; `"42960"` &#124; `"42962"` &#124; `"42964"` &#124; `"43328"` &#124; `"43330"` &#124; `"43332"` &#124; `"43334"` &#124; `"43336"` &#124; `"43338"` &#124; `"43340"` &#124; `"43342"` &#124; `"43344"` &#124; `"43346"` &#124; `"43348"` &#124; `"43350"` &#124; `"43352"` &#124; `"43354"` &#124; `"43356"` &#124; `"43358"` &#124; `"43360"` &#124; `"43362"` &#124; `"43364"` &#124; `"43366"` &#124; `"44321"` &#124; `"44329"` &#124; `"44331"` &#124; `"44333"` &#124; `"44335"` &#124; `"44337"` &#124; `"44339"` &#124; `"44341"` &#124; `"44343"` &#124; `"44345"` &#124; `"44347"` &#124; `"44349"` &#124; `"44351"` &#124; `"44353"` &#124; `"44355"` &#124; `"44357"` &#124; `"44359"` &#124; `"44361"` &#124; `"44363"` &#124; `"44365"` &#124; `"44367"` &#124; `"45270"` &#124; `"45272"` &#124; `"45274"` &#124; `"45276"` &#124; `"54273"` &#124; `"54275"` &#124; `"54277"` &#124; `"54279"` &#124; `"61102"` &#124; `"61104"` &#124; `"61106"` &#124; `"61108"` &#124; `"61110"` &#124; `"61112"` &#124; `"61114"` &#124; `"61116"` &#124; `"61118"` &#124; `"61120"` &#124; `"61122"` &#124; `"61124"` &#124; `"61126"` &#124; `"61128"` &#124; `"61130"` &#124; `"61132"` &#124; `"61134"` &#124; `"61136"` &#124; `"61138"` &#124; `"61140"` &#124; `"61142"` &#124; `"61144"` &#124; `"73101"` &#124; `"73103"` &#124; `"73105"` &#124; `"73107"` &#124; `"73109"` &#124; `"73111"` &#124; `"73113"` &#124; `"73115"` &#124; `"73117"` &#124; `"73119"` &#124; `"73121"` &#124; `"73123"` &#124; `"73125"` &#124; `"73127"` &#124; `"73129"` &#124; `"73131"` &#124; `"73133"` &#124; `"73135"` &#124; `"73137"` &#124; `"73139"` &#124; `"73141"` &#124; `"91300"` &#124; `"91316"` &#124; `"91318"` &#124; `"91320"` &#124; `"91322"` &#124; `"91324"` &#124; `"91326"` &#124; `"91328"` &#124; `"91330"` &#124; `"91332"` &#124; `"91334"` &#124; `"91336"` &#124; `"91338"` &#124; `"91340"` &#124; `"91342"` &#124; `"91344"` &#124; `"91346"` &#124; `"91348"` &#124; `"91350"` &#124; `"91352"` &#124; `"91354"` &#124; `"91356"` &#124; `"91358"` &#124; `"91360"` &#124; `"91362"` &#124; `"91364"` &#124; `"91366"` &#124; `"91368"` &#124; `"91370"` &#124; `"91372"` &#124; `"91374"` &#124; `"91376"` &#124; `"91378"` &#124; `"91380"` &#124; `"91382"` &#124; `"91384"` &#124; `"91386"` &#124; `"91388"` &#124; `"91390"` &#124; `"91392"` &#124; `"91394"` &#124; `"91914"` &#124; `"91916"` &#124; `"91918"` &#124; `"91920"` &#124; `"91922"` &#124; `"91924"` &#124; `"91926"` &#124; `"91928"` &#124; `"91930"` &#124; `"91932"` &#124; `"91934"` &#124; `"91936"` &#124; `"91938"` &#124; `"91940"` &#124; `"91942"` &#124; `"91944"` &#124; `"91946"` &#124; `"91948"` &#124; `"91950"` &#124; `"91952"` &#124; `"91954"` &#124; `"91956"` &#124; `"91958"` &#124; `"91960"` &#124; `"91962"` &#124; `"91964"` &#124; `"91966"` &#124; `"91968"` &#124; `"91970"` &#124; `"91972"` &#124; `"91974"` &#124; `"91976"` &#124; `"91978"` &#124; `"91980"` &#124; `"91982"` &#124; `"91984"` &#124; `"91986"` &#124; `"91988"` &#124; `"91990"` &#124; `"91992"` &#124; `"91994"` &#124; `"91996"` &#124; `"132001"` &#124; `"132005"` &#124; `"132009"` &#124; `"132013"` &#124; `"132017"` &#124; `"132021"` &#124; `"132025"` &#124; `"132029"` &#124; `"132033"` &#124; `"132037"` &#124; `"132041"` &#124; `"132045"` &#124; `"142001"` &#124; `"142003"` &#124; `"142005"` &#124; `"142007"` &#124; `"142009"` &#124; `"142011"` &#124; `"142013"` &#124; `"142015"` &#124; `"142017"` &#124; `"142019"` &#124; `"142021"` &#124; `"142023"` &#124; `"142025"` &#124; `"142027"` &#124; `"142029"` &#124; `"142031"` &#124; `"142033"` &#124; `"142035"` &#124; `"142037"` &#124; `"142039"` &#124; `"142041"` &#124; `"142043"` &#124; `"142045"` &#124; `"142047"` &#124; `"144251"` &#124; `"144253"` &#124; `"144255"` &#124; `"144257"` &#124; `"144259"` &#124; `"144261"` &#124; `"144263"` &#124; `"144265"` &#124; `"144267"` &#124; `"144269"` &#124; `"144271"` &#124; `"144273"` &#124; `"144275"` &#124; `"144277"` &#124; `"144279"` &#124; `"144281"` &#124; `"144283"` &#124; `"144285"` &#124; `"144287"` &#124; `"144289"` &#124; `"144291"` &#124; `"144293"` &#124; `"144295"` &#124; `"144297"` &#124; `"146011"` &#124; `"146015"` &#124; `"146019"` &#124; `"146023"` &#124; `"146027"` &#124; `"146031"` &#124; `"146035"` &#124; `"146039"` &#124; `"146043"` &#124; `"146047"` &#124; `"146051"` &#124; `"146055"` &#124; `"243513"` &#124; `"243517"` &#124; `"243521"` &#124; `"243525"` &#124; `"243529"` &#124; `"243533"` &#124; `"243537"` &#124; `"243541"` &#124; `"243545"` &#124; `"243549"` &#124; `"243553"` &#124; `"243557"` &#124; `"244021"` &#124; `"244025"` &#124; `"244029"` &#124; `"244033"` &#124; `"244037"` &#124; `"244041"` &#124; `"244045"` &#124; `"244049"` &#124; `"244053"` &#124; `"244057"` &#124; `"244061"` &#124; `"244065"` &#124; `"412002"` &#124; `"412006"` &#124; `"412010"` &#124; `"412014"` &#124; `"412018"` &#124; `"412022"` &#124; `"412026"` &#124; `"412030"` &#124; `"412034"` &#124; `"412038"` &#124; `"412042"` &#124; `"412046"` &#124; `"413050"` &#124; `"413054"` &#124; `"413058"` &#124; `"413062"` &#124; `"413066"` &#124; `"413070"` &#124; `"413074"` &#124; `"413078"` &#124; `"413082"` &#124; `"413086"` &#124; `"413090"` &#124; `"413094"` &#124; `"414030"` &#124; `"414032"` &#124; `"414034"` &#124; `"414036"` &#124; `"414038"` &#124; `"414040"` &#124; `"414042"` &#124; `"414044"` &#124; `"414046"` &#124; `"414048"` &#124; `"414050"` &#124; `"414052"` &#124; `"414054"` &#124; `"414056"` &#124; `"414058"` &#124; `"414060"` &#124; `"414062"` &#124; `"414064"` &#124; `"414066"` &#124; `"414068"` &#124; `"414070"` &#124; `"414072"` &#124; `"414074"` &#124; `"414076"` &#124; `"424020"` &#124; `"424022"` &#124; `"424024"` &#124; `"424026"` &#124; `"424028"` &#124; `"424030"` &#124; `"424032"` &#124; `"424034"` &#124; `"424036"` &#124; `"424038"` &#124; `"424040"` &#124; `"424042"` &#124; `"424044"` &#124; `"424046"` &#124; `"424048"` &#124; `"424050"` &#124; `"424052"` &#124; `"424054"` &#124; `"424056"` &#124; `"424058"` &#124; `"424060"` &#124; `"424062"` &#124; `"424064"` &#124; `"424066"` &#124; `"441021"` &#124; `"441023"` &#124; `"441025"` &#124; `"441027"` &#124; `"441029"` &#124; `"441031"` &#124; `"441033"` &#124; `"441035"` &#124; `"441037"` &#124; `"441039"` &#124; `"441041"` &#124; `"441043"` &#124; `"441045"` &#124; `"441047"` &#124; `"441049"` &#124; `"441051"` &#124; `"441053"` &#124; `"441055"` &#124; `"441057"` &#124; `"441059"` &#124; `"441061"` &#124; `"441063"` &#124; `"441065"` &#124; `"441067"` &#124; `"442001"` &#124; `"442003"` &#124; `"442005"` &#124; `"442007"` &#124; `"442009"` &#124; `"442011"` &#124; `"442013"` &#124; `"442015"` &#124; `"442017"` &#124; `"442019"` &#124; `"442021"` &#124; `"442023"` &#124; `"442025"` &#124; `"442027"` &#124; `"442029"` &#124; `"442031"` &#124; `"442033"` &#124; `"442035"` &#124; `"442037"` &#124; `"442039"` &#124; `"442041"` &#124; `"442043"` &#124; `"442045"` &#124; `"442047"` &#124; `"443913"` &#124; `"443915"` &#124; `"443917"` &#124; `"443919"` &#124; `"443921"` &#124; `"443923"` &#124; `"443925"` &#124; `"443927"` &#124; `"443929"` &#124; `"443931"` &#124; `"443933"` &#124; `"443935"` &#124; `"443937"` &#124; `"443939"` &#124; `"443941"` &#124; `"443943"` &#124; `"443945"` &#124; `"443947"` &#124; `"443949"` &#124; `"443951"` &#124; `"443953"` &#124; `"443955"` &#124; `"443957"` &#124; `"443959"` &#124; `"445014"` &#124; `"445018"` &#124; `"445022"` &#124; `"445026"` &#124; `"445030"` &#124; `"445034"` &#124; `"445038"` &#124; `"445042"` &#124; `"445046"` &#124; `"445050"` &#124; `"445054"` &#124; `"445058"` &#124; `"446000"` &#124; `"446002"` &#124; `"446004"` &#124; `"446006"` &#124; `"446008"` &#124; `"446010"` &#124; `"446012"` &#124; `"446014"` &#124; `"446016"` &#124; `"446018"` &#124; `"446020"` &#124; `"446022"` &#124; `"446024"` &#124; `"446026"` &#124; `"446028"` &#124; `"446030"` &#124; `"446032"` &#124; `"446034"` &#124; `"446036"` &#124; `"446038"` &#124; `"446040"` &#124; `"446042"` &#124; `"446044"` &#124; `"446046"` &#124; `"464000"` &#124; `"464002"` &#124; `"464004"` &#124; `"464006"` &#124; `"464008"` &#124; `"464010"` &#124; `"464012"` &#124; `"464014"` &#124; `"464016"` &#124; `"464018"` &#124; `"464020"` &#124; `"464022"` &#124; `"464024"` &#124; `"464026"` &#124; `"464028"` &#124; `"464030"` &#124; `"464032"` &#124; `"464034"` &#124; `"464036"` &#124; `"464038"` &#124; `"464040"` &#124; `"464042"` &#124; `"464044"` &#124; `"464046"` &#124; `"629000"` &#124; `"629004"` &#124; `"629008"` &#124; `"629012"` &#124; `"629016"` &#124; `"629020"` &#124; `"629024"` &#124; `"629028"` &#124; `"629032"` &#124; `"629036"` &#124; `"629040"` &#124; `"629044"` &#124; `"649052"` &#124; `"649056"` &#124; `"649060"` &#124; `"649064"` &#124; `"649068"` &#124; `"649072"` &#124; `"649076"` &#124; `"649080"` &#124; `"649084"` &#124; `"649088"` &#124; `"649092"` &#124; `"649096"`</code>

**Since**: `0.1.0`

**Definition**:&nbsp;&nbsp;[index.ts:217][api-reference-index.ts]

<br/>
<br/>

<br/>

## [About this module][about-this-module]

[about-this-module]: #about-this-module "View About this module"

Package name: `@simrail-sdk/core-setup-pl`

Author: [Niek van Bennekom](https://github.com/niekvb "View GitHub profile")

Version: `0.1.1`

Repository: [`github:simrail-sdk/core-setup-pl` (origin)](https://github.com/simrail-sdk/core-setup-pl.git "View on github")

Keywords: `simrail`, `sdk`, `core`, `setup`, `poland`, `pl`.

[View license][view-license]&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;[view open source licenses][view-open-source-licenses]

[view-license]: ./LICENSE.md "View license"
[view-open-source-licenses]: ./OSL.md "View open source licenses"

*SCTL version: `0.1.11-dev`*
<br/>
<br/>


### [Module dependencies][module-dependencies]

[module-dependencies]: #module-dependencies "View Module dependencies"

#### [Module package dependencies][module-package-dependencies]

[module-package-dependencies]: #module-package-dependencies "View Module package dependencies"


**Development packages**: (2)

- `@types/node`: TypeScript definitions for node.

- `typescript`: TypeScript is a language for application scale JavaScript development.
<br/>
<br/>


#### [Internal module dependencies][internal-module-dependencies]

[internal-module-dependencies]: #internal-module-dependencies "View Internal module dependencies"

This module contains and uses the following internal modules:


- `index.js`
<br/>
<br/>


Dependency tree:

[![Dependency tree graph][dependency-tree-image]][dependency-tree-image]

[dependency-tree-image]: ./stats/dependencyTree.png "Dependency tree"
<br/>
<br/>


### [Module code statistics][module-code-statistics]

[module-code-statistics]: #module-code-statistics "View Module code statistics"

| File type | Number of files | Lines with code | Lines with comments | Blank lines |
| --------- | --------------- | --------------- | ------------------- | ----------- |
| Markdown | 3 | 1703 | 0 | 1214 |
| TypeScript | 2 | 294 | 75 | 10 |
| JavaScript | 2 | 162 | 2 | 0 |
| JSON | 3 | 92 | 0 | 1 |
| YAML | 1 | 40 | 0 | 3 |
| **All (total)** | **11** | **2291** | **77** | **1228** |
