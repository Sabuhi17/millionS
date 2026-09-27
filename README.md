# Milyonçu: Sosial siyasət

«Kim milyonçu olmaq istəyir?» formatında bilik yarışı. Suallar **Mövzu 1. Sosial siyasətin elmi-nəzəri və metodoloji əsasları** slaydlarına əsaslanır.

Tək fayldan (`index.html`) ibarətdir. Quraşdırma, framework və server tələb etmir.

## Qaydalar

- 15 sual, çətinlik getdikcə artır (100 ₼-dən 1 000 000 ₼-ə qədər).
- Hər suala **15 saniyə** vaxt verilir.
- 3 yardım (hər biri bir dəfə): **50:50**, **dosta zəng**, **auditoriya**. Yardım açıq olduqda taymer dayanır.
- Sığortalı məbləğlər: 5-ci sualdan sonra **1 000 ₼**, 10-cu sualdan sonra **32 000 ₼**.
- İstənilən vaxt «Pulu götür» düyməsi ilə oyunu bitirmək olar.
- Klaviatura: `A` `B` `C` `D` və ya `1` `2` `3` `4`.

## Sual bazası

- Ümumilikdə **60 sual**: 15 səviyyə × 4 sual.
- Hər oyunda hər səviyyədən 1 sual təsadüfi seçilir. Cavab variantlarının yeri də hər dəfə qarışdırılır.
- Görülən suallar brauzerin `localStorage` yaddaşında saxlanılır və **təkrar olunmur**. 4 oyundan sonra dövr yenidən başlayır.
- Ana səhifədəki «Sual bazasını sıfırla» düyməsi bu yaddaşı təmizləyir.
- Sual səhv cavablandıqda və ya vaxt bitdikdə nəticə ekranında düzgün cavab və slayd nömrəsi göstərilir.

## Sualları dəyişmək

`index.html` faylında `SUAL BAZASI` şərhindən sonrakı `BANK` massivini redaktə edin:

```js
Q("Sual mətni?", "Düzgün cavab", ["Səhv 1", "Səhv 2", "Səhv 3"], slaydNömrəsi)
```

Massivdə 15 qrup var və hər qrup bir sual səviyyəsinə uyğundur (1-ci qrup 100 ₼, 15-ci qrup 1 000 000 ₼). Hər qrupda ən azı 4 sual saxlamaq məsləhətdir.

## GitHub Pages ilə yayımlamaq

1. Yeni repozitoriya yaradın və `index.html` ilə `README.md` fayllarını yükləyin.
2. **Settings → Pages → Build and deployment** bölməsində **Deploy from a branch** seçin.
3. Branch olaraq `main`, qovluq olaraq `/ (root)` seçib **Save** düyməsini basın.
4. Bir neçə dəqiqədən sonra oyun `https://<istifadəçi-adı>.github.io/<repozitoriya-adı>/` ünvanında açılacaq.

Lokal işə salmaq üçün `index.html` faylını brauzerdə açmaq kifayətdir.

## Texniki qeydlər

- Şrift: Google Fonts (Montserrat). İnternet olmasa sistem şrifti istifadə olunur.
- Səs effektləri WebAudio ilə yaradılır, audio fayl yoxdur. Səsi oyun ekranındakı düymə ilə söndürmək olar.
- Mobil və masaüstü qurğularda işləyir. Mobildə pul pilləkəni «Pillələr» düyməsi ilə açılır.
