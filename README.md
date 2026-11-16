# Velkajärjestely.fi-skill

Skill auttaa agenttia hakemaan ja lukemaan [Velkajärjestely.fi:n](https://xn--velkajrjestely-bib.fi/) tietopankin ohjeita ja artikkeleita MCP-palvelun kautta. Tiedot haetaan käyttöhetkellä ja vastauksiin liitetään lähdelinkit.

## MCP-palvelun käyttöehdot

Yksityishenkilö voi käyttää MCP-yhteyttä maksutta henkilökohtaisiin tarkoituksiinsa. Yritykset, yhteisöt ja muut kuin yksityishenkilöt tarvitsevat palvelun käyttöön kaupallisen sopimuksen Sendanorin kanssa. Sopimus tarvitaan myös, kun yrittäjä käyttää yhteyttä elinkeinotoiminnassaan tai kaupallinen toimija liittää sen omaan tuotteeseensa tai palveluunsa. Yhteyden käyttö ei vaadi kirjautumista, mutta se ei poista sopimuksen tarvetta. Lisätiedot ja yhteystiedot: [Velkajärjestely.fi:n käyttöehdot](https://xn--velkajrjestely-bib.fi/kayttoehdot).

## Asenna skill

Lataa [versio 1.0.0 (ZIP)](dist/velkajarjestely-1.0.0.zip). ZIP sisältää `velkajarjestely`-kansion, jonka sisällä on `SKILL.md`.

- **Codex:** pura ZIP käyttäjäkohtaiseen `~/.agents/skills/`-hakemistoon, jolloin tiedosto on `~/.agents/skills/velkajarjestely/SKILL.md`. Käynnistä Codex tarvittaessa uudelleen. Katso [Codexin skill-ohje](https://developers.openai.com/codex/skills/).
- **Claude Code:** pura ZIP hakemistoon `~/.claude/skills/`, jolloin tiedosto on `~/.claude/skills/velkajarjestely/SKILL.md`. Katso [Claude Coden skill-ohje](https://code.claude.com/docs/en/skills).
- **Claude (verkko tai työpöytä):** lisää ZIP kohdassa Customize → Skills → + → Create skill → Upload a skill. Skillien käyttö edellyttää koodin suorittamisen käyttöönottoa. Katso [Clauden skill-asennusohje](https://support.claude.com/en/articles/12512180-use-skills-in-claude).

## Lisää MCP-yhteys

Skill ja MCP-yhteys ovat erillisiä. Skillin `agents/openai.yaml` ilmoittaa riippuvuuden Codexille, mutta automaattinen yhdistäminen riippuu sovelluksesta. Lisää palvelin tarvittaessa erikseen. Osoite on `https://xn--velkajrjestely-bib.fi/mcp`; siirtotapa on Streamable HTTP eikä kirjautumista tarvita.

Codex CLI ([ohje](https://developers.openai.com/codex/mcp/)):

```sh
codex mcp add velkajarjestely --url https://xn--velkajrjestely-bib.fi/mcp
```

Claude Code ([ohje](https://code.claude.com/docs/en/mcp)):

```sh
claude mcp add --transport http --scope user velkajarjestely https://xn--velkajrjestely-bib.fi/mcp
```

Muissa Claude-sovelluksissa lisää etäpalvelin sovelluksen MCP-liittimien asetuksista, jos käytössä oleva versio ja tilaus tukevat sitä. Varmista yhteys sovelluksessa ennen käyttöä.

## Lisenssi

Skillin tiedostot ovat [MIT-lisensoituja](LICENSE). Lisenssi ei määritä MCP-palvelun tai sivustosisältöjen käyttöoikeuksia; niitä koskevat Velkajärjestely.fi:n käyttöehdot.
