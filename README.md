:::writing{variant=“standard” id=“38157”}

zmk-config-zyraft

PL

Konfiguracja ZMK dla Zyra FT (Sweep/Cradio) - minimalistyczna klawiatura ergonomiczna FalbaTech.

Hardware
	•	Shield: cradio (oficjalny w upstream ZMK)
	•	Kontrolery: 2× nice!nano v2
	•	Bez wyświetlacza (pin D1/P0.06 zajęty przez switch matrix)
	•	34 klawisze (3 rzędy × 5 kolumn + 2 thumb na stronę)
	•	Home-row mods aktywne (Shift/Alt/Ctrl/Gui)

Warstwy

#	Nazwa	Funkcja
0	default_layer	QWERTY base + home-row mods
1	right_layer	Cyfry, nawigacja (aktywuje prawy thumb)
2	left_layer	Symbole, brackets (aktywuje lewy thumb)
3	tri_layer	System, BT controls (oba thumby naraz)

Home-row mods

Lewa ręka:
	•	A = Shift
	•	S = Alt
	•	D = Ctrl
	•	F = Gui

Prawa ręka:
	•	J = Gui
	•	K = Ctrl
	•	L = Alt
	•	' = Shift

Tapping-term 220ms, quick-tap 150ms, require-prior-idle 100ms.

ZMK Studio

Aktywne. Procedura odblokowania (jednakowa we wszystkich klawiaturach FalbaTech FT):

Trzymaj oba thumby aktywujące warstwy systemowe (TAB + BSPC) → wciśnij skrajny lewy górny klawisz.

Po odblokowaniu klawiatura jest edytowalna z:
zmk.studio￼

Bluetooth - obsługa 5 urządzeń

Klawiatura obsługuje 5 niezależnych profili Bluetooth. W warstwie systemowej (tri_layer):

Klawisz	Funkcja
Z	Profil BT 0
X	Profil BT 1
C	Profil BT 2
V	Profil BT 3
B	Profil BT 4
N	Wyczyść aktywny profil
M	Wyczyść wszystkie profile
,	Tryb USB
.	Tryb Bluetooth

Aktywacja warstwy systemowej: trzymaj jednocześnie lewy thumb (TAB) i prawy thumb (BSPC). Warstwa Tri włącza się automatycznie jako conditional layer.

Build

GitHub Actions buduje 3 firmware:
	•	cradio_left-nice_nano-zmk.uf2
	•	cradio_right-nice_nano-zmk.uf2
	•	settings_reset-nice_nano-zmk.uf2

Flashowanie
	1.	Lewa USB - 2× reset - cradio_left-...uf2
	2.	Prawa USB - 2× reset - cradio_right-...uf2
	3.	Połącz TRRS - klawiatura “Zyra FT” w BT

Wsparcie

FalbaTech - https://falbatech.click

⸻

EN

ZMK configuration for Zyra FT (Sweep/Cradio) - minimalist ergonomic FalbaTech keyboard.

Hardware
	•	Shield: cradio (official upstream ZMK shield)
	•	Controllers: 2× nice!nano v2
	•	No display (pin D1/P0.06 used by switch matrix)
	•	34 keys (3 rows × 5 columns + 2 thumb keys per side)
	•	Home-row mods enabled (Shift/Alt/Ctrl/Gui)

Layers

#	Name	Function
0	default_layer	QWERTY base + home-row mods
1	right_layer	Numbers, navigation (activated by right thumb)
2	left_layer	Symbols, brackets (activated by left thumb)
3	tri_layer	System, BT controls (both thumbs together)

Home-row mods

Left hand:
	•	A = Shift
	•	S = Alt
	•	D = Ctrl
	•	F = Gui

Right hand:
	•	J = Gui
	•	K = Ctrl
	•	L = Alt
	•	' = Shift

Tapping-term 220ms, quick-tap 150ms, require-prior-idle 100ms.

ZMK Studio

Enabled. Unlock procedure (same across all FalbaTech FT keyboards):

Hold both thumb keys activating system layers (TAB + BSPC) → press the top left key.

After unlocking, the keyboard can be configured from:
zmk.studio￼

Bluetooth - 5 device support

The keyboard supports 5 independent Bluetooth profiles. In the system layer (tri_layer):

Key	Function
Z	BT Profile 0
X	BT Profile 1
C	BT Profile 2
V	BT Profile 3
B	BT Profile 4
N	Clear active profile
M	Clear all profiles
,	USB mode
.	Bluetooth mode

System layer activation: hold the left thumb (TAB) and right thumb (BSPC) together. The Tri layer activates automatically as a conditional layer.

Build

GitHub Actions builds 3 firmware files:
	•	cradio_left-nice_nano-zmk.uf2
	•	cradio_right-nice_nano-zmk.uf2
	•	settings_reset-nice_nano-zmk.uf2

Flashing
	1.	Left USB - press reset 2× - cradio_left-...uf2
	2.	Right USB - press reset 2× - cradio_right-...uf2
	3.	Connect TRRS - keyboard appears as “Zyra FT” over Bluetooth

Support

FalbaTech - https://falbatech.click
:::
