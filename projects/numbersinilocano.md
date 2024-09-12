---
layout: project
type: project
image: img/Ilocano.jpg
title: "Numbers In Ilocano"
date: 2024-06-07
published: true
labels:
  - C-Language
  - Ilocano
  - Translation
summary: "A program that will print the Ilocano translation of numbers from 1-9999."
---

Overview:


This program was created using C-Language in my ICS 212 class. We were able to choose what language we wanted to translate from and I decided to do Ilocano since this is my parent's native language. 


The main challenge with developing this program is that the resources I found online to translate higher numbers seemed to have different information. For example, for each values place(i.e. tenths, hundreds, thousands) some websites was showing that you mainly just add "ket" in between each values place translation, while some other resources only added it to the last conjunction of place values. 


In the future I would like to change this program so that it will ask the user for a number and will tanslate that specific number, rather than print all of the numbers out. In doing so, I would hope this will help me study Ilocano.


Example of code output after running:


Snippet of Code Used:

int main(void) {

    // Tells user what program does.
    printf("This program will count in Ilocano\n");

    // For loop will go through 1-9999 in increments of 1.
    for(int x = 1; x <= 9999; x++) {

        // Will tell me the digit in the thousands place.
        int thousands = x/1000;

        // Will tell me the digit in the hundreds place.
        int hundreds = x/100 % 10;

        // Will tell me the digit in the tens place.
        int tens = x/10 %10;

        // Will tell me the digit in the ones place.
        int ones = x%10;

        //Formats the first part of the output so you do not have to retype 1 =, 2=,...
        printf("%d = ", x);

        // If statement used to get word for thousands place. When thousands = 0, will skip to next if.
        if(thousands > 0) {

            // Swich prints out words for thousands place.
            switch(thousands){
                case 1:
                    printf("sangaribo ");
                    break;
                case 2:
                    printf("dua ");
                    break;
                case 3:
                    printf("tallo ");
                    break;
                case 4:
                    printf("uppat ");
                    break;
                case 5:
                    printf("lima ");
                    break;
                case 6:
                    printf("innem ");
                    break;
                case 7:
                    printf("pito ");
                    break;
                case 8:
                    printf("walo ");
                    break;
                case 9:
                    printf("siam ");
                    break;
                default:
                    break;
            }
            // In Ilocano 1000 = sangaribo, after its format is (thousands) a ribo.
            if(thousands != 1) {
                printf("a ribo ");
            }
            // Prints a ket if something follows the thousand which is used to connect the numbers.
            if(hundreds != 0 || tens != 0 || ones != 0) {
                printf("ket ");
            }
        }
        // If statement to determine hundred word in ilocano.
        if (hundreds > 0) {
            // Switch statement translate the hurdreds value.
            switch(hundreds) {
                case 1:
                    printf("sangagasut ");
                break;
                case 2:
                    printf("dua a gasut ");
                break;
                case 3:
                    printf("tallo a gasut ");
                break;
                case 4:
                    printf("uppat a gasut ");
                break;
                case 5:
                    printf("lima a gasut ");
                break;
                case 6:
                    printf("innem a gasut ");
                break;
                case 7:
                    printf("pito a gasut ");
                break;
                case 8:
                    printf("walo a gasut" );
                break;
                case 9:
                    printf("siam a gasut ");
                break;
                default:
                    break;
            }
            // Prints ket if there are numbers in the tens or ones.
            if(tens != 0 || ones != 0) {
                printf("ket ");
            }
        }
        // If statement to determine tens word in Ilocano.
        if (tens > 0) {
            // Switch statement prints out the Ilocano translation.
            switch(tens) {
                case 1:
                        printf("sangapulo");
                break;
                case 2:
                        printf("duapulo");
                break;
                case 3:
                        printf("tallopulo");
                break;
                case 4:
                        printf("uppat a pulo");
                break;
                case 5:
                        printf("lima pulo");
                    break;
                case 6:
                        printf("innem a pulo");
                    break;
                case 7:
                        printf("pito pulo");
                    break;
                case 8:
                        printf("wala pulo");
                    break;
                case 9:
                        printf("siam a pulo");
                    break;
                default:
                    break;
            }
