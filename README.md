# code_learner

#include<iostream>
#include<string>
#include<stdlib.h>
#include<windows.h>

void spell(std::string&user_input)
{ std::cout << "You enter the Defense against Dark Arts class" << std::endl << std::endl;
    while (true)
    {
        
        std::cout << "Which of the following spells do you think will light a fire?(1-4): " << std::endl;
        std::cout << "1. Avada Kedavra" << std::endl;
        std::cout << "2. Lumos" << std::endl;
        std::cout << "3. Incendio" << std::endl;
        std::cout << "4. Leviosa" << std::endl;

        
        std::string spell_str;
        std::getline(std::cin, spell_str);
        int spell = std::stoi(spell_str);
        if (spell == 1)
        {
            std::cout << "You Died:((" << std::endl;
            exit(0);
            break ;

        }

        else if (spell == 2)
        {
            std::cout << "This is the wrong spell, try again" << std::endl << std::endl;

        }

        else if (spell == 3)
        {
            std::cout << "You got it!" << std::endl;
            break;
        }

        else if (spell == 4)
        {
            std::cout << "This spell can make you float in the air, try again" << std::endl;
        }

        else
        {
            std::cout << "You entered an invalid option" << std::endl;
            break;
        }

    }
}

void exit_program(std::string&get_input)
{
    
    std::string exit_text;
    std::getline(std::cin, exit_text);
    if (exit_text == "Exit" || exit_text == "exit")
    {
        exit(0);
    }
}




int main()
{
    std::cout << "If you want to exit at any point of the game just type exit or Exit" << std::endl;
    //step 1
    std::cout << "You received a letter from HOGWARTS!" << std::endl;
    std::cout << "Press enter to read the letter" << std::endl;
    std::string enter;
    std::getline(std::cin, enter);
    std::cout << std::endl;
    {
        std::cout << "As you open the Hogwarts seal,You see the words.......\n\
YOU HAVE BEEN ACCEPTED TO HOGWARTS SCHOOL OF WITCHCRAFT AND WIZARDRY" << std::endl;
    }
    //step 2
    std::string exit_program;

    std::cout << "After you enter the dinning hall you go to the sorting hat\nChoose a quality that suits you the most" << std::endl;
  
    std::cout << "A)Bravery\nB)Intellect\nC)Loyalty\nD)Cunning" << std::endl;
    std::string choice;
    std::getline(std::cin, choice);

    if (choice == "a"||choice == "A")
    {
        std::cout << "The Sorting hat is...\n...thinking..." << std::endl << std::endl;
        system("Color 40");
        std::cout << "You are a Gryffindor!" << std::endl;
        
        std::cout << std::endl;

    }

    else if (choice == "b" || choice == "B") {
        std::cout << "The Sorting hat is...\n...thinking..." << std::endl << std::endl;
        system("Color 10");
        std::cout << "You are a Ravenclaw!" << std::endl;
        std::cout << std::endl;

    }

    else if (choice == "c" || choice == "C") {
        std::cout << "The Sorting hat is...\n...thinking..." << std::endl << std::endl;
        system("Color 60");
        std::cout << "You are a Hufflepuff!" << std::endl;
        std::cout << std::endl;

    }

    else if (choice == "d" || choice == "D") {
        std::cout << "The Sorting hat is...\n...thinking..." << std::endl << std::endl;
        system("Color 20");
        std::cout << "You are a Slytherin!" << std::endl;
        std::cout << std::endl;

    }

    else 
    {
        std::cout << "Invalid input.";
        return 0;
    }
    //step 3
    
    
    std::cout << "What class do you want to attend?" << std::endl << std::endl;
    std::cout << "Choose from the options below(a-c):" << std::endl;
    std::cout << "a) Defense against Dark Arts" << std::endl;
    std::cout << "b) Potions Class" << std::endl;
    std::cout << "c) Skip Question" << std::endl;
    std::string choice_1;
    std::getline(std::cin, choice_1);
    
    

     if (choice_1 == "a" || choice_1 == "A")
     {
        std::string user_input;
        spell(user_input);
     }

     else if (choice_1 == "b" || choice_1 == "B")
     {  
         
            std::cout << "What color of potion do you want to make? Choose (1-3)" << std::endl;
            std::cout << "1)Red\n2)Blue\n3)Green" << std::endl;
            std::string color_str;
            std::getline(std::cin, color_str);
            int color = std::stoi(color_str);
            if (color == 1)
            {
                if (choice == "A" || choice == "a")
                {
                    system("Color 04");
                }
                else if (choice == "b" || choice == "B")
                {
                    system("Color 14");
                }
                else if (choice == "C" || choice == "c")
                {
                    system("Color 64");
                }
                else
                {
                    system("Color 24");
                }
                std::cout << "You chose RED..... and made a love potion."<<std::endl;
            }
            else if (color == 2)
            {

                if (choice == "A" || choice == "a")
                {
                    system("Color 41");
                }
                else if (choice == "B" || choice == "b")
                {
                    system("Color 01");
                }
                else if (choice == "C" || choice == "c")
                {
                    system("Color 61");
                }
                else
                {
                    system("Color 21");
                }
                std::cout << "You chose BLUE..... Its a truth potion. As you drink it you reveal a dark secret" << std::endl;
            }
            else if (color == 3)
            {
                if (choice == "A" || choice == "a")
                {
                    system("Color 42");
                }
                else if (choice == "B" || choice == "b")
                {
                    system("Color 12");
                }
                else if (choice == "C" || choice == "c")
                {
                    system("Color 62");
                }
                else
                {
                    system("Color 02");
                }
                std::cout << "You chose Green.....Its the bloodroot potion.Just as you touch it you DIE." << std::endl;
                return 0;

            }
            else
            {
                std::cout << "You entered an invaid option" << std::endl;
                return 0;
            }
     }
     else if (choice_1 == "C" || choice_1 == "c")
     {
         
            int option = MessageBox(NULL, "Are you sure?(Yes or no)", "DISCLAMER", MB_YESNO);
            if (option == IDYES)
            {
                
            }
                    
            else if (option == IDNO)
            {
                std::string user_input;
                spell(user_input);
            }
     }
     else
     {
            std::cout << "Invalid option."<<std::endl;
            return 0;
     }
        
     //step 4
     int ans = MessageBox(NULL, "After class, Malfoy asked you to come to the Slytherin Common room.\nDo you wanna go?", "Hogwarts", MB_YESNO);
     
    
     if (ans == IDYES)
     {
         //step 5
         std::cout << std::endl << "You go to the stone wall in the Dungeons to enter the Slytherin common room\nPlease choose and type the Password to enter the room(all lowercase)\na) aspiration\nb) pure-blood" << std::endl;
         
         std::string pass;
         std::getline(std::cin, pass);
         if (pass != "pure-blood")
         {
             std::cout << "A serpent starts to crawl out and KILLS you";
             return 0;
         }
         else if (pass == "pure-blood")
         {
             std::cout << "A serpent slithered and revealed a door\nYou entered the Slytherin common room\nAfter some time Malfoy asks if you want to go to the FORBIDDEN FOREST " << std::endl ;
             std::cout << "Press enter twice to continue";
             std::cin.ignore();
             std::string empty;
             std::getline(std::cin, empty);
             
             int ans = MessageBox(NULL, "Do you want to go the FORBIDDEN FOREST", "Malfoy", MB_YESNO);
             if (ans == IDYES)
             {
                 std::cout << "You go to the FORBIDDEN FOREST and get caught by Hagrid,then Dumbledore expels all of you. " << std::endl;
                 system("Color fc");
                 std::cout << "GAME OVER";
                 return 0;
             }
             else
             {
                 std::cout << "Good choice! As everyone else got expelled" << std::endl;
                 system("Color 50");
                 std::cout << "GAME OVER.";
             }
         }
         else
         {
             std::cout << "Invalid input." << std::endl;
         }

     
     }
     else
     {  
            std::cout << "Good Choice! You were saved from a disaster."<<std::endl;
            system("Color fc");
            std::cout << "Game Over.";
     }
    return 0;
}
