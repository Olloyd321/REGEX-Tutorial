# REGEX-Tutorial
This Repo is for referencing my Githib Gist REGEX Tutorial

[REGEX Github Gist](https://gist.github.com/Olloyd321/46a1e94f7745acf063410a367b542100)

[Tutorial](https://user-images.githubusercontent.com/119633009/235035885-392d3a28-9047-4552-896f-053d8ee11aa0.mp4)

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Character Classes](#character-classes)
- [Bracket Expressions](#bracket-expressions)

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

### Quantifiers

Quantifiers are symbols that indicate how many times the previous character or group should be matched. Here are some common quantifiers:

        +: Matches one or more occurrences of the previous character or group.
        *: Matches zero or more occurrences of the previous character or group.
        ?: Matches zero or one occurrence of the previous character or group.
        {n}: Matches exactly n occurrences of the previous character or group.
        {n,}: Matches n or more occurrences of the previous character or group.
        {n,m}: Matches between n and m occurrences of the previous character or group.

### Character Classes

Character classes allow you to match a set of characters, rather than a single character.
Useful Characters and symbols used in regular expressions
        * Letters and digits: These characters match themselves. For example, the letter "a" will match the letter "a" in a string.
        * Quantifiers: These indicate how many times the previous character or group should be matched. For example, the quantifier "+"            means "one or more times", while the quantifier "*" means "zero or more times".
        * Anchors: These match the start or end of a string. For example, the anchor "^" matches the start of a string, while the anchor            "$" matches the end of a string.


### Bracket Expressions

[abc]: Matches any one character that is either "a", "b", or "c".
[a-z]: Matches any one lowercase letter from "a" to "z".
[A-Z]: Matches any one uppercase letter from "A" to "Z".
[0-9]: Matches any one digit from 0 to 9.
[_$]: Matches either an underscore or a dollar sign.
        
By combining these characters and symbols in various ways, you can create a regular expression pattern that matches the specific pattern of text you are looking for.

### Regex Components

LiteralsCharacters in the regex that match themselves. For example, the regex a matches the letter "a" in a string.

Metacharacters: Characters in the regex that have a special meaning, and don't match themselves. Examples of metacharacters include ^, $, ., *, +, ?, |, (, ), {, and }.

### Character Classes
Character classes: Sets of characters that match any one of a group of characters. For example, the regex [abc] matches any of the characters "a", "b", or "c".
Quantifiers: Indicate how many times a character or group of characters should be matched. Examples of quantifiers include * (match zero or more), + (match one or more), ? (match zero or one), {n} (match exactly n times), {n,} (match n or more times), and {n,m} (match between n and m times).
Anchors: Indicate the position in the string where a match should start or end. Examples of anchors include ^ (match at the beginning of the string), $ (match at the end of the string), \b (match at a word boundary), and \B (match not at a word boundary).
Modifiers: Change the behavior of the regex. Examples of modifiers include i (case-insensitive matching), g (global matching), and m (multiline matching).

### Anchors
The caret (^): This anchor matches the start of a line or string. For example, the regex ^abc matches the string "abc" only if it appears at the beginning of a line or string. If the string starts with any other character before "abc", the regex will not match.

The dollar sign ($): This anchor matches the end of a line or string. For example, the regex abc$ matches the string "abc" only if it appears at the end of a line or string. If the string ends with any other character after "abc", the regex will not match.****

Resourceful Links

[Modern Regular Expressions](https://blog.bitsrc.io/modern-regular-expression-for-web-developers-4-techniques-you-didnt-know-21bbc3157441)
[REGEX - How To](https://www3.ntu.edu.sg/home/ehchua/programming/howto/Regexe.html#:~:text=A%20Regular%20Expression%20(or%20Regex,strings%20and%20rejects%20the%20rest)
[Intro to REGEX Concept](https://www.youtube.com/watch?v=7DG3kCDx53c)

[@olloyd321](https://github.com/Olloyd321)
