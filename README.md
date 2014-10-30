Substitutions
=============

Default substitution files for use on Pandorabots. Refer to the [blog post](http://blog.pandorabots.com/substitutions-and-sentence-splitting/) for a more detailed explanation of usage.

normal.susbtitution
-------------------

Performs normalization procedures on input strings ("pre-processing").

```
<category>  
<pattern>SAY *</pattern>  
<template><star/></template>  
</category>  
```

Input: Say pandorabots.com  
Output: pandorabots dot com


denormal.substitution
---------------------

Reverses steps taken in normalization procedures.

```
<category>  
<pattern>TAKE ME TO *</pattern>  
<template>Redirecting to <denormalize><star/></denormalize></template.  
</category>  
```

Input: Take me to pandorabots.com.  
Output: Redirecting to pandorabots.com

person.substitution
-------------------

Transforms pronouns between first and second person.

```
<category>  
<pattern>YOU ARE *</pattern>  
<template>I am <person><star/></person></template>  
</category>  
```

Input: You are waiting for me.  
Output: I am waiting for you.

person2.substitution
--------------------

Transforms pronouns between first and third person.

```
<category>  
<pattern>GIVE THE * TO *</pattern>  
<template>User has asked me to give the <star/> to <person2><star index="2"/></person2></template>  
</category>  
```

Input: Give the password to me.  
Output: User has asked me to give the password to him or her.

gender.substitution
-------------------

Transforms gender pronouns between male and female.

```
<category>  
<pattern>DOES IT BELONG TO *</pattern>  
<template>No, it belongs to <gender><star/></gender></template>  
</category>  
```

Input: Does it belong to him?  
Output: No, it belongs to her.