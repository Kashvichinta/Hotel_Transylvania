# Hotel_Transylvania
#include <stdio.h>
#include<stdlib.h>
    struct hotel {
        int room_no[20];
        char name_of_visitor[30];
        int days_of_stay;
        int pay;
        int due;
    }S[20];
int main() {
   int j=0;
   int i, room_type,paid,selected_room, booked[20];
   while(j<20){
       printf("\nWelcome to Hotel Transylvania, a hotel where monsters and humans live in harmony 0_0 \n Started by the vampire Count Dracula in the year 1765.\n We offer you multiple types of rooms as per your budget and spookiness ");
       printf("\n enter the respected number for the room you would like to survive in:\n1:frankestein's tower\t cost:$250\t spookiness: **\n2:the mummy's pyramid\t cost:$300\t spookiness: ***\n3:the werewolf's cave\t cost:$200\t spookiness: *\n4:the vampire's casket\t cost:$500\t spookiness: ****\n");
       scanf("%d",&room_type);
	   switch(room_type){
	   	case 1:printf("select only among the mentioned rooms or you will face the wrath of the lobby's tarantula:");
	   		   for(i=0;i<5;i++){
	   		   		if(booked[i]!=1)
						  printf("%5d",i);
				  }
				printf("\nchoose wisely:");
				scanf("%d",&selected_room);
				if(selected_room>=0 && selected_room<5 && booked[selected_room]!=1)
				printf("\ngood choice. you will enjoy your stay.");
				else{
				printf("how dare you. prepare to be attacked");
				exit(0);}	
				break;
		case 2:printf("select only among the mentioned rooms or you will face the wrath of the lobby's tarantula:");
	   		   for(i=5;i<10;i++){
	   		   		if(booked[i]!=1)
						  printf("%5d",i);
				  }
				printf("\nchoose wisely:");
				scanf("%d",&selected_room);
				if(selected_room>=5 && selected_room<10 && booked[selected_room]!=1)
				printf("\ngood choice. you will enjoy your stay.");
				else{
				printf("how dare you. prepare to be attacked");
				exit(0);}	
				break;
		case 3:printf("select only among the mentioned rooms or you will face the wrath of the lobby's tarantula:");
	   		   for(i=10;i<15;i++){
	   		   		if(booked[i]!=1)
						  printf("%5d",i);
				  }
				printf("\nchoose wisely:");
				scanf("%d",&selected_room);
				if(selected_room>=10 && selected_room<15 && booked[selected_room]!=1)
				printf("\ngood choice. you will enjoy your stay.");
				else{
				printf("how dare you. prepare to be attacked");	
				exit(0);}
				break;
		case 4:printf("select only among the mentioned rooms or you will face the wrath of the lobby's tarantula:");
	   		   for(i=15;i<20;i++){
	   		   		if(booked[i]!=1)
						  printf("%5d",i);
				  }
				printf("\nchoose wisely:");
				scanf("%d",&selected_room);
				if(selected_room>=15 && selected_room<20 && booked[selected_room]!=1)
				printf("\ngood choice. you will enjoy your stay.");
				else{
				printf("how dare you. prepare to be attacked");	
				exit(0);}
				break;
		default: printf("please. i am begging you. choose a sensible number. please.");
				 exit(0);
	   }
       
   
    
    for(i=0;i<20;i++){
        if(selected_room==i){
  booked[i]=1;
 printf("\nEnter name: ");
 scanf("%s", S[i].name_of_visitor);
 printf("\nEnter nights of stay: ");
 scanf("%d", &S[i].days_of_stay);
 if(room_type==1){
 S[i].pay=250*S[i].days_of_stay;
 printf("\nYou need to pay %d", S[i].pay);
 printf("\n\nProceed to pay:");
 printf("\nEnter amount: ");
 scanf("%d", &paid);
 if(paid==S[i].pay)
 printf("\nPaid successfully and ready to be terrified\n");
 else if(paid<S[i].pay)
 {S[i].due= (S[i].pay)-paid;
 printf("\npayment due: %d\n", S[i].due);}}
 
 
 else if(room_type==2){
 S[i].pay=300*S[i].days_of_stay;
 printf("\nYou need to pay $%d", S[i].pay);
 printf("\n\nProceed to pay:");
 printf("\nEnter amount: ");
 scanf("%d", &paid);
 if(paid==S[i].pay)
 printf("\nPaid successfully and ready to be terrified\n");
 else if(paid<S[i].pay)
 {S[i].due= (S[i].pay)-paid;
 printf("\npayment due: %d\n", S[i].due);}}
 
 else if(room_type==3){
 S[i].pay=200*S[i].days_of_stay;
 printf("\nYou need to pay $ %d", S[i].pay);
 printf("\n\nProceed to pay:");
 printf("\nEnter amount: ");
 scanf("%d", &paid);
 if(paid==S[i].pay)
 printf("\nPaid successfully and ready to be terrified\n");
 else if(paid<S[i].pay)
 {S[i].due= (S[i].pay)-paid;
 printf("\npayment due: %f\n", S[i].due);}}
 
 else if(room_type==4){
 S[i].pay=500*S[i].days_of_stay;
 printf("\nYou need to pay $%d", S[i].pay);
 printf("\n\nProceed to pay:");
 printf("\nEnter amount: ");
 scanf("%d", &paid);
 if(paid==S[i].pay)
 printf("\nPaid successfully and ready to be terrified\n");
 else if(paid<S[i].pay)
 {S[i].due= (S[i].pay)-paid;
 printf("\npayment due: %d\n", S[i].due);}}
 
 
}
 }
 
 int stop;
 printf("press 1 to stop and 0 to continue:  ");
 scanf("%d", &stop);
 if(stop==1)
{ j=20;}
 j++;
 
 if(stop==1){
 printf("Booking summary: \n");
 for(i=0;i<20;i++){
 if(booked[i]==1)
 printf("Visitor:%s \n Due:%d \n\n", S[i].name_of_visitor, S[i].due);}}}

 return 0;
}
