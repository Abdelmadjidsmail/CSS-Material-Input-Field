# CSS Material Input Field

input field like material css using SCSS



##### HTML 

```html
    <div class="input">
        <input id="Name" type="text" placeholder="Name" required />
        <label for="Name">Name</label>
      </div>
      <div class="input">
        <input id="EmailAddress" type="email" placeholder="Email Address" />
        <label for="EmailAddress">Email Address</label>
      </div>
      <div class="input">
        <input id="Password" type="password" placeholder="Password" />
        <label for="Password">Password</label>
      </div>
      <div class="input">
        <textarea name="textarea" id="" cols="30" rows="10" placeholder="area"></textarea>
        <label for="textarea">textarea</label>
      </div>
```

##### CSS

```scss
$invalid_color: #ff0000;
$border_bottom_color : #9b9b9b ;
$placeholder_color :#aaa ;
$on_focus : #009788 ;



.input {
  margin: 10px 0;
  position: relative;
  width: 300px;
}
input,textarea {
  background: transparent;
  border: none;
  border-bottom: solid 2px $border_bottom_color ;
  padding: 20px 2px 5px;
  transition: padding 0.4s;
  width: 80%;
}
input:placeholder-shown+ label,textarea:placeholder-shown + label  {
  color: $placeholder_color ;
  font-size: 14px;
  top: 15px;
}
input:focus +label,textarea:focus + label,
label {
  color: $on_focus;
  font-size: 12px;
  pointer-events: none;
  position: absolute;
  left: 2px;
  top: 2px;
  transition: top 0.4s, left 0.4s, font-size 0.4s;
}
input::placeholder ,textarea::placeholder{
  color: transparent;
  display: none;
}
input:focus,
textarea:focus,
textarea:not(:placeholder-shown),
input:not(:placeholder-shown){
  border-bottom: solid 2px $on_focus;
  outline: none;
}
input:invalid {
  border-bottom: 2px solid $invalid_color;
}

```

