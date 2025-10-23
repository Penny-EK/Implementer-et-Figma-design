# REFLEKSION

Jeg synes opgave har været den perfekte kodemulighed: både på den sjove, frustrerende og udfordrende. Det har været en spændende opgave at arbejde med da der har været så mange forskellige elementer, men dette har også været grunden til at jeg blev nødt til at skære noget af projektet fra.

## Opbygning

Jeg har min _SectionWrapper.astro_ component som er den grundlæggende component da den gør det muligt at følge det definerede layout. Så næsten alt indhold på main bliver opdelt i sektioner ud fra SectionWrapper.

_dette er et kodesnippet fra SectionWrapper.astro_

```astro
---
const { Background, Type, Padding } = Astro.props;
---

<section class={Background} style={`padding: ${Padding};`}>
  <div class="inner" class={Type}>
    <slot />
  </div>
</section>
```

_her kan man se hvordan konstanten ”Padding” bliver brugt til at definere hvor meget padding der skal være på den inviduelle sektion, da det netop variere igennem designet._

Og når den bliver kaldt, bliver den padding som bliver angivet sendt med

```
<SectionWrapper Padding="100px 0">
```

## CSS:

### Global.css

Min global.css indeholder ting som:

- Css variabler
- headers
- Layout grid

### Page

Alle pages har css som kun gælder for den inviduelle side.
f.eks. hvis der er specielle vilkår som kun gælder for en sektion på index

### Components

En største del af css ligger i de forskellige komponenter.
Derudover bruger jeg særligt astro props til at kunne redigere på komponenten ud fra specifikke behov, nogen af de props som særligt har gået igen har værer ting som: padding, baggrundsfarve, klasser og type

## Udfordringer:

Ved opstart af projektet var det meget uoverskueligt hvor man skulle starte og etc.. dette gjorde at jeg fik spildt unødvendigt tid på være tabt i opgaven. Dette endte ud i sidste ende med at jeg blev nødt til at i store træk undlade responsiviteten på sitet. Det jeg har skåret fra, har gjort at jeg kunne gå mere i dybden med min kode og forstå flowet af den mere glidende.

### Nemme løsninger

Igennem projektet er der flere ”nemme løsninger” som gør at sitet måske ligner det rigtige, men i længden ikke er holdbart. Disse løsninger har været med til at nedsætte hvor responsivt sitet er.

_Det er bl.a. løsninger som dette i headeren_

```
.hero-content {
      margin-left: 10vw;
    }
```

koden her giver illustrationen at teksten i hero på index følger [main] kolonnen i mit layout grid. Dog hvis der sker en ændring på [main] vil illustrationen fejle.

## Afrunding

Jeg er delvis tilfreds med hvordan projektet har endt ud. der er selvfølgelig flere ting som jeg har været nød til at ignorere, MEN jeg er tilfreds med min arbejdsindsats ud fra de vilkår der har været.

Fremadrettet skal jeg være mere fokuseret på mine evner og min egen arbejdshastighed. Derudover skal jeg nok også være hurtigere til at registrere hvad der er inde for mine evner
