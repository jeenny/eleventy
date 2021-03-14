---
layout: layouts/post.njk
title: Contact
templateClass: tmpl-post
eleventyNavigation:
  key: Contact
  order: Latest
---

<form name="contact" method="POST" data-netlify="true">
    <p>
        <label class="form-label">Your Name: <input type="text" id="name" name="name" class="form-control" /></label>   
    </p>
    <p>
        <label class="form-label">Your Email: <input type="email" id="email" name="email" class="form-control"/></label>
    </p>
    <p>
        <label class="form-label">Your Role: </label>
        <select name="role[]" class="form-select" style="width:auto;" required>
        <option value="leader">Leader</option>
        <option value="follower">Follower</option>
        </select>
    </p>
    <p>
        <label class="form-label">Message: <textarea name="message" class="form-control"></textarea></label>
    </p>
    <p>
        <button class="btn btn-outline-primary" type="submit">Send</button>
</form>
<script>
    //get default border colours (to use on input when validation passes)
    var borderStylePass = document.querySelector('#name').style.border;
    //set fail border colours (to use on input when validation fails)
    var borderStyleFail = '1px solid red';
    //get the form submit button
    var submit_button = document.querySelector('.form_submit');
    //attach form event listener
    submit_button.addEventListener("click", function(event){
        //get the form "name" elemement
        var name = document.querySelector('#name');
        //get the form "email" element
        var email = document.querySelector('#email');
        //all validation is assumed to be passed until tested
        blnValidated = true;
        //change the border as it the validation passed
        name.style.border = borderStylePass;
        //if validation fails change the bln to false and change the input border colour
        if(!name.value){
            blnValidated = false;
            name.style.border = borderStyleFail;
        }
        //if validation fails change the bln to false and change the input border colour
        email.style.border = borderStylePass;
        if(!email.value){
            blnValidated = false;
            email.style.border = borderStyleFail;
        }
        //if validation failed do not allow the form to submit the data
        if(!blnValidated){
            event.preventDefault();
        }
    }, false);
</script>