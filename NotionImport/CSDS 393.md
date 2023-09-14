[https://docs.google.com/spreadsheets/d/1VjH_U-hyeZCp4HSt_Y-spvOpu2WG7iRX-ULAZ9v482Q/edit#gid=0](https://docs.google.com/spreadsheets/d/1VjH_U-hyeZCp4HSt_Y-spvOpu2WG7iRX-ULAZ9v482Q/edit#gid=0) Schedule

[docs.google.com/spreadsheets/d/1mnX2TCIxYSYM-4urj6K41TCNDMjBjOwNbOk8ra7stSE/edit#gid=0](http://docs.google.com/spreadsheets/d/1mnX2TCIxYSYM-4urj6K41TCNDMjBjOwNbOk8ra7stSE/edit#gid=0) Assigned TA

  

https://csds393groupgamer.atlassian.net/jira/software/projects/C3P/boards/2/backlog?selectedIssue=C3P-57

## Checklist

- [x] Study for quiz
- [x] Design doc May 29
- [x] Assignment 2 Apr 4
- [x] Lab lecture material
- [x] Quiz! Thursday
- [x] Implement hover descriptions: [https://www.youtube.com/watch?v=d_qk7egZ8_c](https://www.youtube.com/watch?v=d_qk7egZ8_c)
- [x] Functional Test Doc
- [x] Demo Prep
- [x] Final Report: user manual May 1
- [x] Add token effects
    - [x] [https://www.youtube.com/watch?v=auglNRLM944](https://www.youtube.com/watch?v=auglNRLM944)
    - [x] Write tests:
        - [x] token
        - [x] vanishing token
        - [ ] heavy token
        - [ ] mine token
        - [x] Board manager

  

- Add win checks to delete token
- Add win checks in take turn outside of the if (updateboardstate) block

  

  

[[Scripts]]

  

## Sprites

Connect4 Board [https://www.seekpng.com/ima/u2e6e6e6q8q8u2q8/](https://www.seekpng.com/ima/u2e6e6e6q8q8u2q8/)

  

Not working code: needs to check in both directions independently

/**  
* Checks for win condition of any length sequence  
*/  
private bool DidWin(int playerNum)  
{  
int count = 0;  
int currentToken;  
//Vertical  
for (int y = col - maxOffset; y <= col + maxOffset; y++)  
{  
if (y < 0 || y > height - 1)  
{  
continue;  
}

```
        currentToken = boardState[row, y];        if(currentToken != playerNum)        {            goto HORIZONTAL;        }        else        {            count++;        }        if(count >= goal)        {            return true;        }    }HORIZONTAL:;    //Horizontal    count = 0;    for (int x = col - maxOffset; x <= col + maxOffset; x++)    {        if (x < 0 || x > width - 1)        {            continue;        }        currentToken = boardState[x, col];        if (currentToken != playerNum)        {            goto POSITIVE_DIAGONAL;        }        else        {            count++;        }        if (count >= goal)        {            return true;        }    }//DiagonalPOSITIVE_DIAGONAL:;    count = 0;    for (int offset = -maxOffset; offset <= maxOffset; offset++)    {        if (row + offset < 0 || row + offset > width - 1 || col + offset < 0 || col + offset > height - 1)        {            continue;        }        count = 0;        currentToken = boardState[row + offset, col + offset];        if (currentToken != playerNum)        {            goto NEGATIVE_DIAGONAL;        }        else        {            count++;        }        if (count >= goal)        {            return true;        }    }NEGATIVE_DIAGONAL:;    count = 0;    for (int offset = -maxOffset; offset <= maxOffset; offset++)    {        int yOffset = offset * -1;        if (row + offset < 0 || row + offset > width - 1 || col + yOffset < 0 || col + yOffset > height - 1)        {            continue;        }        count = 0;        currentToken = boardState[row + offset, col + yOffset];        if (currentToken != playerNum)        {            return false;        }        else        {            count++;        }        if (count >= goal)        {            return true;        }    }    return false;}
```