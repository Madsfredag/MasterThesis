# Referat og beslutninger fra vejledermødet 21. oktober 2026

Kilde: Mads' referat, modtaget 22. oktober 2026. Notatet samler mødeindholdet og skelner mellem aftaler, anbefalinger og åbne spørgsmål.

## Status på projektet

- Testapplikationen kører i Azure.
- Projektets diagram blev gennemgået.
- Den fremlagte litteratursøgning omfattede IEEE og ACM med 793 poster efter fjernelse af dubletter. Tallet er den rapporterede status ved mødet, ikke et antal endeligt inkluderede studier.

## SLR: godkendt spørgsmål og prioritet

Følgende reviewspørgsmål er godkendt til at blive prøvet af:

> Hvordan bruger LLM-baserede agenter operationel telemetri til at diagnosticere fejl i cloud- og microservicesystemer, og hvilken evidens understøtter diagnosernes korrekthed og pålidelighed?

SLR'en bør især identificere måder at vurdere agenter på. Disse vurderingskriterier skal give et konkret grundlag for at sammenligne og vælge en agentmetode. Agentdesign er fortsat relevant, men udvælgelsen skal understøttes af en tydelig evaluering.

Dette er ikke en godkendelse af en bestemt model, agentarkitektur eller et færdigt SLR-resultat.

## Datakilder og tidsafgrænsning

Den fremlagte søgning anvendte engelsksprogede studier fra 2020–2026.

Vejlederne foreslog Google Scholar og bad om at undersøge, om IEEE og ACM alene giver tilstrækkelig dækning, herunder hvilke udgivere og samlinger søgningerne faktisk omfatter. Databaserne er derfor ikke endeligt godkendt som tilstrækkelige. Bemærkningen om udgiverdækning er et spørgsmål, der skal undersøges, ikke en fastslået egenskab ved databaserne.

Hvis traditionel ML bliver relevant, kan det være nødvendigt at søge længere tilbage end 2020. En sådan ændring er betinget af behovet og er ikke allerede besluttet eller gennemført.

## Antal studier og agenttilgange

Der er ikke aftalt et bestemt antal kernestudier. Antallet skal være tilstrækkeligt til at understøtte analysen og konklusionerne. Det er vigtigt at forklare:

- Hvilke kriterier der bruges til at vurdere studier og løsninger.
- Hvordan kriterierne er valgt.
- Hvordan vurderingerne fører til det endelige valg.

Tilsvarende er der ikke aftalt et bestemt antal agenttilgange. Undersøg så mange, som er nødvendige for et begrundet valg. Den tidligere arbejdsidé om 5–15 kernestudier er ikke et fast inklusionsloft.

## ML og LLM

Christian anbefalede at overveje andre ML-metoder som alternativ til LLM'er, hvor det er relevant, eller som minimum analysere mulighederne i rapporten.

Der er ikke truffet beslutning om at erstatte LLM-tilgangen. Det er fortsat åbent, hvilke opgaver andre ML-metoder kunne løse, hvilke data det ville kræve, og om de skal indgå som implementeret sammenligningsgrundlag eller som en faglig analyse.

## Placering i rapporten

- Den fulde SLR placeres i bilaget, herunder fremgangsmåde og den faktisk gennemførte proces.
- De væsentlige resultater og deres betydning skal fremgå af hovedrapporten.
- State of the Art skal præsentere det forskningsmæssige vidensgrundlag, som projektet bygger videre på.
- State of the Art må gerne fylde 10–12 sider, hvis indholdet begrunder det. Dette er ikke et krav om et bestemt sidetal.

## Aftale til næste møde

Send den fulde SLR til vejlederne til godkendelse.

## Arbejdskonsekvenser

Følgende omsætter feedbacken til næste arbejde. Det er ikke yderligere beslutninger truffet af vejlederne.

1. Brug det godkendte spørgsmål til at afprøve og præcisere reviewets kriterier.
2. Afklar søgekildernes dækning og behovet for supplerende søgninger.
3. Prioritér udtræk af evalueringsmetoder, datasæt, kendte fejlårsager, baselines, målepunkter og begrænsninger.
4. Sammenhold kriterierne med de data og fejlscenarier, PoC'en faktisk kan understøtte.
5. Hold en enkelt agent og en koordinator med specialister som foreløbige kandidater, ikke som en endeligt fastlagt sammenligning eller vinder.
6. Undersøg, hvor traditionel ML er et meningsfuldt alternativ eller supplement.
7. Færdiggør review og syntese, og send den fulde SLR til vejlederne.

Fælles arbejde med telemetriadgang og evidens kan fortsætte, mens sammenligningsgrundlaget afklares.

## Forhold til tidligere materiale

Det tidligere IEEE/OpenAlex-review og det nyere IEEE/ACM-materiale er forskellige søge- og screeningsgrundlag. De må ikke blandes eller beskrives som ét færdigt review. Mødet godkender ikke tidligere screeningsbeslutninger eller en afsluttet udvælgelse.

Mødet ændrer ikke i sig selv projektets godkendte problemformulering eller overordnede forskningsspørgsmål. Nye ændringer skal aftales eksplicit.
