# donemsonuu.c
dönem sonu projesi

#include<stdio.h> //Giriş ve çıkış işlemlerini yerine getiren fonskiyonları barındıran kütüphanedir.
#include<ctype.h> /*(char+type=ctype) bir karakterin tipini algılar ve değiştirir.Dizgiler(string) üzerinde yapılan işlemlerde
avantaj sağlar */ 
#include<stdlib.h> /*Standart library header anlamına gelir. Dinamik bellek yönetimi,tamsayı aritmetiği,arama,sıralama,dönüştürme gibi genel amaçlı fonksiyonları tanımlayan kütüphane. */
#include<string.h> /*Karakter dizgileri ile ilgili fonksiyon, veri türü ve makro tanımlamaları içerir. C dilinde karakter dizileri üzerinde operatörler ile işlem yapılamadığı için bu tarz fonksiyonlar içeren kütüphaneler kullanılır. */
#include <conio.h> /* Çoğunlukla MS-DOS derleyicileri tarafından konsol girdi/çıktı işlemleri için sunulan bir başlık dosyasıdır. */
int anamenu();
int main()
     {
     int r,r1,onsay,i,n,a1,a2,a3,a4,a5,a6,a7,a8;
     int sayac =0;
     


	
	anamenu();
    
     system("CLS");
     
    printf("\n -------------------------  How I Met Your Mother Karakter quizine hosgeldiniz. --------------------------");
    printf("\n\n Cozmeye baslamadan once bilmenizde fayda olan birkac bilgi:");
    printf("\n - Quizimizde sizi daha iyi tanimaya yonelik sorularimiz var ve verdiginiz cevaplarla en cok hangi karaktere benzediginizi ortaya koyacagiz.");
    printf("\n    Toplamda 3 adet on sorumuz var. Bu sorulari quizimizi cozebilecek kadar diziye hakim olup olmadiginizi anlamak icin kullanacagiz. ");
    printf("\n On asamayi tamamladiktan sonra 8 tane asil sorumuz gelecek, size en yakin gelen secenekleri tuslamaniz beklenecektir.");
    printf("\n\n\t Iyi eglenceler!");
    printf("\n\n\n Ilk on soruya gecmek icin B'yi tuslayin.\n");
    printf("\n Ana menuye donmek icin herhangi baska bir tusa tiklayin.");
    if (toupper(getch())=='B')
		{
		    goto baslangic;
        }
	else
		{
        anamenu(); 
       }

     baslangic:
     system("CLS");
     onsay=0;
     for(i=1;i<=3;i++)
     {
    system("CLS");
    


     switch(i)
		{case 1:
		printf("\n\nHangisi bir ana karakter degildir?");
		printf("\n\nA.Ted\t\tB.Barney\n\nC.Robin\t\tD.Mahmut");
		
		if (toupper(getch())=='D')
			{
			    printf("\n\nTebrikler, dogru bildiniz!");
          printf("\n Ilerlemek icin bosluk tusuna basiniz.");
                onsay++;
			    getch();
			    break;
            }
		else
		       {
		           printf("\n\nYanlis! Dogru cevap: D.Mahmut");
               printf("\n Ilerlemek icin bosluk tusuna basiniz.");
		           getch();
		       break;
		       }

        case 2:
		printf("\n\n\n Dunyanin her yerinde sevilerek izlenen dizi kac sezondan olusmaktadir?");
		printf("\n\nA.9 sezon\t\tB.7 sezon\n\nC.13 sezon\t\tD.8 sezon");
		if (toupper(getch())=='A')
			{printf("\n\nTebrikler, dogru bildiniz!");
       printf("\n Ilerlemek icin bosluk tusuna basiniz.");
            onsay++;
			getch();
			break;}
		else
		       {printf("\n\nYanlis! Dogru cevap: A.9 sezon");
            printf("\n Ilerlemek icin bosluk tusuna basiniz.");
		       getch();
		       break;}

        case 3:
		printf("\n\n\n Ted'in Tracy icin actigi semsiye hangi renktir?");
		printf("\n\nA.Kirmizi\t\tB.Sari\n\nC.Mavi\t\tD.Yesil");
		if (toupper(getch())=='B')
			{printf("\n\nTebrikler, dogru bildiniz!");
       printf("\n Ilerlemek icin bosluk tusuna basiniz.");
            onsay++;
			getch();
			break;}
		else
		       {
                printf("\n\nYanlis! Dogru cevap: B.Sari");
                printf("\n Ilerlemek icin bosluk tusuna basiniz.");
		       getch();
		       break;
               }
}
}
		

	if(onsay >=1)
	{goto test;}
	else
	{
	system("CLS");
	printf("\n\n Bu quizi cozmek icin diziyi yeterince izlememissiniz. :( ");
	getch();
	anamenu();
	}
     test:
     system("CLS");
     printf("\n\n\tTebrikler, quizi cozmek icin on asamayi gectiniz");
     printf("\n\n\n\n\t!Baslamak icin herhangi bir tusa basiniz!");
       
     if(toupper(getch())=='p')
		{goto game;}
  game:
     
     for(i=1;i<=8;i++)
     {
      system("CLS");
      r=i;
     
     switch(r)
		{
	   soru1:
     case 1:
		printf("\n\nRuh esinde aradigin ilk ozellik nedir?");
		printf("\n\nA.Ortak hobilere sahip olmali\t\tB.Espri kabiliyeti olmali\n\nC.Duzgun bir karaktere sahip olmalı\t\tD.Yuva kurmaya karar vermis biri olmali\n\nE.Sempatik ve cekici olmali ");
		a1=toupper(getch());
		if (a1== 'A' ){
         sayac+=0;
		 break;}
		if (a1=='B'){
		   sayac+=50; 
		       
		       break;}
        if(a1=='C'){
        sayac+=100;
               break; } 
        if(a1=='D') {
       sayac+=150;
        break;}
        if(a1=='E'){
        sayac+=200;
             break; }
      else{
              system("CLS");
             	printf("HATALI TUSLAMA\n");
        
             	goto soru1;
			 }
       

        soru2:
        case 2:
		printf("\n\n\nHangisini tercih edersin?");
		printf("\n\nA.Solucan dolu bir kase yiyip piyangoyu kazanmak \t\tB.Orumcek tarafindan isirilip super kahraman olmak\n\n C.Ruyalarini kontrol edebilecek evcil bir hayvana sahip olmak \t\tD.Her hafta bir tane altin yumurtlayan bir tavukla uyumak");
        //sonuca etkisi yok.
          
     a2=toupper(getch());
		if (a2== 'A' ){
         sayac+=0;
		 
		 break;}
	 if (a2=='B'){
		   sayac+=0;
		       break;}
      if(a2=='C'){
        sayac+=0;
               break;  }
     if(a2=='D'){
        sayac+=0;
        break;}
          else {
            system("CLS");
        	printf("HATALI TUSLAMA\n");
            
        	goto soru2;
		}
       
        soru3:
        case 3:
		printf("\n\n\nHangisi hayat amacina daha yakin?");
		printf("\n\nA.Unlu bir sanatci olmak\t\tB.Guiness Dunya rekortmeni olmak \n\nC.Olimpiyat madalyali bir sporcu olmak\t\tD.Basarili bir is insani olmak \n\nE.Unlu bir aktor/aktris olmak");
		a3=toupper(getch());
		if (a3== 'A' ){
         sayac+=0;
		 
		 break;}
		 if (a3=='B'){
		   sayac+=50; 
		       
		       break;}
        if(a3=='C'){
        sayac+=100;
              
               break;}  
        if(a3=='D') {
        sayac+=150;
        break;}
        if(a3=='E'){
        sayac+=200;
             
             break;}
         else
         {
           system("CLS");
             	printf("HATALI TUSLAMA\n");
           
             	goto soru3;
			 }
        

        soru4:
        case 4:
		printf("\n\n\nEvlilige bakis acin ne?");
		printf("\n\nA.Dogru kisiyi buldugunda harika bir sey\t\tB.Iliskinin amaci evlilik degil mi?\n\nC.Hayalini kurmasam da ansizin evlenebilirim\t\tD.Iki insan birbirini seviyorsa gerisi onemsiz\n\n E.Asla yapmayacagim bir sey");
		a4=toupper(getch());
		if (a4== 'A' ){
     sayac+=0;
		 
		 break;}		  
    if (a4=='B'){
		  sayac+=50; 
		       
		    break;}
        if(a4=='C'){
        sayac+=100;
              
       break;}
              
     if(a4=='D'){
         sayac+=150;
        
       break;}
    
     if(a4=='E'){
      sayac+=200;
             
            break;}
      else{
        system("CLS");
            	printf("HATALI TUSLAMA\n");
        
            	goto soru4;
			}

        soru5:
        case 5:
        printf("\n\n\nArkadaslarin seni nasil tanimlar?");
        printf("\n\nA.Caliskan ve basarili\t\tB.Sevecen/sevimli \n\nC.Idealist\t\tD.Karizmatik  \n\nE.Serseri");
          a5=toupper(getch());
        if (a5== 'A' ){
         sayac+=0;
		 
		 break;}
		if (a5=='B'){
		   sayac+=50; 
		       
		       break;}
         if(a5=='C'){
        sayac+=100;
              
               break;}  
        if(a5=='D') {
        sayac+=150;
        
        break;}
       if(a5=='E'){
        sayac+=200;
             
             break; } 
      else{
        system("CLS");
        printf("HATALI TUSLAMA\n");
        
        goto soru5;
      }
        
        
        soru6:
        case 6:
        printf("\n\n\nIki secenekten birini sec!");
        printf("\n\nA.Asik oldugun insan disinda herkesin seni sevmesi\n\nB.Asik oldugun insan disinda herkesin senden nefret etmesi");
        //sonuca etkisi yok.
          a6=toupper(getch());
      if (a6== 'A' ){
         sayac+=0;
		 break;}
		 if (a6=='B'){
		   sayac+=0;
		       break;}
        if(a6=='C'){
        sayac+=0;
               break;  }
         if(a6=='D') {
       sayac+=0;
        break;}
        if(a6=='E'){
        sayac+=0;
             break; } 
      else{
        system("CLS");
        printf("HATALI TUSLAMA\n");
        
        goto soru6;
      }
        
         soru7:
      case 7:
        printf("\n\n\nDis gorunus senin icin ne ifade ediyor?");
        printf("\n\nA.Dis gorunusten onemli seyler de var\t\tB.Insanin ici guzelse disi da guzel olur \n\nC.Ilk izlenim acisindan kesinlikle cok onemli\t\tD.Onemlidir ama her sey de degil \n\nE.Onemli degil diyen yalan soyluyordur");
           a7=toupper(getch());
        if (a7== 'A' ){
         sayac+=0;
		 break;}
		  if (a7=='B'){
		   sayac+=50; 
		       break;}
         if(a7=='C'){
        sayac+=100;
               break; } 
        if(a7=='D') {
        sayac+=150;
        
        break;}
        if(a7=='E'){
        sayac+=200;
             break;  }
      else{
        system("CLS");
        printf("HATALI TUSLAMA\n");
       
        goto soru7;
      }
       

        soru8:
        case 8:
		printf("\n\n\nBir ozelligini degistirme sansin olsa hangisi olurdu?");
		printf("\n\nA.Basarisiz olma korkusu\t\tB.Cekingenlik\n\nC.Guven problemi\t\tD.Ozguven eksikligi\n\nE.Kararsizlik");
          a8=toupper(getch());
		if (a8== 'A' );{
         sayac+=0;
		 break;}
		 if (a8=='B'){
		   sayac+=50; 
		       
		       break;}
         if(a8=='C'){
        sayac+=100;
              
               break;}  
         if(a8=='D'){
        sayac+=150;
        break;}
         if(a8=='E'){
        sayac +=200;
          
             break;  }
      else {
        system("CLS");
        printf("HATALI TUSLAMA!\n");
        
        goto soru8;
      }
        
               }
		       }
		       
		   
	


    system("CLS");
	
	if ( sayac < 240)
	{ printf("\n\t\t\t\t\tLILY:\n\n");
		printf("Sen tanimlayan ilk kelime klas: Sanatcisin, zarifsin. Seni yururken gorenler, 'bu kesinlikle yurumuyor; suzuluyor' der. Bu, zerafetinden olsa gerek. Ama bu zerafet de asla donuk ve soğuk değil. Espriden de anlıyorsun! Tam asik olunacak ve omur adanacak kadın/adamsın..");
		
		goto git;
	}
	 else if(sayac>=240 & sayac < 480){ 
     printf("\n\t\t\t\t\tMARSHALL:\n\n");
		printf("Hani hep 'yalan soyleyen ve kotu davranan, sevilir' diye yaygin bir gorus vardir ya. Iste sen bu soze adeta tokat gibi bir cevapsin. Yalani sevmiyorsun ve hep dogruyu yapmaya calisiyorsun. Ayrica cocuk gibisin: Hayalci, oyuncu ve masum. Aman zaten buyuyunce ne oluyor ki...");
     
   
      goto git;
	}
	 else if(sayac>=480 & sayac < 720){
     printf("\n\t\t\t\t\tROBIN:\n\n");
		printf("Guzelsin hatta cok cok guzel. Ama seni, sadece guzel olarak tanimlamak haksizlik olur. Bir yerlere gelmek ya da bir seyler elde etmek icin bu guzelligini kullanmiyorsun. Hayatta her seyi kendi basina hallediyorsun, kendi basina varoldun zaten hep. Bu yuzden darlanmak ve birilerine baglanmak senin icin oldukca zor. Kendine guveninse tam.");
 

        goto git;
	}
	 else if (sayac>=720 & sayac < 960){
		printf("\n\t\t\t\t\tTED:\n\n");
    printf("Basrolsun sen basrol! Sirf bu yuzden de cogu kisi tarafindan sevilmiyorsun. Nefret eden etsin. Cunku seni sevenler; senin ne kadar kulturlu, altin kalpli ve de arkadas canlisi olduğunu biliyor. Tek bir kotu huyun var, oda insanlarin yazim ve telaffuz hatalarini duzeltmek. Mesela az once yaptığım baglac hatasina ayar olduysan, dogru yerdesin.");

        goto git;
	}
	 else if( sayac >= 960 & sayac <=1200){
		printf("\n\t\t\t\t\tBARNEY:\n\n");
    printf("Ooo!.. Kimmissin sen kim? Barney mi? Tebrikler, cunku senin hayatin tam bir 'legen... wait for it... dary'. Efsane yani. Efsane kelimesi de yaninda pek bir sonuk kaldi be! Bir kere cekicisin, istedigini elde edebilirsin: Bu, 1. Zenginsin: 2. E yakisikli/guzelsin de: Bu da 3... ");
        
        goto git;
        }
    git:
	puts("\n\nYeni oyuna gecmek icin Y tusuna basiniz");
	puts("Ana menuye geri donmek icin herhangi bir tusa basiniz");
	if (toupper(getch())=='Y')
		goto baslangic;
	else
   {
        anamenu();
       system("CLS"); 
       }

      
	return 0;	
}

int anamenu()
    {
    	
    FILE *fp, *fp2; 
    char ad[50];
    char secim;
       
    if ( (fp = fopen("dosya.txt","w"))==NULL) //w dosyayı yazma modunda açar.
    {
        printf("Dosya acilamadi");
        exit(1); ////Kaynakları tamamen temizleyerek programı normal bir şekilde sonlandırır.Ön tanımlanmış bir fonksiyondur.
    }

    printf("Test icin adinizi giriniz:");
    gets(ad);


    fprintf(fp,"%s\t",ad); //fprintf() yazması gereken bilgiyi ekrana değil, ilk parametresi fp dosya göstericisinin işaret ettiği dosyaya yazar.

    fclose(fp);  //dosyayı kapatır.



    if ( (fp2 = fopen("dosya.txt","r"))==NULL) //r dosyayı okuma modunda açar. NULL işlemin doğruluğunu kontrol eder.
    {
        printf("Dosya acilamadi");
        exit(1); //güvenli bir şekilde programı bitirir.
    }

    fscanf(fp2, "%s\t",ad); //fprintf ile alınan ad yazdırılır.

     system("CLS"); //CLS komutu ekranı temizler.
     printf("\t\t\t Hangi How I Met Your Mother Karakterisin? \n");
     printf("\n\t\t\t BASLA");
     printf("\n\t\t\t Merhaba %s",ad);
     printf("\n\t\t\t Quize baslamak icin S'ye");
     printf("\n\t\t\t Yeniden cozmek icin R'ye");
     printf("\n\t\t\t Quizden ayrilmak icin Q'ya basiniz. \n");
        secim=toupper(getch()); //büyük harf de küçük harf de girilebilir.
    if (secim=='R'){
	  system("clrscr");
	}
	 else if (secim=='Q')
	 exit(1); //Kaynakları tamamen temizleyerek programı normal bir şekilde sonlandırır.Ön tanımlanmış bir fonksiyondur.
    else if(secim=='S')
      system("CLS");
 }
