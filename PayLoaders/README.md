# PayLoader Sections.

In this sections, i going to talk about payloaders that use or i improve, maybe that very simple but can help to beginner, a introduce in the world to penetration testing.

# Payloader 01

 Description.

 This is "payloader" create reverse shell in base that concept called "Server Side Template Injection" and this use adding named "HandleBars", that use send command by terminal, with use "nc" that catch command of return.

 Requirement

| Characteristic | Value |
| ------------- | ------------- |
| System Operating  | Linux base  |
| Libraries  | Python, HandleBars  |
| Software  |  BurpSuite   |

Steps

1. Run BurpSuite.
2. Go to section "Proxy"
3. Before go to "Interceptor"
4. Clic to button with text "Open browser"
5. Insert to url machine to attack.
6. In this case of the virtual machine called "Bike" load one form, if add to value in the field that solicitud and click "send", can see in seccion "History" all request and interactions with server, one that thems, is  of type "POST" and contains fields that send in request, one of them this is "email", this is use by  send attack of the malicious code.

 Note: You can use virtual machine called "Bike" that by Hack the Box



