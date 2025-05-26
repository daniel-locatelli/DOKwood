erDiagram
BAUTEIL ||--o{ BAUTEIL_TYP : ist_vom_typ
BAUTEIL ||--o{ BAUTEIL_LUFTSCHALLWERTE : hat_luftschallwerte
BAUTEIL ||--o{ BAUTEIL_TRITTSCHALLWERTE : hat_trittschallwerte
BAUTEIL ||--o{ BAUTEIL_AUFBAU_SCHICHT : hat_schicht
BAUTEIL ||--o{ BAUTEIL_WERTE_FREQUENZEN : hat_frequenzwerte
BAUTEIL ||--o{ OEKOLOGISCHE_INDIKATOREN_SUMMARISCH : hat_sum_oeko_indikatoren
BAUTEIL ||--o{ SCHALLDAEMM_HERKUNFT : hat_herkunft
BAUTEIL ||--o{ ESTRICH_TYP : hat_estrich_typ
BAUTEIL ||--o{ BEWEHRUNG_TYP : hat_bewehrung_typ
BAUTEIL ||--o{ DAEMMUNG_HOHLRAUM : hat_hohlraumdaemmung
BAUTEIL ||--o{ BEKLEIDUNG_ART : hat_bekleidung_art
BAUTEIL ||--o{ UNTERKONSTRUKTION_TYP : hat_unterkonstruktion_typ

    PRODUKT ||--o{ HERSTELLER : hat_hersteller
    PRODUKT ||--o{ PRODUKT_KATEGORIE : ist_vom_typ
    PRODUKT ||--o{ MATERIAL_KATEGORIE : hat_materialkategorie
    PRODUKT ||--o{ MATERIAL_TYP : hat_materialtyp
    PRODUKT ||--o{ BRANDVERHALTENSGRUPPE : hat_brandverhaltensgruppe
    PRODUKT ||--o{ FUNKTION : hat_funktion
    PRODUKT ||--o{ EINSATZBEREICH : hat_einsatzbereich
    PRODUKT ||--o{ BAUSTOFFKENNWERTE_SIA : hat_sia_kennwerte
    PRODUKT ||--o{ OEKOLOGISCHE_INDIKATOREN_SUMMARISCH : hat_sum_oeko_indikatoren
    PRODUKT ||--o{ HOLZSCHUTZMITTEL_WIRKSAMKEIT : hat_hsm_wirksamkeit
    PRODUKT ||--o{ HOLZSCHUTZMITTEL_VERWENDERKATEGORIE : hat_hsm_verwenderkategorie
    PRODUKT ||--o{ HOLZSCHUTZMITTEL_AGGREGATSZUSTAND : hat_hsm_aggregatszustand
    PRODUKT ||--o{ HOLZSCHUTZMITTEL_GEBRAUCHSKLASSE : hat_hsm_gebrauchsklasse
    PRODUKT ||--o{ HOLZSCHUTZMITTEL_VERWENDUNGSZIEL : hat_hsm_verwendungsziel
    PRODUKT ||--o{ HOLZSCHUTZMITTEL_VERWENDUNGSMETHODE : hat_hsm_verwendungsmethode
    PRODUKT ||--o{ FORMALDEHYD_INFORMATION : hat_formaldehyd_info
    PRODUKT ||--o{ HOLZART_SPEZIES : hat_holzart_spezies
    PRODUKT ||--o{ HERKUNFT_ORT : hat_holz_herkunft

    BAUSTOFFKENNWERTE_SIA ||--o{ MATERIALGRUPPE_SIA : ist_materialgruppe

    OEKOBILANZ_DATEN ||--o{ KBOB_KATEGORIE : ist_kbob_kategorie

    HOLZART ||--o{ HOLZTYP : ist_vom_typ
    HOLZART ||--o{ HOLZART_GATTUNG : hat_gattung
    HOLZART ||--o{ HOLZART_SPEZIES : hat_spezies
    HOLZART ||--o{ HERKUNFT_ORT : hat_herkunftsort
    HOLZART ||--o{ OEKOLOGISCHE_INDIKATOREN_SUMMARISCH : hat_sum_oeko_indikatoren

    HOLZART_SPEZIES ||--o{ HOLZART_GATTUNG : ist_spezies_von

    BAUTEIL_AUFBAU_SCHICHT ||--o{ PRODUKT : verwendet_produkt
    BAUTEIL_AUFBAU_SCHICHT ||--o{ OEKOBILANZ_DATEN : hat_kbob_daten_herstellung
    BAUTEIL_AUFBAU_SCHICHT ||--o{ OEKOBILANZ_DATEN : hat_kbob_daten_entsorgung

    OEKOLOGISCHE_INDIKATOREN_SUMMARISCH ||--o{ OEKOLOGISCHE_INDIKATOREN_DETAIL : hat_detail
    OEKOLOGISCHE_INDIKATOREN_SUMMARISCH ||--o{ OEKOBILANZ_DATEN : basiert_auf

    BAUTEIL {
        VARCHAR lignum_id_nr PK "Lignum ID-№"
        VARCHAR katalognummer "Katalognummer"
        VARCHAR quelle_konstruktion "Quelle Konstruktion"
        VARCHAR grundkonstruktion "Grundkonstruktion"
        VARCHAR fassadentyp "Fassadentyp"
        VARCHAR beplankung "Beplankung"
        VARCHAR bekleidung "Bekleidung"
        VARCHAR ref_brandschutz "Ref. Brandschutz"
        DECIMAL aufbauhoehe_mm "Aufbauhöhe [mm]"
        DECIMAL gewicht_kg_m2 "Gewicht [kg/m²]"
        DECIMAL u_wert_wm2k "U-Wert [W/m²K]"
        DECIMAL gwp_kg_co2_eq_m2 "GWP [kg CO₂-eq/m²]"
        VARCHAR typ_schalldaemmwerte "Typ Schalldämmwerte"
        TEXT beschreibung "Beschreibung"
        DECIMAL umweltbelastungspunkte_ubp_m2 "Umweltbelastungspunkte (UBP) [UBP'21/m²]"
        DECIMAL primaerenergie_nicht_erneuerbar_total_pe_nrt_kwh_oil_eq_m2 "Primärenergie nicht erneuerbar total (PE_NRT) [kWh oil-eq/m²]"
        DECIMAL treibhausgasemissionen_total_gwp_total_kg_co2_m2 "Treibhausgasemissionen total (GWP_total) [kg CO₂/m²]"
        DECIMAL biogener_kohlenstoff_im_produkt_enthalten_kg_co2_m2 "Biogener Kohlenstoff im Produkt enthalten [kg CO₂/m²]"
        DECIMAL biogene_kohlenstoffspeicherung_kg_c_m2 "Biogene Kohlenstoffspeicherung [kg C/m²]"
    }

    BAUTEIL_TYP {
        VARCHAR typ_id PK "Typ ID"
        VARCHAR typ_name "Typ Name"
    }

    BAUTEIL_LUFTSCHALLWERTE {
        VARCHAR lignum_id_nr PK,FK "Lignum ID-№"
        DECIMAL rw_wert_db "Rw [dB]"
        DECIMAL c_wert_db "C [dB]"
        DECIMAL c50_3150_wert_db "C50-3150 [dB]"
        DECIMAL ctr_wert_db "Ctr [dB]"
    }

    BAUTEIL_TRITTSCHALLWERTE {
        VARCHAR lignum_id_nr PK,FK "Lignum ID-№"
        DECIMAL lnw_wert_db "Lnw [dB]"
        DECIMAL ci_wert_db "CI [dB]"
        DECIMAL ci50_2500_wert_db "CI50-2500 [dB]"
    }

    BAUTEIL_AUFBAU_SCHICHT {
        VARCHAR schicht_id PK "Schicht ID"
        VARCHAR lignum_id_nr FK "Lignum ID-№ (Bauteil)"
        VARCHAR produkt_lignum_id_nr FK "Lignum ID-№ (Produkt)"
        VARCHAR schicht_name "Schicht Name"
        VARCHAR produkt_bezeichnung "Produkt Bezeichnung"
        VARCHAR hersteller_name "Hersteller Name"
        DECIMAL dicke_mm "Dicke [mm]"
        DECIMAL gewicht_kg_m2 "Gewicht [kg/m²]"
        DECIMAL breite_b_mm "Breite (b) [mm]"
        DECIMAL achsabstand_e_mm "Achsabstand (e) [mm]"
        VARCHAR kbob_id_nr_herstellung FK "KBOB ID-№ Herstellung"
        VARCHAR kbob_id_nr_entsorgung FK "KBOB ID-№ Entsorgung"
    }

    BAUTEIL_WERTE_FREQUENZEN {
        VARCHAR frequenzwert_id PK "Frequenzwert ID"
        VARCHAR lignum_id_nr FK "Lignum ID-№ (Bauteil)"
        VARCHAR schalltyp "Schalltyp"
        VARCHAR farbe "Farbe"
        VARCHAR typ "Typ"
        INT frequenz_25_hz "Frequenz 25 Hz"
        INT frequenz_32_hz "Frequenz 32 Hz"
        INT frequenz_40_hz "Frequenz 40 Hz"
        INT frequenz_50_hz "Frequenz 50 Hz"
        INT frequenz_63_hz "Frequenz 63 Hz"
        INT frequenz_80_hz "Frequenz 80 Hz"
        INT frequenz_100_hz "Frequenz 100 Hz"
        INT frequenz_125_hz "Frequenz 125 Hz"
        INT frequenz_160_hz "Frequenz 160 Hz"
        INT frequenz_200_hz "Frequenz 200 Hz"
        INT frequenz_250_hz "Frequenz 250 Hz"
        INT frequenz_315_hz "Frequenz 315 Hz"
        INT frequenz_400_hz "Frequenz 400 Hz"
        INT frequenz_500_hz "Frequenz 500 Hz"
        INT frequenz_630_hz "Frequenz 630 Hz"
        INT frequenz_800_hz "Frequenz 800 Hz"
        INT frequenz_1000_hz "Frequenz 1000 Hz"
        INT frequenz_1250_hz "Frequenz 1250 Hz"
        INT frequenz_1600_hz "Frequenz 1600 Hz"
        INT frequenz_2000_hz "Frequenz 2000 Hz"
        INT frequenz_2500_hz "Frequenz 2500 Hz"
        INT frequenz_3150_hz "Frequenz 3150 Hz"
        INT frequenz_4000_hz "Frequenz 4000 Hz"
        INT frequenz_5000_hz "Frequenz 5000 Hz"
    }

    OEKOLOGISCHE_INDIKATOREN_SUMMARISCH {
        VARCHAR oeko_indikator_id PK "Öko Indikator ID"
        VARCHAR bezugs_id FK "Bezugs ID (Bauteil/Produkt/Holzart)"
        VARCHAR kbob_id_nr_herstellung FK "KBOB ID-№ Herstellung"
        VARCHAR indikator_name "Indikator Name"
        DECIMAL wert "Wert"
        VARCHAR einheit "Einheit"
        VARCHAR link_bsdd "Link bSDD"
        VARCHAR module "Module"
        VARCHAR link_module "Link Module"
    }

    OEKOLOGISCHE_INDIKATOREN_DETAIL {
        VARCHAR detail_id PK "Detail ID"
        VARCHAR oeko_indikator_id FK "Öko Indikator ID (Summary)"
        VARCHAR detail_name "Detail Name"
        DECIMAL wert "Wert"
        VARCHAR einheit "Einheit"
        VARCHAR link_bsdd "Link bSDD"
        VARCHAR module "Module"
        VARCHAR link_module "Link Module"
    }

    HERSTELLER {
        VARCHAR hersteller_id PK "Hersteller ID"
        VARCHAR hersteller_name "Hersteller Name"
        VARCHAR land "Land"
    }

    SCHALLDAEMM_HERKUNFT {
        VARCHAR herkunft_id PK "Herkunft ID"
        VARCHAR herkunft_name "Herkunft Name"
    }

    ESTRICH_TYP {
        VARCHAR estrich_id PK "Estrich ID"
        VARCHAR estrich_name "Estrich Name"
    }

    BEWEHRUNG_TYP {
        VARCHAR bewehrung_id PK "Bewehrung ID"
        VARCHAR bewehrung_name "Bewehrung Name"
    }

    DAEMMUNG_HOHLRAUM {
        VARCHAR daemmung_id PK "Dämmung ID"
        VARCHAR daemmung_name "Dämmung Name"
    }

    BEKLEIDUNG_ART {
        VARCHAR bekleidung_art_id PK "Bekleidung Art ID"
        VARCHAR bekleidung_art_name "Bekleidung Art Name"
    }

    UNTERKONSTRUKTION_TYP {
        VARCHAR unterkonstruktion_id PK "Unterkonstruktion ID"
        VARCHAR unterkonstruktion_name "Unterkonstruktion Name"
    }

    PRODUKT {
        VARCHAR lignum_id_nr PK "Lignum ID-№"
        VARCHAR produktname "Produktname"
        VARCHAR produktfamilie "Produktfamilie"
        VARCHAR produktgruppe "Produktgruppe"
        VARCHAR statik_hbt2 "Statik HBT2"
        VARCHAR bauproduktenorm "Bauproduktenorm"
        DECIMAL dichte_kg_m3 "Dichte [kg/m³]"
        DECIMAL produktdicke_mm "Produktdicke [mm]"
        DECIMAL breite_mm "Breite [mm]"
        DECIMAL laenge_mm "Länge [mm]"
        INT anzahl_pro_verpackungseinheit_stk "Anzahl pro Verpackungseinheit [Stk.]"
    }

    PRODUKT_KATEGORIE {
        VARCHAR kategorie_id PK "Kategorie ID"
        VARCHAR kategorie_name "Kategorie Name"
    }

    BAUSTOFFKENNWERTE_SIA {
        VARCHAR sia_nr PK "SIA-Nr"
        VARCHAR produktbezeichnung "Produktbezeichnung"
        VARCHAR bemerkungen "Bemerkungen"
        VARCHAR hersteller_info "Hersteller Info"
        VARCHAR gueltig_bis "Gültig bis"
        VARCHAR datenstand "Datenstand"
        VARCHAR quelle "Quelle"
        DECIMAL rohdichte_kg_m3 "Rohdichte ρ [kg/m³]"
        DECIMAL waermeleitfaehigkeit_wmk "Wärmeleitfähigkeit λ [W/mK]"
        DECIMAL waermekapazitaet_wh_kgk "Wärmekapazität [Wh/kgK]"
        DECIMAL waermekapazitaet_j_kgk "Wärmekapazität [J/kgK]"
        DECIMAL dampfsperrwert_trocken "Dampfsperrwert (trocken)"
        DECIMAL dampfsperrwert_feucht "Dampfsperrwert (feucht)"
        BOOLEAN en_iso_10456_2007_tab_3 "EN ISO 10456:2007 Tab. 3"
        BOOLEAN en_iso_10456_2007_tab_4 "EN ISO 10456:2007 Tab. 4"
        BOOLEAN sn_en_1745_2020_anh_a "SN EN 1745:2020 Anhang A"
        BOOLEAN sn_en_12524_tab_na_1 "SN EN 12524 Tab. NA.1"
        BOOLEAN sia_279_2018_tab_1 "SIA 279:2018 Tab. 1"
        BOOLEAN building_material_properties "Building Material Properties"
    }

    MATERIALGRUPPE_SIA {
        VARCHAR materialgruppe_id PK "Materialgruppe ID"
        VARCHAR materialgruppe_name "Materialgruppe Name"
    }

    OEKOBILANZ_DATEN {
        VARCHAR kbob_id_nr_herstellung PK "KBOB ID-№ Herstellung"
        VARCHAR uuid_nummer "UUID-Nummer"
        VARCHAR bezeichnung_baumaterial "Bezeichnung Baumaterial"
        VARCHAR kbob_id_nr_entsorgung "KBOB ID-№ Entsorgung"
        VARCHAR bezeichnung_entsorgung "Bezeichnung Entsorgung"
        DECIMAL masse_pro_volumen_kg_m3 "Masse pro Volumen [kg/m³]"
        VARCHAR deklarierte_einheit "Deklarierte Einheit"
        VARCHAR letztes_update "Letztes Update"
        VARCHAR kategorie "Kategorie"
        DECIMAL umweltbelastungspunkte_ubp_kg "Umweltbelastungspunkte (UBP) [UBP/kg]"
        DECIMAL umweltbelastungspunkte_ubp_pro_kg "UBP Herstellung [UBP/kg]"
        DECIMAL umweltbelastungspunkte_ubp_dis_kg "UBP Entsorgung [UBP/kg]"
        DECIMAL primaerenergie_total_pe_t_kwh_oil_eq_kg "Primärenergie total (PE_T) [kWh oil-eq/kg]"
        DECIMAL primaerenergie_herstellung_pe_pro_kwh_oil_eq_kg "PE Herstellung [kWh oil-eq/kg]"
        DECIMAL primaerenergie_herstellung_energetisch_genutzt_pe_e_pro_kwh_oil_eq_kg "PE Herstellung energetisch genutzt [kWh oil-eq/kg]"
        DECIMAL primaerenergie_herstellung_stofflich_gebunden_pe_m_pro_kwh_oil_eq_kg "PE Herstellung stofflich gebunden [kWh oil-eq/kg]"
        DECIMAL primaerenergie_entsorgung_pe_dis_kwh_oil_eq_kg "PE Entsorgung [kWh oil-eq/kg]"
        DECIMAL primaerenergie_erneuerbar_total_pe_rt_kwh_oil_eq_kg "PE erneuerbar total (PE_RT) [kWh oil-eq/kg]"
        DECIMAL primaerenergie_erneuerbar_herstellung_pe_rt_pro_kwh_oil_eq_kg "PE erneuerbar Herstellung [kWh oil-eq/kg]"
        DECIMAL primaerenergie_erneuerbar_herstellung_energetisch_genutzt_pe_re_pro_kwh_oil_eq_kg "PE erneuerbar Herstellung energetisch genutzt [kWh oil-eq/kg]"
        DECIMAL primaerenergie_erneuerbar_herstellung_stofflich_gebunden_pe_rm_pro_kwh_oil_eq_kg "PE erneuerbar Herstellung stofflich gebunden [kWh oil-eq/kg]"
        DECIMAL primaerenergie_erneuerbar_entsorgung_pe_rt_dis_kwh_oil_eq_kg "PE erneuerbar Entsorgung [kWh oil-eq/kg]"
        DECIMAL primaerenergie_nicht_erneuerbar_total_pe_nrt_kwh_oil_eq_kg "PE nicht erneuerbar total (PE_NRT) [kWh oil-eq/kg]"
        DECIMAL primaerenergie_nicht_erneuerbar_herstellung_pe_nrt_pro_kwh_oil_eq_kg "PE nicht erneuerbar Herstellung [kWh oil-eq/kg]"
        DECIMAL primaerenergie_nicht_erneuerbar_herstellung_energetisch_genutzt_pe_nre_pro_kwh_oil_eq_kg "PE nicht erneuerbar Herstellung energetisch genutzt [kWh oil-eq/kg]"
        DECIMAL primaerenergie_nicht_erneuerbar_herstellung_stofflich_gebunden_pe_nrm_pro_kwh_oil_eq_kg "PE nicht erneuerbar Herstellung stofflich gebunden [kWh oil-eq/kg]"
        DECIMAL primaerenergie_nicht_erneuerbar_entsorgung_pe_nrt_dis_kwh_oil_eq_kg "PE nicht erneuerbar Entsorgung [kWh oil-eq/kg]"
        DECIMAL treibhausgasemissionen_total_gwp_total_kg_co2_eq_kg "Treibhausgasemissionen total (GWP_total) [kg CO₂-eq/kg]"
        DECIMAL treibhausgasemissionen_herstellung_gwp_pro_kg_co2_eq_kg "GWP Herstellung [kg CO₂-eq/kg]"
        DECIMAL treibhausgasemissionen_entsorgung_gwp_dis_kg_co2_eq_kg "GWP Entsorgung [kg CO₂-eq/kg]"
        DECIMAL biogener_kohlenstoff_im_produkt_enthalten_bio_c_kg_co2_eq_kg "Biogener Kohlenstoff im Produkt enthalten (bio-C) [kg CO₂-eq/kg]"
        DECIMAL biogene_kohlenstoffspeicherrung_bio_c_kg_c_kg "Biogene Kohlenstoffspeicherung (bio-C) [kg C/kg]"
    }

    KBOB_KATEGORIE {
        VARCHAR kategorie_id PK "Kategorie ID"
        VARCHAR kategorie_name "Kategorie Name"
    }

    HOLZART {
        VARCHAR lignum_id_nr PK "Lignum ID-№"
        VARCHAR botanischer_name "Botanischer Name"
        VARCHAR holzcode "Holzcode"
        VARCHAR vorkommen "Vorkommen"
        DECIMAL rohdichte_kg_m3 "Rohdichte [kg/m³]"
        DECIMAL el_modul_n_mm2 "EL Modul [N/mm²]"
        DECIMAL biegefestigkeit_n_mm2 "Biegefestigkeit [N/mm²]"
        DECIMAL druckfestigkeit_n_mm2 "Druckfestigkeit [N/mm²]"
        DECIMAL zugfestigkeit_n_mm2 "Zugfestigkeit [N/mm²]"
        DECIMAL scherfestigkeit_n_mm2 "Scherfestigkeit [N/mm²]"
        DECIMAL haerte_brinell_n_mm2 "Härte Brinell [N/mm²]"
        DECIMAL druck_schwindmass_prozent "Druck-Schwindmass [%]"
        DECIMAL tangential_schwindmass_prozent "Tangential-Schwindmass [%]"
        DECIMAL radial_schwindmass_prozent "Radial-Schwindmass [%]"
        DECIMAL dimensionsstabilitaet_prozent "Dimensionsstabilität [%]"
        TEXT kommentar "Kommentar"
        VARCHAR quellengabe "Quellengabe"
    }

    HOLZTYP {
        VARCHAR holztyp_id PK "Holztyp ID"
        VARCHAR holztyp_name "Holztyp Name"
    }

    HOLZART_GATTUNG {
        VARCHAR gattung_code PK "Gattung Code"
        VARCHAR gattung_name "Gattung Name"
    }

    HOLZART_SPEZIES {
        VARCHAR spezies_code PK "Spezies Code"
        VARCHAR spezies_name "Spezies Name"
        VARCHAR gattung_code FK "Gattung Code"
    }

    HERKUNFT_ORT {
        VARCHAR herkunft_id PK "Herkunft ID"
        VARCHAR herkunft_name "Herkunft Name"
    }

    BRANDVERHALTENSGRUPPE {
        VARCHAR gruppe_id PK "Gruppe ID"
        VARCHAR gruppe_name "Gruppe Name"
    }

    MATERIAL_KATEGORIE {
        VARCHAR kategorie_id PK "Kategorie ID"
        VARCHAR kategorie_name "Kategorie Name"
    }

    MATERIAL_TYP {
        VARCHAR typ_id PK "Typ ID"
        VARCHAR typ_name "Typ Name"
    }

    FUNKTION {
        VARCHAR funktion_id PK "Funktion ID"
        VARCHAR funktion_name "Funktion Name"
    }

    EINSATZBEREICH {
        VARCHAR bereich_id PK "Bereich ID"
        VARCHAR bereich_name "Bereich Name"
    }

    HOLZSCHUTZMITTEL_WIRKSAMKEIT {
        VARCHAR wirksamkeit_id PK "Wirksamkeit ID"
        VARCHAR wirksamkeit_name "Wirksamkeit Name"
    }

    HOLZSCHUTZMITTEL_VERWENDERKATEGORIE {
        VARCHAR kategorie_id PK "Kategorie ID"
        VARCHAR kategorie_name "Kategorie Name"
    }

    HOLZSCHUTZMITTEL_AGGREGATSZUSTAND {
        VARCHAR zustand_id PK "Zustand ID"
        VARCHAR zustand_name "Zustand Name"
    }

    HOLZSCHUTZMITTEL_GEBRAUCHSKLASSE {
        VARCHAR klasse_id PK "Klasse ID"
        VARCHAR klasse_name "Klasse Name"
    }

    HOLZSCHUTZMITTEL_VERWENDUNGSZIEL {
        VARCHAR ziel_id PK "Ziel ID"
        VARCHAR ziel_name "Ziel Name"
    }

    HOLZSCHUTZMITTEL_VERWENDUNGSMETHODE {
        VARCHAR methode_id PK "Methode ID"
        VARCHAR methode_name "Methode Name"
    }

    FORMALDEHYD_INFORMATION {
        VARCHAR info_id PK "Info ID"
        VARCHAR info_level "Info Level"
    }
