---
layout: layouts/post.njk
title: Contact
templateClass: tmpl-post
eleventyNavigation:
  key: Contact
  order: 7
---

<form>
  <div class="row gx-3">
    <div class="col-md">
      <div class="form-floating mb-3">
        <input type="text" class="form-control" id="floatingInputGrid" required>
        <label for="floatingInputGrid">First Name</label>
      </div>
    </div>
    <div class="col-md">
      <div class="form-floating mb-3">
        <input type="text" class="form-control" id="floatingInputGrid" required>
        <label for="floatingInputGrid">Last Name</label>
      </div>
    </div>
  </div>
<div class="form-floating mb-3">
  <input type="email" class="form-control" id="floatingInput" required>
  <label for="floatingInput">Email address</label>
</div>
<div class="mb-3">
  <label for="exampleFormControlTextarea1" class="form-label">Message</label>
  <textarea class="form-control" id="exampleFormControlTextarea1" rows="4" required></textarea>
</div>
 <div class="form-check mb-3">
      <input class="form-check-input" type="checkbox" value="" id="invalidCheck2" required>
      <label class="form-check-label" for="invalidCheck2">
        I agree to the terms and conditions
      </label>
    </div>
<div class="col">
  <button class="btn btn-outline-primary" type="submit">Send</button>
  </div>    
</form>
