I am sending the tabs Kriterien, Produkt and Richtwerte from a web app developed in PHP. I need to reverse engineer it to understand how they designed the database.Create an entity relationship diagram in mermaid to show how their database may be organized.

Here are some extra information about those tabs:

# Kriterien tab

The last children it the "Kriterien" tree has some extra information. What I mean by last children is the deepest you can go in the folder structure. It can be one, two or three levels, for example "6. Entsorgung", "4. 1. Grenzwert für Lösungsmittelgehalt in Bitumenmassen" and "1. 2. 1. Innovative, klimarelev. Heizsysteme, Niedertemperaturhzg., Warmwasserbereitung" respectivelly.

- A tab called Beschreibung, which contains the text sections:

Anforderung, Nachweis für Hersteller, Ziel und Nutzen and Verwendung

- A tab Produkte, which has a table with the columns Titel and Firma

- A tab Relevante Produktgruppen, which references the Produkt table.

# Produkte tab

The produkte also has extra information at the last children. But the intermediate folders work like a filter for products too.

- There is a table for Aufbauten, one for Bauprodukte, and one for Haustechnik.

Aufbauten has the following columns:
 Produktindex
 Titel (fix ausgewählt)
 Firmenname
 Ort
 Land
 Spez. Wärmeleitfähigkeit (λ)
 PENRT Nicht erneuerbare Primärenergie, total (pro m²)
 GWP-total Globales Erwärmungspotenzial - total (pro m²)
 AP Versauerungspotential von Boden und Wasser (pro m²)
 Datum der letzten Änderung
 Neue Produkte

Bauprodukte has the columns:
Produktindex
 Titel (fix ausgewählt)
 Firmenname
 Ort
 Land
 Spez. Wärmeleitfähigkeit (λ)
 Wärmedurchgangskoef. Fenster (Uw)
 Wärmedurchgangskoef. Rahmen (Uf)
 Wärmedurchgangskoef. Verglasung (Ug)
 Energiedurchlassgrad (g)
 Dichte (ρ)
 Wärmedurchgangskoef. Tür (UD)
 Diffusionswiderstand (μ)
 Wärmespeicherkapazität (c)
 PENRT Nicht erneuerbare Primärenergie, total (pro kg)
 GWP-total Globales Erwärmungspotenzial - total (pro kg)
 AP Versauerungspotential von Boden und Wasser (pro kg)
 PENRT Nicht erneuerbare Primärenergie, total (pro m²)
 GWP-total Globales Erwärmungspotenzial - total (pro m²)
 AP Versauerungspotential von Boden und Wasser (pro m²)
 Anteil nachwachsende Rohstoffe
 Anteil fossile Rohstoffe
 Anteil metallische Rohstoffe
 Anteil Recyclingstoffe
 Anteil mineralische Rohstoffe
 Anteil Bitumen
 Anteil halogenorg. Verbindung
 Datum der letzten Änderung
 Neue Produkte

Haustechnik has the columns:
 Produktindex
 Titel (fix ausgewählt)
 Firmenname
 Ort
 Land
 Spez. Wärmeleitfähigkeit (λ)
 Dichte (ρ)
 Diffusionswiderstand (μ)
 Wärmespeicherkapazität (c)
 PENRT Nicht erneuerbare Primärenergie, total (pro kg)
 GWP-total Globales Erwärmungspotenzial - total (pro kg)
 AP Versauerungspotential von Boden und Wasser (pro kg)
 Anteil nachwachsende Rohstoffe
 Anteil fossile Rohstoffe
 Anteil metallische Rohstoffe
 Anteil Recyclingstoffe
 Anteil mineralische Rohstoffe
 Anteil Bitumen
 Anteil halogenorg. Verbindung
 Nennwärmeleistung
 Kleinste Wärmeleistung
 Wirkungsgrad (bei Nennwärmeleistung)
 Wirkungsgrad (bei kleinster Wärmeleistung)
 CO (bei Nennwärmeleistung)
 OGC (bei Nennwärmeleistung)
 Staub (bei Nennwärmeleistung)
 NOx (bei Nennwärmeleistung)
 Datum der letzten Änderung
 Neue Produkte

- The last children also have an extra tab called "Relevante Kriterien" which link back to the Kriterien table.

# Firmen tab

Is just a list with all the companies sorted alphabetically.
The Firma, company in German, has a description and basic information like address, email, telephone, name, and an image place for the logo.
It can also have the fields Produkte, Aufbauten, Vertrieb. To link a product to a specific company.

# Richtwerte tab

This is actually comprised of multiple Katalogs: Kennwerte 2025 A2; IBO-Richtwerte 2020; IBO-Richtwerte 2012; aspern klimafit 2.0; ökobaudat. Each one can have the categories Bauprodukte, Haustechnik, and Prozesse.

Bauprodukte has the columns:
Titel (fix ausgewählt)
Spez. Wärmeleitfähigkeit (λ)
Wärmedurchgangskoef. Rahmen (Uf)
Wärmedurchgangskoef. Verglasung (Ug)
Energiedurchlassgrad (g)
Dichte (ρ)
Wärmedurchgangskoef. Tür (UD)
Diffusionswiderstand (μ)
Wärmespeicherkapazität (c)
PENRT Nicht erneuerbare Primärenergie, total (pro kg)
GWP-total Globales Erwärmungspotenzial - total (pro kg)
AP Versauerungspotential von Boden und Wasser (pro kg)
PENRT Nicht erneuerbare Primärenergie, total (pro m²)
GWP-total Globales Erwärmungspotenzial - total (pro m²)
AP Versauerungspotential von Boden und Wasser (pro m²)
Datum der letzten Änderung

Haustechnik has the columns:
Titel (fix ausgewählt)
Spez. Wärmeleitfähigkeit (λ)
Dichte (ρ)
Wärmespeicherkapazität (c)
PENRT Nicht erneuerbare Primärenergie, total (pro kg)
GWP-total Globales Erwärmungspotenzial - total (pro kg)
AP Versauerungspotential von Boden und Wasser (pro kg)
PENRT Nicht erneuerbare Primärenergie, total (pro m²)
GWP-total Globales Erwärmungspotenzial - total (pro m²)
AP Versauerungspotential von Boden und Wasser (pro m²)
Datum der letzten Änderung

Prozesse has the columns:
Titel (fix ausgewählt)
PENRT Nicht erneuerbare Primärenergie, total (pro kg)
GWP-total Globales Erwärmungspotenzial - total (pro kg)
AP Versauerungspotential von Boden und Wasser (pro kg)
PENRT Nicht erneuerbare Primärenergie, total (pro m²)
GWP-total Globales Erwärmungspotenzial - total (pro m²)
AP Versauerungspotential von Boden und Wasser (pro m²)
Datum der letzten Änderung

When selecting one item from the table you get the Name, description, category, and another set of items in Kennwerte, for example: Bauphysikalische Kennwerte, Bauökologische Kennwerte: Ecoinvent A1.
