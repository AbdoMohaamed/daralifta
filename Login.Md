@model Conference.Areas.ViewModel.AdminViewModel

@*----------------------------------------------------*@
<!DOCTYPE html>
<html lang="ar-EG" dir="rtl">
<head>
    @{
        Layout = null;
    }
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width, initial-scale=1, shrink-to-fit=no">
    <title>تسجيل الدخول</title>
    <link href="~/Areas/Content/Themes/css/app.css" rel="stylesheet" /> 
</head>

<body>
    <div class="wrapper ">
        <nav id="sidebar" class="sidebar js-sidebar">
            <div class="sidebar-content js-simplebar">
                <a class="sidebar-brand" href="index.html">
                    <span class="align-middle">الرئيسية</span>
                </a>

                <ul class="sidebar-nav" dir="rtl">

                    <li class="sidebar-item active">
                        <a class="sidebar-link" href="/News">
                            <i class="align-middle" data-feather="sliders"></i> <span class="align-middle">الاخبار</span>
                        </a>
                    </li>

                </ul>
            </div>
        </nav>

        <div class="main">
            <nav class="navbar navbar-expand navbar-light navbar-bg">
                <a class="sidebar-toggle js-sidebar-toggle">
                    <i class="hamburger align-self-center"></i>
                </a>
            </nav>
            <div class="container-fluid">
                <div class="row mb-2 mb-xl-3">
                    <div class="col-auto d-none d-sm-block">
                        <img src="~/Areas/Content/Themes/img/photos/logoo.png" class="img-responsive" style="max-height:60px!important">
                    </div>
                    <div class="col-auto ml-auto text-left mt-n1">
                        <nav aria-label="breadcrumb">
                            <ol class="breadcrumb bg-transparent p-0 mt-1 mb-0">
                                <li class="breadcrumb-item">مؤتمر الإمانة</li>
                                <li class="breadcrumb-item active">صفحة تسجيل الدخول </li>
                            </ol>
                        </nav>
                    </div>
                </div>
            </div>
            <div class="login_style">
                <div class="row">
                    <div class="col-md-3 ">
                    </div>
                    <div class="col-md-6 ">
                        <div class="card">
                            <div class="card-body">
                                <h2>مرحبا بكم </h2>
                                    <form  class="needs-validation" novalidate method="post" action="/Admin/Login">
                                        @Html.AntiForgeryToken()
                                        <h4>برجاء إدخال بيانات الدخول الخاصة بكم </h4>
                                        <hr>
                                        <div class="error_message">
                                            @Html.DisplayFor(model => model.Message, new { @class = "text-danger" })
                                        </div>
                                        <div class="form-group">
                                            <label class="control-label col-md-2 label_style" for="UserName">اسم المستخدم</label>
                                            <div class="col-md-10">
                                                <div class="form-group">
                                                    <label class="text-inverse" for="validationCustom01">اسم المستخدم</label>
                                                    <input type="text" class="form-control" name="UserName" id="validationCustom01" placeholder="اسم المستخدم" required>
                                                    <div class="invalid-feedback">
                                                        أدخل اسم المستخدم !
                                                    </div>
                                                </div>
                                            </div>
                                        </div>
                                        <div class="form-group">
                                            <label class="control-label col-md-2 label_style" for="Password">كلمة المرور</label>
                                            <div class="col-md-10">
                                                <div class="form-group">
                                                    <label class="text-inverse" for="validationCustom01">كلمة المرور</label>
                                                    <input type="Password" name="Password" class="form-control" id="validationCustom01" placeholder="كلمة المرور" required>
                                                    <div class="invalid-feedback">
                                                       أدخل الرقم السرى !
                                                    </div>
                                                </div>
                                            </div>
                                        </div>

                                        <div class="form-group" style="padding-top:5px">
                                            <div class="checkbox">
                                                <input class="check-box" data-val="true" data-val-required="The تذكر بيانات الدخول field is required." id="RememberMe" name="RememberMe" type="checkbox" value="true"><input name="RememberMe" type="hidden" value="false">
                                                <label class="control-label col-sm-7 label_style" for="RememberMe">تذكر بيانات الدخول</label>
                                            </div>
                                            <div class="col-sm-5">
                                                <span class="field-validation-valid text-danger" data-valmsg-for="RememberMe" data-valmsg-replace="true"></span>

                                            </div>
                                        </div>

                                        <div class="form-group text-center">
                                            <div class="col-md-offset-2 col-md-10">
                                                <button class="btn btn-info" type="submit">تسجيل الدخول </button>
                                            </div>
                                        </div>
                                    </form>
                               
                            </div>
                        </div>
                    </div>
                </div>
            </div>

            <footer class="footer">
                <div class="container-fluid">
                    <div class="row text-muted">
                        <div class="col-6 text-start">
                            <p class="mb-0">
                                <a class="text-muted" href="https://adminkit.io/" target="_blank"><strong>الرئيسية</strong></a> - <a class="text-muted" href="https://adminkit.io/" target="_blank"><strong>قالب الإدارة  </strong></a> &copy;
                            </p>
                        </div>
                        <div class="col-6 text-end">
                            <ul class="list-inline">
                                <li class="list-inline-item">
                                    <a class="text-muted" href="https://adminkit.io/" target="_blank">الدعم</a>
                                </li>
                                <li class="list-inline-item">
                                    <a class="text-muted" href="https://adminkit.io/" target="_blank">مركز المساعدة</a>
                                </li>
                                <li class="list-inline-item">
                                    <a class="text-muted" href="https://adminkit.io/" target="_blank">الخصوصية</a>
                                </li>
                                <li class="list-inline-item">
                                    <a class="text-muted" href="https://adminkit.io/" target="_blank">الشروط</a>
                                </li>
                            </ul>
                        </div>
                    </div>
                </div>
            </footer>
        </div>
    </div>
    @* W8YJN-64F83-9DF7D-W92PF-8B8PX *@
  
  <script type="text/javascript">
 
      (function () {
          'use strict'
          var forms = document.querySelectorAll('.needs-validation')
          Array.prototype.slice.call(forms)
              .forEach(function (form) {
                  form.addEventListener('submit', function (event) {
                      if (!form.checkValidity()) {
                          event.preventDefault()
                          event.stopPropagation()
                      }

                      form.classList.add('was-validated')
                  }, false)
              })
      })()
  </script>
</body>

</html>




