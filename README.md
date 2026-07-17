# Advanced Weather App 
This is an API based project that uses wttr.in API in order to get the information about the weather.
On running the program, it will show you the MAIN MENU containing four options  
1. CURRENT WEATHER REPORT
2. SEARCH HISTORY
3. DELETE SEARCH HISTORY
4. EXIT

<img width="1036" height="276" alt="Screenshot (26)" src="https://github.com/user-attachments/assets/c957fd02-5ffb-425c-b49d-762f32a545c4" />

You can see a number is present before each option. The user has to enter the number present before the option in order to use it.

Now let's understand the functionalities of the four options of the MAIN MENU.

##CURRENT WEATHER REPORT

Enter the integer 1 in order to use this option. Then you have to enter the name of the city whose current weather conditions you want to know. The temperature (°C), humidity(%), weather description and wind speed(in kilometer per hour) will be displayed
<img width="1063" height="350" alt="Screenshot (29)" src="https://github.com/user-attachments/assets/8e5d7bbc-2451-4cbc-b393-cc12ddc9f895" />

A message will appaer  at the bottom. Here if you Enter 'y' or 'Y', the weather forecast of the present day and upcoming two days will be displayed
<img width="1061" height="851" alt="Screenshot (30)" src="https://github.com/user-attachments/assets/275bf491-f143-4a1d-a1ab-d410384e8856" />
 Note that in the output, date is in YYYY-MM-DD format.

 You can see at the bottom, the MAIN MENU appears again, this is because the program is running in an infinite loop. In order to close the program you have to use the EXIT option by entering the integer 4. In this way you will break the infinite loop and you will exit from the program. Let's see the current weather conditions of two more cities but here we are not interested to know the forecast.
 <img width="1130" height="941" alt="Screenshot (34)" src="https://github.com/user-attachments/assets/fad21388-e751-4812-97ee-d7e6eb7b42b3" />


##SEARCH HISTORY

Enter the integer 2 in order to use the SEARCH HISTORY of the MAIN MENU. You will get the entire search historhy containing the searched locations in newest to oldest order i.e. the city which you have searched at first will appear at the bottom and the city which you have searched at last will appear in the top.
<img width="1101" height="931" alt="Screenshot (60)" src="https://github.com/user-attachments/assets/b0e5fb41-9228-485e-971b-447045c54346" />


The names of the cities in the searched history are stored in a binary file, so they are stored in the computer memory permanently and the data will not get lost if you close the program or if the computer is switched off.

You can see integers before the searched cities. You can enter the integer present before the name of the cities in order to see the current weather conditions of the city from the search history itself. For example we want to get the curent weather conditions of kolkata, we have to enter 3.

<img width="1068" height="374" alt="Screenshot (61)" src="https://github.com/user-attachments/assets/52b5d7df-f9ad-41de-a8d3-8a71118436f0" />

Again by entering 'y' or 'Y' you can have the weather forecast of that day and upcoming two days. Else press enter key if you don't want to have the weather forecast.

Now we are going to see the search history again.
<img width="1060" height="677" alt="Screenshot (62)" src="https://github.com/user-attachments/assets/745e5292-8a35-4818-9748-627fb8013f91" />
You can see that KOLKATA is in the top having number 1 before it. This is because, from the search history we have searched kolkata , which is the last search we have done. The remaining cities in the search history can get a new position and accordingly a new number can present infront of them.

Now, if we don't want to search anything from our search history then we will enter 0. Again we will have our MAIN MENU.
<img width="1076" height="455" alt="Screenshot (64)" src="https://github.com/user-attachments/assets/411a1859-171a-4751-8323-c7ceef9de98c" />

##DELETE SEARCH HISTORY

Let's search the current weather conditions of few more cities in order to understand this option clearly.
<img width="1062" height="659" alt="Screenshot (65)" src="https://github.com/user-attachments/assets/cfff8ad9-e6fd-4d1d-937f-3d6a25d00a6d" />
<img width="1054" height="495" alt="Screenshot (67)" src="https://github.com/user-attachments/assets/e37a04c5-be02-4705-a464-023f999fcb44" />

Now let's see the search history.
<img width="1077" height="307" alt="Screenshot (68)" src="https://github.com/user-attachments/assets/1d2c6404-a754-482d-80ea-8a05e1b8cee0" />
To use the DELETE SEARCH HISTORY option from the MAIN MENU , enter the integer 3. After that you have to enter your choice:-
 * If you want to delete particular search(es) from your search history, you have to enter 1.
 * If you want to delete your entire search history, you have to enter 2.

For example, if we want to delete LONDON, KOLKATA and PARIS from the search history, we will enter 1, as we want to delete particular searches. Then we have to enter the number present before a particular search in order to delete it from search history, after that we have to enter 'Y' or 'y' only if we want to delete more. Again we have to enter the number present before a particular search in order to delete it from search history, this cycle will keep on repeating as long as we are entering 'Y' or 'y'. In the search history, the number present before LONDON, KOLKATA and PARIS are 2, 4 and 5 respectively. So, we will deal with them in the same way as it is mentioned above in order to delete their names from the search history.
<img width="1073" height="911" alt="Screenshot (70)" src="https://github.com/user-attachments/assets/83f5f70d-3940-47e4-ab33-f25014ebf94a" />
You can see that a message "required elements are deleted" is displayed after giving the input 'n' instead of 'Y'(or 'y'). Let's see the search history now.
<img width="1095" height="249" alt="Screenshot (71)" src="https://github.com/user-attachments/assets/647beb24-57cc-4da6-b387-f08b323cfbac" />
As we can see LONDON, KOLKATA and PARIS are deleted from search history. The search history is showing the names of the cities in the order that is expected. Before MUMBAI the number 1 is present as it was before and there are new numbers present before PATNA and DELHI, marking their new serial numbers which can be used for operations like getting the current weather report (and getting forecast) and deleting the names of cities present after the numbers in the search history.

Now we want to delete the entire search history. For that we have to use DELETE SEARCH HISTORY option of MAIN MENU by entering 3 and then we have to enter 2 to delete the entire search history. After entering 2, an input message "DO YOU WANT YOUR ENTIRE SEARCH HISTORY TO BE DELETED? ENTER 'Y' IF SO..." will appear. We have to enter 'Y' or 'y' to delete the entire search history. A message "ENTIRE SEARCH HISTORY HAS BEEN DELETED!" will appear.
<img width="1085" height="480" alt="Screenshot (73)" src="https://github.com/user-attachments/assets/f7a8ff31-6d6e-4639-b0d2-d61269755823" />
Now let's see the search history.
<img width="1072" height="501" alt="Screenshot (74)" src="https://github.com/user-attachments/assets/3451d45c-c298-4fe6-abdf-7628edd00bfb" />
As you can see there are no names of any cities in the search history. This is because the entire search history has been deleted.

##EXIT

To use EXIT option of the MAIN MENU you have to enter 4. On using this option, you will break the infinite loop that is running in the program and you will exit from the program.

In case if you enter any integer other than 1 or 2 or 3 or 4, a message "INVALID CHOICE" will be displayed.
<img width="1064" height="385" alt="Screenshot (76)" src="https://github.com/user-attachments/assets/f6badad1-c0b0-47bc-a580-dad66d33fed5" />











 
 
  

