# VM-Screen-Commands


1.  Start a screen 

        screen
    
2. List all screens
   
       screen -ls
3.  Create a new screen session

        screen -S myScreen
4. Send commands to that session
   
       screen -S my_session -X stuff "echo 'Hello from screen!' > screen_output.txt\n"

5.  Attach to the session 

        screen -r my_session

6. The other person can enter into the screen using

        screen -x session_name

7.  Detach from the session

         Inside the screen, press Ctrl+A then D to detach manually

8.  Rename the session 

        screen -S my_session -X sessionname renamed_session
    
9.  Kill the session
   
        screen -S renamed_session -X quit


10.  Scrollback / Scroll up

          Inside screen: Ctrl+A then [ 


11.  Split screen (multi-region)

              Inside screen: Ctrl+A then S to split horizontally, Ctrl+A then Tab to switch, Ctrl+A then X to close region


12.  Window management

            "Inside screen:"
            "- Ctrl+A then C : create new window"
             "- Ctrl+A then N : next window"
             "- Ctrl+A then P : previous window"
             "- Ctrl+A then <number> : go to specific window"


13.  Logging
    
         "Inside screen: Ctrl+A then H to start logging"
         "Ctrl+A then H again to stop logging. Output saved as screenlog.<n>"



echo "You can explore the session with 'screen -r renamed_session' or check output files like screen_output.txt"
