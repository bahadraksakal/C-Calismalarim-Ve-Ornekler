#include <stdio.h>
#include <stdlib.h>
#include <string.h>
// sarki sozleri ters cevrilmis hexa codelerden olusmutur.
int main()
{
     char sarki_sozleri[201]="4757f6261602b6e69686470256271646029402e6168647025627f6d60237479602c297f624a0461656860297d60266f602";
     char sarki_sozleri_duzeldi[strlen(sarki_sozleri)+1];
     char hexacodeler[95][3];

    for(int i=0;i<95;i++)
    {
        sprintf(hexacodeler[i],"%x%c",i+32,'\0');
        //printf("%s\n",hexacodeler[i]);
    }

    for(int i=0;i<strlen(sarki_sozleri);i++)
    {
        sarki_sozleri_duzeldi[i]=sarki_sozleri[strlen(sarki_sozleri)-1-i];
        //printf("%c",sarki_sozleri_duzeldi[i]);
    }
    sarki_sozleri_duzeldi[strlen(sarki_sozleri)]='\0';

    puts(sarki_sozleri_duzeldi);
    printf("orj %d\n",strlen(sarki_sozleri));
    printf("duzeldi %d\n",strlen(sarki_sozleri_duzeldi));

    int i,j;

    for(i=0;i<strlen(sarki_sozleri_duzeldi);i++)// sonuclar hep tam sayi cikicak.
    {
        for(j=0;j<95;j++)
        {
            if(sarki_sozleri_duzeldi[i]==hexacodeler[j][0] && sarki_sozleri_duzeldi[i+1]==hexacodeler[j][1])
            {
                printf("%c",j+32);
                i+=1;
            }
        }
    }

    return 0;
}
