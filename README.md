<div align="center">

## ATM Simulation


</div>

### Description

This was originally written for rent-a-coder, but since the buyer never accepted any of the bids I decided to post it here. It's really limited but it shows how to use functions and if... else loops. It also shows how to used enum to make a simple menu. You could make a menu without enum, but enum makes it easier to code and to maintain
 
### More Info
 
This program is really limited but it shows how to use functions and if... else loops. It also shows how to used enum to make a simple menu. You could make a menu without enum, but enum makes it easier to code and to maintain

0


<span>             |<span>
---                |---
**Submitted On**   |
**By**             |[Kevin Oliver](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByAuthor/kevin-oliver.md)
**Level**          |Beginner
**User Rating**    |3.8 (15 globes from 4 users)
**Compatibility**  |C\+\+ \(general\), Microsoft Visual C\+\+
**Category**       |[Controls/ Forms/ Dialogs/ Menus](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByCategory/controls-forms-dialogs-menus__3-3.md)
**World**          |[C / C\+\+](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByWorld/c-c.md)
**Archive File**   |[](https://github.com/Planet-Source-Code/kevin-oliver-atm-simulation__3-2586/archive/master.zip)

### API Declarations

iostream.h


### Source Code

```
#include <iostream.h>
void fdeposit()
{
	cout << "Enter the amount to be deposited\n";
	cout << "$";
  float amountdeposited = 0.00;
	cin >> amountdeposited;
	cout << "\n You deposited $" << amountdeposited << "\n";
}
void fwithdraw()
{
	cout << "Enter the amount to be withdrawn\n";
  cout << "$";
	int amountwithdrawn = 0;
	cin >> amountwithdrawn;
	int temp = 0;
	int numberof50s = 0;
	int numberof20s = 0;
	temp = (amountwithdrawn % 10);
	if (temp != 0.00)
	{
		cout << "That amount can not be withdrawn\n";
		return;
	}
	if (amountwithdrawn < 20)
	{
		cout << "That amount can not be withdrawn\n";
		return;
	}
	temp = amountwithdrawn / 10;
	if (temp % 5 == 0)
	{
		numberof50s = (temp / 5);
	}
	else
	{
		if (temp % 2 == 0)
		{
		numberof20s = (temp / 2);
		}
	}
	if ((temp % 5)%2 == 0)
	{
		numberof50s = (temp / 5);
		numberof20s = ((temp %5)/2);
	}
	cout << numberof50s << " $50 bills withdrawn\n";
	cout << numberof20s << " $20 bills withdrawn\n";
	cout << "$" << amountwithdrawn << " withdrawn\n";
}
int main()
{
	cout << "ID = \t C0103060x\n";
	cout << "NAME = \t Claudio A";
	enum menuoptions { deposit = 1, withdraw = 2, balance = 3};
	cout << "Press the corresponding number to access an option\n";
	cout << "1. Deposit money\n";
	cout << "2. Withdraw money\n";
	cout << "3. Balance Inquiry\n";
	int choice = 0;
	cin >> choice;
	if (choice == deposit)
		fdeposit();
	if (choice == withdraw)
		fwithdraw();
	if (choice == balance)
		cout << "Sorry, that option is not yet available!\n";
	return 0;
}
```

