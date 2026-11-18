# 24BAG0CR2 – MVP 1.0 starter

## Hali ya mradi
Huu ni mwanzo wa majaribio wa Android Wi‑Fi Direct. Unaonyesha discovery ya vifaa, kuomba kuunganishwa na peer wa kwanza, na TCP server ya msingi kwa Group Owner.

**Si mesh ya multi-hop bado.** Wi‑Fi Direct group ni muunganisho wa kikundi kimoja; idadi ya clients inategemea simu, Android version na mtengenezaji. Lengo la 10–50 linahitaji majaribio na baadaye routing/relay architecture au Wi‑Fi routers/nodes maalumu.

## Mahitaji
- Android Studio (toleo la karibuni la stable)
- JDK 17
- SDK Platform 35
- Angalau simu mbili za Android zenye Wi‑Fi Direct
- Wi‑Fi iwashwe kwenye simu zote

## Kufungua
1. Fungua Android Studio.
2. Chagua **Open** na uchague folder `24BAG0CR2_MVP1`.
3. Subiri Gradle Sync ikamilike.
4. Unganisha simu mbili kwa USB, wezesha Developer options na USB debugging.
5. Run app kwenye simu zote mbili.
6. Ruhusu Nearby Wi‑Fi Devices (Android 13+) au Location permission (Android 12 na chini).
7. Kwenye simu zote, bonyeza **TAFUTA SIMU ZA KARIBU**.
8. Kwenye simu moja bonyeza **OMBA KUUNGANISHWA NA SIMU YA KWANZA** baada ya kuona kifaa kingine.

## Tahadhari za MVP
- App hii ni prototype ya majaribio; si programu iliyokaguliwa kiusalama.
- TCP demo hii bado ni ya msingi na inahitaji kuboreshwa ili peer/client aweze kutuma ujumbe kwa Group Owner kwa uhakika, kisha server isambaze kwa wanachama wote.
- Uhamishaji wa picha/mafaili, encryption, message IDs, delivery acknowledgements, offline queue, multi-hop forwarding na UI ya orodha ya wanachama bado hazijajengwa.
- Usitumie kutuma taarifa nyeti au za siri.
- Android 13+ permission policy na tabia ya Wi‑Fi Direct hutofautiana kwa kifaa; baadhi ya simu zinahitaji Location Services kuwashwa kwa discovery.

## Mpango wa hatua zinazofuata
1. Imarisha lifecycle na permission handling.
2. Tengeneza protocol ya ujumbe yenye IDs na encryption.
3. Broadcast ujumbe kwa wanachama wote.
4. Ongeza file transfer kwa chunks na checksum.
5. Jenga relay/routing ya multi-hop kwa vifaa vinavyoweza kushiriki kama nodes.
6. Pima kwa simu nyingi halisi; usiahidi 50 hadi vipimo vithibitishe.

## Kujenga APK kwa kutumia simu pekee (GitHub Actions)
1. Tengeneza akaunti ya GitHub kwenye github.com ikiwa huna.
2. Fungua GitHub kwenye browser ya simu na tengeneza repository mpya, mfano `24BAG0CR2`.
3. Pakua na unzip project hii kwenye simu. Tumia file manager kutoa ZIP.
4. Pakia mafaili yote ya ndani ya folder kwenye repository, ukihakikisha `.github/workflows/build-apk.yml` nayo ipo.
5. Fungua kichupo cha Actions kwenye repository. Chagua `Build 24BAG0CR2 APK`, kisha `Run workflow`.
6. Ikimaliza kwa alama ya kijani, fungua run husika, nenda sehemu ya Artifacts na pakua `24BAG0CR2-debug-apk`.
7. Fungua APK kwenye simu na ruhusu install kutoka browser/files ikiwa Android itauliza.

GitHub Actions hujenga APK kwenye kompyuta ya cloud; simu yako inatumika kuandaa project, kuendesha build na kupakua APK. Usichapishe passwords, signing keys au taarifa za siri kwenye repository.

Kumbuka: hii bado ni prototype Wi-Fi Direct, si multi-hop mesh kamili. Pima kwanza kwa simu mbili.
