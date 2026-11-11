# Kaip pridėti klausimų

Programa nieko nežino apie temas – viską skaito iš `data/`.

## Naujas klausimas
Atidarykite reikiamą `data/*.json` ir pridėkite objektą:

    {"tema":"Naujos temos pavadinimas","klausimas":"...?","atsakymai":["A","B","C"],"teisingas":[1]}

- `teisingas` – teisingo atsakymo numeris nuo 0 (keli numeriai = keli teisingi, pvz. [0,2]).
- Nauja `tema` atsiranda sąraše automatiškai.
- Paveikslėliui: `"vaizdas":"media/image99.png"`.

## Naujas dalykas (pvz. iš naujų skaidrių)
1. Sukurkite `data/mano_dalykas.json` (tas pats formatas).
2. Į `data/manifest.json` įrašykite eilutę:
   {"id":"mano","title":"Mano dalykas","file":"mano_dalykas.json"}
3. Pasirinktinai grupės: "groups":[{"title":"1 atsiskaitymas","topics":["Tema A","Tema B"]}]

## Paleidimas
Per serverį (ne dvigubu paspaudimu): `python3 -m http.server`, tada http://localhost:8000
arba GitHub Pages / Netlify.
