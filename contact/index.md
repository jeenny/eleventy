---
layout: layouts/post.njk
title: Contact
templateClass: tmpl-post
eleventyNavigation:
  key: Contact
  order: Latest
---


<form>
  <div class="row gx-3">
    <div class="col-md">
      <div class="form-floating mb-3">
        <input type="email" class="form-control" id="floatingInputGrid">
        <label for="floatingInputGrid">First Name</label>
      </div>
    </div>
    <div class="col-md">
      <div class="form-floating">
        <input type="email" class="form-control" id="floatingInputGrid">
        <label for="floatingInputGrid">Last Name</label>
      </div>
    </div>
  </div>
<div class="form-floating mb-3">
  <input type="email" class="form-control" id="floatingInput" placeholder="name@example.com">
  <label for="floatingInput">Email address</label>
</div>
<div class="form-floating">
  <input type="password" class="form-control" id="floatingPassword" placeholder="Password">
  <label for="floatingPassword">Message</label>
</div>
</form>
