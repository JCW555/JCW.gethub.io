```mermaid
flowchart TD
Start([Start]) --> End([End])
```
Start([Start]) --> Generate_Temperature([Generate Random Temperature])
    Generate_Temperature --> Get_User_Guess([Get User Guess])
    Get_User_Guess --> Validate_Input([Validate User Input])
    Validate_Input -->|Invalid Input|> Error_Message([Error Message])
    Validate_Input -->|Valid Input|> Compare_Guess([Compare Guess to Temperature])
    Compare_Guess -->|Too High|> Too_High_Feedback([Too High Feedback])
    Compare_Guess -->|Too Low|> Too_Low_Feedback([Too Low Feedback])
    Compare_Guess -->|Correct|> Correct_Feedback([Correct Feedback])
    Too_High_Feedback --> Get_User_Guess
    Too_Low_Feedback --> Get_User_Guess
    Correct_Feedback --> End([End])