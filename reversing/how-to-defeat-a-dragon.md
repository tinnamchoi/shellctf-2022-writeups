# How to defeat a dragon

* ```strings vault | grep SHELLCTF``` gives us ```SHELLCTFH```, but not the full flag. 
* Opening the given file in a text editor gives us ```SHELLCTFH�{5348454H�E�H�U�H�c4c43544H�67b31355H�E�H�U�H�f5233763H�37235316H�E�H�U�H�e675f333H�473793f7H�E�H�U�H�E�d}```
* Removing all the non-hex characters for ```5348454c4c4354467b31355f523376337235316e675f333473793f7d```, then converting it into ASCII text gives us the flag. 
