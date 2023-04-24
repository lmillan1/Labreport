# Lab Report 2

## Part 1

Code for StringServer:


<img width="1512" alt="Screen Shot 2023-04-24 at 2 20 52 PM" src="https://user-images.githubusercontent.com/130090548/234119913-6c018fd0-9a14-42fc-96ad-570ccc9fa910.png">

Screenshot of using /add-message?s=Hello:

<img width="615" alt="Screen Shot 2023-04-24 at 2 19 47 PM" src="https://user-images.githubusercontent.com/130090548/234120301-fca2a1e2-42c0-44e3-9060-80a6ac3205b3.png">


<img width="611" alt="Screen Shot 2023-04-24 at 2 20 01 PM" src="https://user-images.githubusercontent.com/130090548/234120290-30cb3728-8065-430e-86e4-79d07da6fdc5.png">







Screenshot of using /add-message?s=How are you:

<img width="608" alt="Screen Shot 2023-04-24 at 2 20 20 PM" src="https://user-images.githubusercontent.com/130090548/234120238-2112497d-135f-4e08-846f-93aac516fed9.png">



<img width="608" alt="Screen Shot 2023-04-24 at 2 20 33 PM" src="https://user-images.githubusercontent.com/130090548/234120225-28153043-6f74-4f6b-9bc5-ae588b1f5188.png">



For each of the two screenshots, describe:

Which methods in your code are called?


Screenshot using hello:
It calls the method handleRequest()

Screenshot using How are you:

It calles the mthod handleRequest()

What are the relevant arguments to those methods, and the values of any relevant fields of the class?


Screenshot using hello:
URI object representing the incoming request. In this case, the URI path is /add-message and the query string is s=Hello

Screenshot using How are you:
UrI object reperesenting the incoming request. In this case, the URI path is /add-message and the query string is s= How are you.

How do the values of any relevant fields of the class change from this specific request? If no values got changed, explain why.
By values, we mean specific Strings, ints, URIs, and so on. "abc" is a value, 456 is a value, new URI("http://...") is a value, and so on.)


Screenshot using hello:
Message is an emptry string before the request and its value changes to hello after the request

Screenshot using How are you:
message is hello before the request and its value changes to How are you after the request.


# Part 2


# Part 3 
