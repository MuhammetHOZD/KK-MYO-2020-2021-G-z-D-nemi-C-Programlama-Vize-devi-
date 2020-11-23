#include<stdio.h>
#include<time.h>
#define TUR (3)

int i=0 ;
int main( void )
{
	int ög_no;
  basa_dön:
	printf("\nÖĞRENCİ NUMARASINI GİRİNİZ> ");
	scanf("%d",&ög_no);
	if( ög_no == 200706014 )
		printf("\n********** ÖĞRENCİ BİLGİLERİ **********\n\n"
    "AD: MUHAMMET HÜSEYİN\n"
    "SOYADI: ÖZDEMİR\n"
    "OKUL NO : 200706014\n"
    "OKULU: KKÜ\n"
    "BÖLÜMÜ: ELEKTRONİK TEKNOLOJİSİ\n"
    "YAŞADIGI ŞEHİR: ANKARA\n"
    "YAŞI: 19\n"
    "DOĞGUM TARİHİ: 30/07/2001\n");
	else {
		if( ög_no <= 200706013 )
			printf("ÖĞRENCİ NUMARASI YANLIŞ\n"
      "TEKRAR DENEYİNİZ\n");
    else{
      if(ög_no >= 200706015)
			printf("ÖĞRENCİ NUMARASI YANLIŞ\n"
      "TEKRAR DENEYİNİZ\n");
      goto basa_dön;
    }
    goto basa_dön;
	}

int dogum_tarihi,yas;
printf("\n\n********** YAŞ HESAPLAMA **********\n"
"\nDOĞUM YILINIZI GİRİNİZ> ");
scanf("%d",&dogum_tarihi);
yas= 2020-dogum_tarihi ;
printf("YAŞINIZ (%d) \nBEREKETLİ ÖMÜRLER DİLERİZ",yas);

 time_t t;
  struct tm *ptm;

  time (&t);

  ptm = gmtime(&t);

  printf("\n\nŞu anki saat  "
"%02d:%02d\n", ptm->tm_hour + TUR, ptm->tm_min);


if(ptm->tm_hour + TUR >= 05 && ptm->tm_hour + TUR <10)
 printf("HAYIRLI SABAHLAR\n");
else{
  if(ptm->tm_hour + TUR >=10 && ptm->tm_hour + TUR <17)
  printf("HAYIRLI GÜNLER\n");
  else{
    if(ptm->tm_hour + TUR >=17 && ptm->tm_hour + TUR <22)
    printf("HAYIRLI AKŞAMLAR\n");
    else{
      if(ptm->tm_hour + TUR >=22 && ptm->tm_hour + TUR <24)
      printf("HAYIRLI GECELER\n");
      else{
        if(ptm->tm_hour + TUR >= 00 && ptm->tm_hour + TUR <05)
 printf("HAYIRLI GECELER\n");
      }
    }
  }
}

int devam_tusu ;
tekrar_dene:
printf ("\nDevam Etmek İçin\n" 
" 1 Tuşuna basıp ENTER tuşuna basınız> ");
scanf("%d",&devam_tusu);
if (devam_tusu == 1)
printf("\nİŞLEM BAŞLATILIYOR");
 else {
  if(devam_tusu != 1)
  printf("TEKRAR DENEYİNİZ");
  goto tekrar_dene;
}

for(;i<100;){
  printf("\nİŞLEM TAMAMLANIYOR %%%2d",(i+1));
  i = i+1 ;
}
printf("\nİŞLEM TAMAMLANDI\n");

int devam_tusu2 ;
tekrar_dene2:
printf ("\nDevam Etmek İçin\n" 
" 1 Tuşuna basıp ENTER tuşuna basınız> ");
scanf("%d",&devam_tusu2);
if (devam_tusu2 == 1)
printf("\nİŞLEM BAŞLATILIYOR");
 else {
  if(devam_tusu2 != 1)
  printf("TEKRAR DENEYİNİZ");
  goto tekrar_dene2;
}

while(i<2020){
  i =i+2;
  printf("%d ", i);
  if(i == 2020)
  break;
}
printf("\n\n\n------------------------- MUHAMMET HÜSYEYİN ÖZDEMİR ------------------------"
" \n\n---------------------- C PROGRAMLAMA DERSİ VİZE ÖDEVİ ----------------------");
	return 0;
}
