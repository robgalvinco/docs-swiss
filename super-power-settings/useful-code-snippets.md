---
description: Helpful code snippets to be used for certain scenarios
---

# Useful Code Snippets

## Hide My Account link in Nav

Use this when you may be using SSO and do not want people accessing the Account pages

```
<!-- HIDE Account link in Nav and content on all account pages -->          
<style>

a[href="/account"], .my-account  {
  display:none !important;
} 

</style>
```

## Hide Billing & orders

Use this when you are using a 3rd party checkout platform and not using Thinkific's

```
<style>

/* Hide Billing and orders on account menu tab  */
.my-account__menu li:nth-child(n+5){display:none;}

</style>
```

## Hide Subscriptions Section on the Billing Page

Use this when you do not have any subscription products or you have a "payment plan" and do not want people to cancel the payment plan

```
<!-- HIDE SUBSCRIPTIONS SECTION ON BILLING PAGE -->
<style>

.my-account__content #subscriptions { display:none;}
.my-account__billing__h4:nth-of-type(2) { display:none;}

/* Hide delete card button */
#delete-card{display:none;}

/* Don't allow edit card at all */
a[href="/account/billings/credit_card"]  {
    display:none !important;
  }  

</style>
```

## Hide Delete Credit Card Button on the Billing Page

Use this when you do not have any subscription products or you have a "payment plan" and do not want people to delete their card - which will cancel subscriptions

```
<!-- HIDE DELETE CARD ON BILLING PAGE -->
<style>
   #delete-card{display:none;}
</style>
```

## Always hide the progress bar

This will hide the progress bar inside the course player for all courses

```
<style >
    div[class^="_course-progress"] { opacity: 0;height:0; }
</style>
```

## Hide Quiz Instructions

In quiz lessons there are some "obvious instructions" that some prefer not to show. ex: "Choose only ONE best answer". This will hide the instructions for all quiz types, so if you have some that are "choose more than one", than this would not be advised

```
<style>
.take .course-player__quiz__instructions {
display:none;
}
</style>
```



## Hide Header on Reviews Page

Choose an option below and place this into the Site Footer Code Settings:

_**yoursite.thinkific.com/manage/settings?section=site-footer-code#tab-code-analytics**_

```
<style>
    /* will hide the entire header */
    .new-course-review-page  .header, .edit-course-review-page  .header{
        display:none;
    }
    
    /* will hide just the  header  links*/
    .new-course-review-page  .header ul, .edit-course-review-page  .header ul{
        display:none;
    }

</style>
```
