# Codelijst CSOR — Kwantificeerbaar aspect

Deze repository bevat de SKOS-codelijst **Kwantificeerbaar aspect** binnen het CSOR-datamodel (Chemische Stoffen en Omgevingsparameters-Register) van de Vlaamse overheid.

## Beschrijving

Een kwantificeerbaar aspect duidt aan wat de interpretatie is van de numerieke waarde van een meting binnen een natuurkundige dimensie. Zo kan een parameter voor een stikstofhoudende variabele (bv. NO3) twee aspecten kennen: bv. "gram stikstofhoudende variabele per kilogram droge stof" en "gram stikstof per kilogram droge stof". Hoewel beide eenzelfde natuurkundige dimensie uitdrukken (massa/massa), zijn de geassocieerde waarden onderling onvergelijkbaar. Via het kwantificeerbare aspect geeft men aan hoe de waarde geïnterpreteerd moet worden.

- Concept scheme URI: `https://data.omgeving.vlaanderen.be/id/conceptscheme/csor/kwantificeerbaaraspect`
- Namespace: `https://data.omgeving.vlaanderen.be/ns/csor#`
- Named graph (Virtuoso): `https://data.omgeving.vlaanderen.be/id/graph/codelijst-csor-kwantificeerbaar-aspect`
- Aantal concepten: 119

## Bestandsstructuur

```
src/main/resources/be/vlaanderen/omgeving/data/id/conceptscheme/csor/kwantificeerbareaspect/
├── kwantificeerbareaspecten.ttl    # Turtle-serialisatie (hoofdbestand)
├── kwantificeerbareaspecten.nt     # N-Triples-serialisatie
└── kwantificeerbareaspecten.rj     # RDF/JSON-serialisatie
```

## Gebruikte standaarden

| Prefix | Namespace | Doel |
|--------|-----------|------|
| `skos` | `http://www.w3.org/2004/02/skos/core#` | Concept scheme structuur |
| `csor` | `https://data.omgeving.vlaanderen.be/ns/csor#` | CSOR-specifieke eigenschappen |
| `dcterms` | `http://purl.org/dc/terms/` | Metadata (Dublin Core) |
| `iadopt` | `https://w3id.org/iadopt/ont/` | I-ADOPT observatieraamwerk |
| `owl` | `http://www.w3.org/2002/07/owl#` | OWL-annotaties (bv. `owl:deprecated`) |
| `qudt` | `http://qudt.org/schema/qudt/` | Eenheden en grootheden |
| `rdf` | `http://www.w3.org/1999/02/22-rdf-syntax-ns#` | RDF-basistypes |
| `rdfs` | `http://www.w3.org/2000/01/rdf-schema#` | RDF Schema |
| `xsd` | `http://www.w3.org/2001/XMLSchema#` | XML Schema datatypes |

## Eigenschappen per concept

Elk `csor:KwantificeerbaarAspect` heeft de volgende eigenschappen:

| Eigenschap | Beschrijving |
|------------|--------------|
| `skos:prefLabel` | Nederlandse benaming |
| `skos:notation` | Uniek symbool/code (bv. `TEMP`, `MASSAVERH`) |
| `csor:symbool` | Symbool (gelijk aan `skos:notation`) |
| `csor:kwantificeerbaarAspectType` | Type: `INDIVIDUELE_OBSERVATIE` of `VRACHT` |
| `csor:natuurkundigeDimensie` | Verwijzing naar de natuurkundige dimensie |
| `csor:eenheden` | Toegelaten eenheden voor dit aspect |
| `csor:resultaatType` | Type meetresultaat |

## Licentie

[GNU General Public License v3](LICENSE)
