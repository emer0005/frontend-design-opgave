I denne opgave har vi arbejdet med at omsætte et Figma-design til et kodet site i Astro med fokus på vedligeholdelsesvenlig CSS. En af de største udfordringer var at implementere nye CSS-teknikker som container, subgrid og anchor positioning på en måde, der samtidig fungerer på tværs af browsere.

En succes vi oplevede var opbygning af vores komponenter, hvilket gjorde det lettere at genbruge samt holde overblikket over koden. Vi oplevede udfordringer med opbygning af vores slug og brugen af subgrid.
Hvis vi havde haft mere tid vil vi gerne har finpudset og ryddet op i koden.

Vi har anvendt flere teknikker fra undervisningen for eksempel er @container brugt i komponenter for at gøre dem mere fleksible på forskellige sider, og subgrid er anvendt for at sikre konsistent alignment mellem sektioner. Derudover har vi brugt custom properties (fx --space- og --step-) til spacing og typografi, hvilket gør designet mere skalerbart. Relative Color Syntax er brugt til hover, så farver automatisk tilpasses uden at definere nye værdier.

Defensive CSS er tænkt ind, fx ved brug af max-width: 100% på billeder samt fallback-løsninger med @supports not (...), hvis en feature ikke understøttes. Derudover er der taget hensyn til prefers-reduced-motion for at begrænse animationer.

Vi har benyttet progressive enhancement ved FAQ sektionen, som fungerer uden JavaScript, og derefter er forbedret med animation i browsere, der understøtter det.
Ligeledes er Anchor Positioning brugt til login-popover.

CSS’en er organiseret med globale styles (fx reset, tokens og typografi) samt komponent-specifik CSS i de enkelte Astro-komponenter. Dette gør det nemmere at vedligeholde og skalere løsningen, da ændringer kan foretages lokalt uden at påvirke resten af systemet.
