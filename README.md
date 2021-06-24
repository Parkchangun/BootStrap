# BOOTSTRAP
[Bootstrap Link]("https://getbootstrap.com/docs/5.0/getting-started/introduction/")

## INSTALL

* cdn을 통한 install
  ```html
  <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.0.2/dist/css/bootstrap.min.css" rel="stylesheet" integrity="sha384-EVSTQN3/azprG1Anm3QDgpJLIm9Nao0Yz1ztcQTwFspd3yD65VohhpuuCOmLASjC" crossorigin="anonymous">
  ```
* import를 통한 scss, js install
  ```scss
  //Customize
  @import "../node_modules/bootstrap/scss/functions";
  @import "../node_modules/bootstrap/scss/variables";
  @import "../node_modules/bootstrap/scss/mixins";

  $theme-colors: (
    "primary":    $primary,
    "secondary":  yellowgreen,
    "success":    $success,
    "info":       $info,
    "warning":    $warning,
    "danger":     $danger,
    "light":      $light,
    "dark":       $dark
  );

  //All Bootstrap
  @import "../node_modules/bootstrap/scss/bootstrap.scss";
  ```
  ```js
  //All Bootstrap + popper
  import bootstrap from 'bootstrap/dist/js/bootstrap.bundle'

  //Customize
  import Dropdown from 'bootstrap/js/dist/dropdown'
  import Modal from 'bootstrap/js/dist/modal'

  const dropdownElementList = [].slice.call(document.querySelectorAll('.dropdown-toggle'))
  dropdownElementList.map(function (dropdownToggleEl) {
    return new Dropdown(dropdownToggleEl)
  })

  new Modal(document.getElementById('exampleModal'), {
    backdrop: 'static'
  })
  ```