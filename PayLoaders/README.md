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
7. Si hace clic derecho sobre el tipo de operación de "POST" y selecciona las opciones denominadas "Enviar a repetidor" y luego, vaya a la opción "Repetidor", verá, puede "volver a enviar" esa petición, pero cambia a los parámetros.
8. Then, you must go to the "Request Body Parameters" section and located this parameter called "Email", and end thi row, see arrow, could clic. And show windows expanded where you insert value and "decoder" convert in one value valid.
9. Should located in the folder called "Payloader 01", inside the folder, you will find, that file called "body.txt", this is file contains that body that payloader use in reverse tcp, is very important replace value @IP@ by the real ip in that use in the penetration test.
10. Después de cambiar el valor, copie y pegue el valor de la sesión en el decodificador.
11. After of resend request with payload, open other terminal and typing this is command "nc -nlvp 4242", how "root".
11. Now, just resent request with payload, if all things is okay, you can see that connection reverset and in the terminal one shell of the victims

 Note: You can use virtual machine called "Bike" that by Hack the Box

 



