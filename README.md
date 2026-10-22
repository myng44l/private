# Auto Settlers (NeoForge 1.21.1, fuer ATM 10)

## Bauen
1. Offizielles NeoForge-MDK 1.21.1 laden (github.com/NeoForgeMDKs/MDK-1.21.1-NeoGradle), Java 21.
2. gradle.properties: mod_id=autosettlers, mod_name=Auto Settlers, mod_group_id=com.example.autosettlers
3. MDK-`src/` durch das `src/` aus diesem Projekt ersetzen (Beispielklassen loeschen).
4. `./gradlew build` -> build/libs/*.jar in den mods-Ordner von ATM 10.

## Spielen
Siedler-Spawn-Ei (Kreativ-Tab "Spawn Eggs") benutzen. Danach:
- Farmen: reife Pflanzen ernten + neu pflanzen
- Holzfaellen: nur natuerliche Baeume, pflanzt Setzlinge nach (wenn im Inventar)
- Minen: freiliegende Erze (Tag c:ores) bis mineDepth tief
- Maschinen: Eintraege aus `machines` fuettern und leeren
- Lager: Ernte wandert in Kisten/Lager (Block mit >= 9 Slots)
- Bauen: neue Haeuser aus `blueprints`, danach zieht ein neuer Siedler ein

## Config: config/autosettlers-common.toml
- allowedMods: welche Mods benutzt werden duerfen (Mod-IDs)
- machines: Maschinen-Block-IDs, z.B. "mekanism:enrichment_chamber"
- jobs: Arbeiten einzeln an/aus
- building.materialMode: FREE (gratis) oder CONSUME (Material aus Lagern)
