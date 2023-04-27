# REGEX-Tutorial
This Repo is for referencing my Githib Gist REGEX Tutorial

[REGEX Github Gist](https://gist.github.com/Olloyd321/46a1e94f7745acf063410a367b542100)

This is a tutorial on the conecept of REGEX.

Regular Expressions (Regex) is a powerful tool used in web development to match patterns in text. It's a sequence of characters that form a search pattern. Regex is used to search, replace, and validate data in web applications.

In other words in this example - a syntax test making it possible to see if an email address is input correctly - such as no spaces, lmiited special characters, empty characters etc.

Regex is used for form validation. For example, to make sure that an email address entered correctly, a regular expression pattern can be used to match the string against the pattern of a valid email address.

Example of a Regular Expression - In this example I will use the concept of REGEX in an email validation form -

                // Here I am obtaining the email input in the HTML file by using 'document.getElementById'
                const emailInput = document.getElementById("email");
                // Here I am defining the regular expression pattern for validating the email 
                const emailPattern = /^\w+([.-]?\w+)*@\w+([.-]?\w+)*(\.\w{2,3})+$/;
                
                // Adding an event listener to the email input field. 
                // Once email is entered, we use the test() method of the regex to check if the input matches the email pattern. 
                // If it does, we set the customValidity property of the email input field to an empty string.
                // This indicates that the input is valid. 
                // Finally I can set the customValidity property to a message asking the user to enter a valid email address.
                
                emailInput.addEventListener("input", () => {
                  if (emailPattern.test(emailInput.value)) {
                    emailInput.setCustomValidity("");
                    // If the customValidity property is an empty string, this indicates there are no validation errors/input is valid.
                  } else {
                    // Otherwise we return an error code to the user
                    emailInput.setCustomValidity("Please enter a valid email address.");
                  }
                });
                
                Notes
                **Setting the customValidity property to an empty string is important because it will clear any previous error messages                   that may have been displayed if the user had entered an invalid email address before. 
                **

Quantifiers

Quantifiers are symbols that indicate how many times the previous character or group should be matched. Here are some common quantifiers:

        +: Matches one or more occurrences of the previous character or group.
        *: Matches zero or more occurrences of the previous character or group.
        ?: Matches zero or one occurrence of the previous character or group.
        {n}: Matches exactly n occurrences of the previous character or group.
        {n,}: Matches n or more occurrences of the previous character or group.
        {n,m}: Matches between n and m occurrences of the previous character or group.

Character Classes

Character classes allow you to match a set of characters, rather than a single character.
Useful Characters and symbols used in regular expressions
        * Letters and digits: These characters match themselves. For example, the letter "a" will match the letter "a" in a string.
        * Quantifiers: These indicate how many times the previous character or group should be matched. For example, the quantifier "+"            means "one or more times", while the quantifier "*" means "zero or more times".
        * Anchors: These match the start or end of a string. For example, the anchor "^" matches the start of a string, while the anchor            "$" matches the end of a string.
        
        Here are some more common character classes:

        [abc]: Matches any one of the characters "a", "b", or "c".
        [a-z]: Matches any lowercase letter from "a" to "z".
        [A-Z]: Matches any uppercase letter from "A" to "Z".
        [0-9]: Matches any digit from 0 to 9.
        [a-zA-Z]: Matches any letter, either lowercase or uppercase.
        
By combining these characters and symbols in various ways, you can create a regular expression pattern that matches the specific pattern of text you are looking for.


Resourceful Links

[Modern Regular Expressions](https://blog.bitsrc.io/modern-regular-expression-for-web-developers-4-techniques-you-didnt-know-21bbc3157441)
[REGEX - How To](https://www3.ntu.edu.sg/home/ehchua/programming/howto/Regexe.html#:~:text=A%20Regular%20Expression%20(or%20Regex,strings%20and%20rejects%20the%20rest)
[Intro to REGEX Concept](https://www.youtube.com/watch?v=7DG3kCDx53c)
