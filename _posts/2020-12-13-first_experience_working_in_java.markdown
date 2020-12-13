---
layout: post
title:      "First Experience Working in Java"
date:       2020-12-13 20:49:49 +0000
permalink:  first_experience_working_in_java
---

Hey all!

As of recently, I am in the interview process for a job that has asked me to take an introductory course in Java. At first, I wasn't sure what to expect, but it has so far been a really interesting process. It's different in a lot of ways from JS and React/Redux, but at the same time shares a lot of similarities.

Like Ruby, which I already knew a little bit about, Java is an object oriented language. As such, it uses classes to bundle together code and behaviors belonging to similar objects. But there's a big difference compared to Ruby and JS that has taken me some time to get used to. Namely, this is the declaration of return types.

You see, in JS, a function would be written as such:

```
function returnValue(value) {
  return value
}
```

In Java, this function would work very similarly. However, in Java, the signature (or title) of the function must include the type of value that is being returned. If you are passing an argument into the function, its type must also be specified. So if you wanted to write the function above in Java (in Java they are referred to as methods), and you wanted it to return a String object, you would write it as follows:

```
public String returnValue(String value) {
  return value;
}
```

As you can see here, we have to write 'String' before the name of the method, and also before the name of the argument. Otherwise this method will not work. If you don't want to return anything, you can type 'void' as the return type.

Something else you may notice is 'public' in the method's signature. This has to do with access modifiers, which are another feature of Java that was new to me. However, that is a complex topic best left for another time.

The last big difference here that I struggle sometimes to remember is the semicolon ending the line inside the method. You may notice that I didn't include one in the JS example above, but did include it in the Java example. This is because in JS, ending lines with semicolons is optional. It's considered to be good practice, but your code is still perfectly able to compile and run without them. In Java, however, this is not the case. Your code will not successfully compile if you have lines that are missing a semicolon at the end. For this reason, I highly encourage anyone learning JS right now to always get in the habit of using semicolons. Building the habit of doing so now will greatly help you if you decide to learn Java in the future.

Java may be a little tricky to learn at first, but once you get the hang of it and learn the differences between it and other object oriented languages, it can be quite fun and engaging. I hope this was helpful!
