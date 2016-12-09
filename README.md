# WELCOME YOU TUTORIAL LEARNING ANDROID [![Build Status](https://travis-ci.org/nomensa/jquery.hide-show.svg)](https://travis-ci.org/nomensa/jquery.hide-show.svg?branch=master)

- [Understand definition class or interface in android studio](#understand-definition-class-or-interface-in-android-studio)
  - [Context](#context)
    - [What is the purpose of class context](#what-is-the-purpose-of-class-context)
  - [Intent](#intent)
    - [Starting intent from onclicklistener](#starting-intent-from-onclicklistener)

##What is the purpose of class context

<p align="center">
It allows access to application-specific resources and classes, as well as up-calls for application-level operations such as launching activities, broadcasting and receiving intents
</p>

##Starting intent from onclicklistener

    protected void addListenerOnButton(){
        btn.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View view) {
                Intent intent = new Intent(MainActivity.this,Level0Activity.class);
                startActivity(intent);
            }
        });
    }
