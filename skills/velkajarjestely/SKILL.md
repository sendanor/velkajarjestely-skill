---
name: velkajarjestely
description: Hyödynnä Velkajärjestely.fi:n ajankohtaisia artikkeleita ja tietopankkia, kun käyttäjä kysyy velkajärjestelystä tai pyytää sivuston sisältöihin perustuvaa selvitystä.
---

# Velkajärjestely.fi

Hae tiedot MCP-palvelusta käyttöhetkellä. Palvelin on `velkajarjestely`, osoite `https://xn--velkajrjestely-bib.fi/mcp` (Streamable HTTP, ei kirjautumista). Tarkista käytettävissä olevien työkalujen ajantasaiset skeemat ennen kutsuja.

- `search`: anna `query` (1–500 merkkiä); tulokset sisältävät tunnuksen, otsikon ja alkuperäisen URL-osoitteen.
- `fetch`: anna hakutuloksen `id` (1–200 merkkiä) ja lue olennaiset dokumentit kokonaan ennen vastaamista. Tulos sisältää tekstin, URL-osoitteen ja metatiedot.
- `list_documents`: tarvittaessa selaa julkaisuja; valinnaiset `collection` (`all`, `knowledge` tai `news`), `updated_since` (aikaleima aikavyöhykkeineen), `include_undated`, `topic_id`, `limit` (1–100) ja `cursor`. Jatka tarvittaessa tuloksen `next_cursor`-arvolla. Tuntemattomat päivitysajat sisältyvät oletuksena.

Vastaa selkeällä suomella ja liitä väitteiden yhteyteen luettujen alkuperäisten sivujen linkit. Huomioi julkaisun, päivityksen, tiedon ja tarkistuksen päivämäärät (`published_at`, `updated_at`, `information_date`, `reviewed_on`); puuttuva päivämäärä ei osoita ajantasaisuutta. Erota lakiehdotukset ja niiden valmistelu voimassa olevasta laista. Tarkista voimassaolo ja olennainen lainsäädäntö tarvittaessa virallisista lähteistä ja linkitä myös niihin. Kerro, jos tieto puuttuu, ajantasaisuus jää epäselväksi tai MCP-yhteys tai lähteen luku epäonnistuu; älä keksi sisältöä tai lähteitä.
