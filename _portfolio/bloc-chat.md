---

layout: post
title: Bloc Chat
thumbnail-path: "img/bloc-chat.png"
short-description: "An Angular-based chatroom service with a Firebase database"

---

{:.center}
![]({{ site.baseurl }}/img/bloc-chat.png)

## Bloc Chat

Bloc Chat was the first project I completed using both AngularJS and Firebase. It offers the ability to sign in as a user, create new chatrooms, and chat with other people, while storing that chat history in a database along with the time sent and the chatroom it was sent in.   

## Development

The first time using Firebase went well, due to the extensive documentation and general intuitiveness of the code. Angular, on the other hand, provided a little more difficulty for me. I had created multiple controllers to handle the logic of the sidebar, main chat window, and popup modals, but found that much of the same information had to be passed to multiple controllers. This made me consider using the `$rootScope` for a lot of the information that was required in multiple controllers (`currentUser`, `currentRoomId`, etc.) Fortunately I was able to avoid this by looking over what I had written and simplifying my methods of passing around data.  

## Challenges

The most difficult part of development figuring out how to best allow a user to sign in with their email and also provide a password. Firebase has a method for this, `$createUserWithEmailAndPassword`, but I struggled with calling this method in the Authorization Service, but returning any error messages in a promise in the Modal Controller so I could display to the user if they needed a longer or more secure password, or simply if their passwords didn't match. I would eventually scrap the Authorization Service altogether and I ended up injecting the Firebase Auth Service directly into the Modal Controller, which was far more simple and cleaner. 

## Conclusion

I found myself realizing after this project and many others, that if I were to do the whole project over again, I would have done things very differently, knowing what I know now after having the experience of doing things in an inefficient way. The experience itself though was invaluable to teaching me how to properly pass data around in angular and how to arrange relatively complex SPAs.