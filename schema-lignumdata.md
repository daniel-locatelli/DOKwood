Schemas
pagination{
page	integer
}
translated_prop{
name	string
workingtitle	string
}
object_with_url{
url	string
}
translated_prop_with_url{
name	string
workingtitle	string
url	string
}
cei_bois_guid_translated_prop{
name	string
workingtitle	string
value_guid	string
nullable: true
property_guid	string
nullable: true
unit_guid	string
nullable: true
}
cei_bois_guid_translated_prop_with_url{
name	string
workingtitle	string
url	string
value_guid	string
nullable: true
property_guid	string
nullable: true
unit_guid	string
nullable: true
}
cei_bois_guid_prop{
value	{
oneOf ->	
string
integer
number($double)
}
value_guid	string
nullable: true
property_guid	string
nullable: true
unit_guid	string
nullable: true
}
oekobilanz{
ubp	oekobilanz_guid_prop{
property_guid*	string
nullable: true
value*	number($double)
nullable: true
phase*	{
value	string
value_guid	string
}
unit*	string
nullable: true
unit_guid*	string
nullable: true
unit_html	string
nullable: true
}
ubp-pro	oekobilanz_guid_prop{
property_guid*	string
nullable: true
value*	number($double)
nullable: true
phase*	{
value	string
value_guid	string
}
unit*	string
nullable: true
unit_guid*	string
nullable: true
unit_html	string
nullable: true
}
ubp-dis	oekobilanz_guid_prop{
property_guid*	string
nullable: true
value*	number($double)
nullable: true
phase*	{
value	string
value_guid	string
}
unit*	string
nullable: true
unit_guid*	string
nullable: true
unit_html	string
nullable: true
}
pe	oekobilanz_guid_prop{
property_guid*	string
nullable: true
value*	number($double)
nullable: true
phase*	{
value	string
value_guid	string
}
unit*	string
nullable: true
unit_guid*	string
nullable: true
unit_html	string
nullable: true
}
pe-pro	oekobilanz_guid_prop{
property_guid*	string
nullable: true
value*	number($double)
nullable: true
phase*	{
value	string
value_guid	string
}
unit*	string
nullable: true
unit_guid*	string
nullable: true
unit_html	string
nullable: true
}
pe-hast-ev	oekobilanz_guid_prop{
property_guid*	string
nullable: true
value*	number($double)
nullable: true
phase*	{
value	string
value_guid	string
}
unit*	string
nullable: true
unit_guid*	string
nullable: true
unit_html	string
nullable: true
}
pe-hast-sg	oekobilanz_guid_prop{
property_guid*	string
nullable: true
value*	number($double)
nullable: true
phase*	{
value	string
value_guid	string
}
unit*	string
nullable: true
unit_guid*	string
nullable: true
unit_html	string
nullable: true
}
pe-dis	oekobilanz_guid_prop{
property_guid*	string
nullable: true
value*	number($double)
nullable: true
phase*	{
value	string
value_guid	string
}
unit*	string
nullable: true
unit_guid*	string
nullable: true
unit_html	string
nullable: true
}
pe-re	oekobilanz_guid_prop{
property_guid*	string
nullable: true
value*	number($double)
nullable: true
phase*	{
value	string
value_guid	string
}
unit*	string
nullable: true
unit_guid*	string
nullable: true
unit_html	string
nullable: true
}
pe-re-sg	oekobilanz_guid_prop{
property_guid*	string
nullable: true
value*	number($double)
nullable: true
phase*	{
value	string
value_guid	string
}
unit*	string
nullable: true
unit_guid*	string
nullable: true
unit_html	string
nullable: true
}
pe-re-ev	oekobilanz_guid_prop{
property_guid*	string
nullable: true
value*	number($double)
nullable: true
phase*	{
value	string
value_guid	string
}
unit*	string
nullable: true
unit_guid*	string
nullable: true
unit_html	string
nullable: true
}
pe-re-pro	oekobilanz_guid_prop{
property_guid*	string
nullable: true
value*	number($double)
nullable: true
phase*	{
value	string
value_guid	string
}
unit*	string
nullable: true
unit_guid*	string
nullable: true
unit_html	string
nullable: true
}
pe-re-pro-sg	oekobilanz_guid_prop{
property_guid*	string
nullable: true
value*	number($double)
nullable: true
phase*	{
value	string
value_guid	string
}
unit*	string
nullable: true
unit_guid*	string
nullable: true
unit_html	string
nullable: true
}
pe-re-pro-ev	oekobilanz_guid_prop{
property_guid*	[...]
value*	[...]
phase*	{...}
unit*	[...]
unit_guid*	[...]
unit_html	[...]
}
pe-re-dis	oekobilanz_guid_prop{...}
pe-re-dis-sg	oekobilanz_guid_prop{...}
pe-re-dis-ev	oekobilanz_guid_prop{...}
pe-nr	oekobilanz_guid_prop{...}
pe-nr-sg	oekobilanz_guid_prop{...}
pe-nr-ev	oekobilanz_guid_prop{...}
pe-nr-pro	oekobilanz_guid_prop{...}
pe-nr-pro-sg	oekobilanz_guid_prop{...}
pe-nr-pro-ev	oekobilanz_guid_prop{...}
pe-nr-dis	oekobilanz_guid_prop{...}
pe-nr-dis-sg	oekobilanz_guid_prop{...}
pe-nr-dis-ev	oekobilanz_guid_prop{...}
gwp	oekobilanz_guid_prop{...}
gwp-pro	oekobilanz_guid_prop{...}
gwp-dis	oekobilanz_guid_prop{...}
co2	oekobilanz_guid_prop{...}
co2-pro	oekobilanz_guid_prop{...}
co2-dis	oekobilanz_guid_prop{...}
bio-e	oekobilanz_guid_prop{...}
bio-co2	oekobilanz_guid_prop{...}
bio-c	oekobilanz_guid_prop{...}
}
oekobilanz_guid_prop{
property_guid*	string
nullable: true
value*	number($double)
nullable: true
phase*	{
value	string
value_guid	string
}
unit*	string
nullable: true
unit_guid*	string
nullable: true
unit_html	string
nullable: true
}
cei_bois_guid_base{
property_guid	string
nullable: true
unit_guid	string
nullable: true
}
country{
name	string
workingtitle	string
workingtitle_en	string
nullable: true
code	string
nullable: true
wgsrpd	string
nullable: true
value_guid	string
nullable: true
property_guid	string
nullable: true
unit_guid	string
nullable: true
}
image_with_color{
url	string
color	string
}
image_with_copyright_and_info{
url	string
copyright	string
info	[string]
}
object_with_guid{
value	string
value_guid	string
property_guid	string
unit_guid	string
cei_bois_name	string
}
messwerte{
25	number
32	number
40	number
50	number
63	number
80	number
100	number
125	number
160	number
200	number
250	number
315	number
400	number
500	number
630	number
800	number
1000	number
1250	number
1600	number
2000	number
2500	number
3150	number
4000	number
5000	number
}
bauteil{
id	string
aufbau	[{
produktname	string
produktid	string
herstellername	string
schicht	string
dicke	string
gewicht	string
breite	string
achsabstand	string
aufbau	string
brandverhaltensgruppe	string
grafikfarbcode	string
faserrichtung	string
kbob_id	string
}]
bauteilgruppe	{
ifcorientation	string
name	string
workingtitle	string
}
bauteilname	string
bauteiltyp	translated_prop{
name	string
workingtitle	string
}
bekleidung	translated_prop{
name	string
workingtitle	string
}
beplankung	translated_prop{
name	string
workingtitle	string
}
beschreibung	string
beschwerungkonstruktion	translated_prop{
name	string
workingtitle	string
}
beschwerungtragschicht	translated_prop{
name	string
workingtitle	string
}
brandschutz	string
daemmwerte	{
luftschalldaemmwerte	{
c100_3150	number
c50_3150	number
ctr100_3150	number
rw	number
}
trittschalldaemmwerte	{
lnw	number
ci100_2500	number
ci50_2500	number
}
typschalldaemmwerte	string
}
daemmkonstruktion	translated_prop{
name	string
workingtitle	string
}
created_at	string($date-time)
updated_at	string($date-time)
estrich	translated_prop{
name	string
workingtitle	string
}
fasadentyp	translated_prop{
name	string
workingtitle	string
}
katalognr	string
kommentar	string
laufnummer	string
media	{
detail	string
ifc	string
image_iframe	string
image_jpg	string
print	string
pruefbericht	string
}
messwertsatz	{...}
oekobilanz	oekobilanz{
ubp	oekobilanz_guid_prop{
property_guid*	string
nullable: true
value*	number($double)
nullable: true
phase*	{
value	string
value_guid	string
}
unit*	string
nullable: true
unit_guid*	string
nullable: true
unit_html	string
nullable: true
}
ubp-pro	oekobilanz_guid_prop{
property_guid*	string
nullable: true
value*	number($double)
nullable: true
phase*	{
value	string
value_guid	string
}
unit*	string
nullable: true
unit_guid*	string
nullable: true
unit_html	string
nullable: true
}
ubp-dis	oekobilanz_guid_prop{
property_guid*	string
nullable: true
value*	number($double)
nullable: true
phase*	{
value	string
value_guid	string
}
unit*	string
nullable: true
unit_guid*	string
nullable: true
unit_html	string
nullable: true
}
pe	oekobilanz_guid_prop{
property_guid*	string
nullable: true
value*	number($double)
nullable: true
phase*	{
value	string
value_guid	string
}
unit*	string
nullable: true
unit_guid*	string
nullable: true
unit_html	string
nullable: true
}
pe-pro	oekobilanz_guid_prop{
property_guid*	string
nullable: true
value*	number($double)
nullable: true
phase*	{
value	string
value_guid	string
}
unit*	string
nullable: true
unit_guid*	string
nullable: true
unit_html	string
nullable: true
}
pe-hast-ev	oekobilanz_guid_prop{
property_guid*	string
nullable: true
value*	number($double)
nullable: true
phase*	{
value	string
value_guid	string
}
unit*	string
nullable: true
unit_guid*	string
nullable: true
unit_html	string
nullable: true
}
pe-hast-sg	oekobilanz_guid_prop{
property_guid*	string
nullable: true
value*	number($double)
nullable: true
phase*	{
value	string
value_guid	string
}
unit*	string
nullable: true
unit_guid*	string
nullable: true
unit_html	string
nullable: true
}
pe-dis	oekobilanz_guid_prop{
property_guid*	string
nullable: true
value*	number($double)
nullable: true
phase*	{
value	string
value_guid	string
}
unit*	string
nullable: true
unit_guid*	string
nullable: true
unit_html	string
nullable: true
}
pe-re	oekobilanz_guid_prop{
property_guid*	string
nullable: true
value*	number($double)
nullable: true
phase*	{
value	string
value_guid	string
}
unit*	string
nullable: true
unit_guid*	string
nullable: true
unit_html	string
nullable: true
}
pe-re-sg	oekobilanz_guid_prop{
property_guid*	string
nullable: true
value*	number($double)
nullable: true
phase*	{
value	string
value_guid	string
}
unit*	string
nullable: true
unit_guid*	string
nullable: true
unit_html	string
nullable: true
}
pe-re-ev	oekobilanz_guid_prop{
property_guid*	string
nullable: true
value*	number($double)
nullable: true
phase*	{
value	string
value_guid	string
}
unit*	string
nullable: true
unit_guid*	string
nullable: true
unit_html	string
nullable: true
}
pe-re-pro	oekobilanz_guid_prop{
property_guid*	string
nullable: true
value*	number($double)
nullable: true
phase*	{
value	string
value_guid	string
}
unit*	string
nullable: true
unit_guid*	string
nullable: true
unit_html	string
nullable: true
}
pe-re-pro-sg	oekobilanz_guid_prop{
property_guid*	string
nullable: true
value*	number($double)
nullable: true
phase*	{
value	string
value_guid	string
}
unit*	string
nullable: true
unit_guid*	string
nullable: true
unit_html	string
nullable: true
}
pe-re-pro-ev	oekobilanz_guid_prop{
property_guid*	string
nullable: true
value*	number($double)
nullable: true
phase*	{
value	string
value_guid	string
}
unit*	string
nullable: true
unit_guid*	string
nullable: true
unit_html	string
nullable: true
}
pe-re-dis	oekobilanz_guid_prop{
property_guid*	string
nullable: true
value*	number($double)
nullable: true
phase*	{
value	string
value_guid	string
}
unit*	string
nullable: true
unit_guid*	string
nullable: true
unit_html	string
nullable: true
}
pe-re-dis-sg	oekobilanz_guid_prop{
property_guid*	string
nullable: true
value*	number($double)
nullable: true
phase*	{
value	string
value_guid	string
}
unit*	[...]
unit_guid*	string
nullable: true
unit_html	string
nullable: true
}
pe-re-dis-ev	oekobilanz_guid_prop{
property_guid*	string
nullable: true
value*	number($double)
nullable: true
phase*	{
value	string
value_guid	string
}
unit*	string
nullable: true
unit_guid*	string
nullable: true
unit_html	string
nullable: true
}
pe-nr	oekobilanz_guid_prop{
property_guid*	string
nullable: true
value*	number($double)
nullable: true
phase*	{
value	string
value_guid	string
}
unit*	string
nullable: true
unit_guid*	string
nullable: true
unit_html	string
nullable: true
}
pe-nr-sg	oekobilanz_guid_prop{
property_guid*	string
nullable: true
value*	number($double)
nullable: true
phase*	{
value	string
value_guid	string
}
unit*	string
nullable: true
unit_guid*	string
nullable: true
unit_html	string
nullable: true
}
pe-nr-ev	oekobilanz_guid_prop{
property_guid*	string
nullable: true
value*	number($double)
nullable: true
phase*	{
value	string
value_guid	string
}
unit*	string
nullable: true
unit_guid*	string
nullable: true
unit_html	string
nullable: true
}
pe-nr-pro	oekobilanz_guid_prop{
property_guid*	string
nullable: true
value*	number($double)
nullable: true
phase*	{
value	string
value_guid	string
}
unit*	string
nullable: true
unit_guid*	string
nullable: true
unit_html	string
nullable: true
}
pe-nr-pro-sg	oekobilanz_guid_prop{
property_guid*	string
nullable: true
value*	number($double)
nullable: true
phase*	{
value	string
value_guid	string
}
unit*	string
nullable: true
unit_guid*	string
nullable: true
unit_html	string
nullable: true
}
pe-nr-pro-ev	oekobilanz_guid_prop{
property_guid*	string
nullable: true
value*	number($double)
nullable: true
phase*	{
value	string
value_guid	string
}
unit*	string
nullable: true
unit_guid*	string
nullable: true
unit_html	string
nullable: true
}
pe-nr-dis	oekobilanz_guid_prop{
property_guid*	string
nullable: true
value*	number($double)
nullable: true
phase*	{
value	string
value_guid	string
}
unit*	string
nullable: true
unit_guid*	string
nullable: true
unit_html	string
nullable: true
}
pe-nr-dis-sg	oekobilanz_guid_prop{
property_guid*	string
nullable: true
value*	number($double)
nullable: true
phase*	{
value	string
value_guid	string
}
unit*	string
nullable: true
unit_guid*	string
nullable: true
unit_html	string
nullable: true
}
pe-nr-dis-ev	oekobilanz_guid_prop{
property_guid*	string
nullable: true
value*	number($double)
nullable: true
phase*	{
value	string
value_guid	string
}
unit*	string
nullable: true
unit_guid*	string
nullable: true
unit_html	string
nullable: true
}
gwp	oekobilanz_guid_prop{
property_guid*	string
nullable: true
value*	number($double)
nullable: true
phase*	{
value	string
value_guid	string
}
unit*	string
nullable: true
unit_guid*	string
nullable: true
unit_html	string
nullable: true
}
gwp-pro	oekobilanz_guid_prop{
property_guid*	string
nullable: true
value*	number($double)
nullable: true
phase*	{
value	string
value_guid	string
}
unit*	string
nullable: true
unit_guid*	string
nullable: true
unit_html	string
nullable: true
}
gwp-dis	oekobilanz_guid_prop{
property_guid*	string
nullable: true
value*	number($double)
nullable: true
phase*	{
value	string
value_guid	string
}
unit*	string
nullable: true
unit_guid*	string
nullable: true
unit_html	string
nullable: true
}
co2	oekobilanz_guid_prop{
property_guid*	string
nullable: true
value*	number($double)
nullable: true
phase*	{
value	string
value_guid	string
}
unit*	string
nullable: true
unit_guid*	string
nullable: true
unit_html	string
nullable: true
}
co2-pro	oekobilanz_guid_prop{
property_guid*	string
nullable: true
value*	number($double)
nullable: true
phase*	{
value	string
value_guid	string
}
unit*	string
nullable: true
unit_guid*	string
nullable: true
unit_html	string
nullable: true
}
co2-dis	oekobilanz_guid_prop{
property_guid*	string
nullable: true
value*	number($double)
nullable: true
phase*	{
value	string
value_guid	string
}
unit*	string
nullable: true
unit_guid*	string
nullable: true
unit_html	string
nullable: true
}
bio-e	oekobilanz_guid_prop{
property_guid*	string
nullable: true
value*	number($double)
nullable: true
phase*	{
value	string
value_guid	string
}
unit*	string
nullable: true
unit_guid*	string
nullable: true
unit_html	string
nullable: true
}
bio-co2	oekobilanz_guid_prop{
property_guid*	string
nullable: true
value*	number($double)
nullable: true
phase*	{
value	string
value_guid	string
}
unit*	string
nullable: true
unit_guid*	string
nullable: true
unit_html	string
nullable: true
}
bio-c	oekobilanz_guid_prop{
property_guid*	string
nullable: true
value*	number($double)
nullable: true
phase*	{
value	string
value_guid	string
}
unit*	string
nullable: true
unit_guid*	string
nullable: true
unit_html	string
nullable: true
}
}
quellekonstruktion	{
year	number
quelle	string
}
uwert	number($double)
wandbekleidung	translated_prop{
name	string
workingtitle	string
}
}
filter_key_label_pair{
label	string
values	[{
key	string
label	string
}]
}
filter_key_label_value_pair{
label	string
values	[{
key	string
value	string
label	string
}]
}
filter_min_max_value{
min	number($double)
max	number($double)
}
filter_min_max_object{
label	string
values	filter_min_max_value{
min	number($double)
max	number($double)
}
}
sia_product{
id	number
sia_id	string
label	string
sia_material_group_id	number
hersteller	{
id	string
name	string
}
company	{
id	string
name	string
}
density_informative	string
density	string
density_min	number($double)
density_avg	number($double)
density_max	number($double)
mortar	string
thickness	string
thickness_min	number($double)
thickness_avg	number($double)
thickness_max	number($double)
length	string
length_min	number($double)
length_avg	number($double)
length_max	number($double)
height	string
height_min	number($double)
height_avg	number($double)
height_max	number($double)
thermal_conductivity	number($double)
thermal_conductivity_dry	number($double)
thermal_conductivity_design	number($double)
thermal_storage_capacity_watt_hours	number($double)
thermal_storage_capacity_joules	number($double)
water_vapour_diffusion_resistance_number_dry	number($double)
water_vapour_diffusion_resistance_number_moist	number($double)
en_iso_10456_2007_tab_3	boolean
en_iso_10456_2007_tab_4	boolean
sn_en_1745_2020_anh_a	boolean
sn_en_12524_tab_na_1	boolean
sia_279_2018_tab_1	boolean
building_material_properties	boolean
valid_until	string($date)
state_of_data	string($date)
}
kbob{
id	string
uid	string
kbobId	string
workingtitle	string
disposal	string
disposalKbobId	string
thickness	number($double)
density	number($double)
size	string
ref	string
ubp	number($double)
ubph	number($double)
ubpe	number($double)
ubpf	number($double)
ubpi	number($double)
pe	number($double)
peb	number($double)
pef	number($double)
pei	number($double)
peh	number($double)
peev	number($double)
pesg	number($double)
pee	number($double)
peeb	number($double)
peef	number($double)
peei	number($double)
peer	number($double)
peeras	number($double)
peerh	number($double)
peerheg	number($double)
peerhsg	number($double)
peere	number($double)
pene	number($double)
peneb	number($double)
penef	number($double)
penei	number($double)
peneh	number($double)
penehev	number($double)
penehsg	number($double)
penee	number($double)
thg	number($double)
thgh	number($double)
thge	number($double)
thgb	number($double)
thgf	number($double)
thgi	number($double)
bioc	number($double)
}