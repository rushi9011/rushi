@model PageSections

<!DOCTYPE html>
<html>
<head>
    <title>Edit Page</title>
    <script src="https://cdn.ckeditor.com/4.16.2/standard/ckeditor.js"></script>
</head>
<body>
    <h2>Edit Page</h2>
    <br>

    @using (Html.BeginForm())
    {
        @Html.AntiForgeryToken()

        <div>
            @Html.ValidationSummary(true, "", new { @class = "text-danger" })

            <div>
                <label asp-for="Header"></label>
                <textarea asp-for="Header" class="form-control ckeditor"></textarea>
                <span asp-validation-for="Header" class="text-danger"></span>
            </div>
            <br>

            <div>
                <label asp-for="Footer"></label>
                <textarea asp-for="Footer" class="form-control ckeditor"></textarea>
                <span asp-validation-for="Footer" class="text-danger"></span>
            </div>
            <br>

            <div>
                <label asp-for="Left"></label>
                <textarea asp-for="Left" class="form-control ckeditor"></textarea>
                <span asp-validation-for="Left" class="text-danger"></span>
            </div>
            <br>

            <div>
                <label asp-for="Right"></label>
                <textarea asp-for="Right" class="form-control ckeditor"></textarea>
                <span asp-validation-for="Right" class="text-danger"></span>
            </div>
            <br>

            <div>
                <label asp-for="Center"></label>
                <textarea asp-for="Center" class="form-control ckeditor"></textarea>
                <span asp-validation-for="Center" class="text-danger"></span>
            </div>
            <br> 

            <div>
                <input type="submit" value="Save" class="btn btn-primary" />
                <a asp-action="Index">Back to List</a>
            </div>
        </div>
    }

    <script>
        CKEDITOR.replaceAll('ckeditor');
    </script>
</body>
</html>


---------------new code-------------------------------------------------------

@model PageSections

<!DOCTYPE html>
<html>
<head>
    <title>Edit Page</title>
    <script src="https://cdn.tiny.cloud/1/YOUR_API_KEY/tinymce/5/tinymce.min.js" referrerpolicy="origin"></script>
</head>
<body>
    <h2>Edit Page</h2>
    <br>

    @using (Html.BeginForm())
    {
        @Html.AntiForgeryToken()

        <div>
            @Html.ValidationSummary(true, "", new { @class = "text-danger" })

            <div>
                <label asp-for="Header"></label>
                <textarea asp-for="Header" class="form-control"></textarea>
                <span asp-validation-for="Header" class="text-danger"></span>
            </div>
            <br>

            <div>
                <label asp-for="Footer"></label>
                <textarea asp-for="Footer" class="form-control"></textarea>
                <span asp-validation-for="Footer" class="text-danger"></span>
            </div>
            <br>

            <div>
                <label asp-for="Left"></label>
                <textarea asp-for="Left" class="form-control"></textarea>
                <span asp-validation-for="Left" class="text-danger"></span>
            </div>
            <br>

            <div>
                <label asp-for="Right"></label>
                <textarea asp-for="Right" class="form-control"></textarea>
                <span asp-validation-for="Right" class="text-danger"></span>
            </div>
            <br>

            <div>
                <label asp-for="Center"></label>
                <textarea asp-for="Center" class="form-control"></textarea>
                <span asp-validation-for="Center" class="text-danger"></span>
            </div>
            <br> 

            <div>
                <input type="submit" value="Save" class="btn btn-primary" />
                <a asp-action="Index">Back to List</a>
            </div>
        </div>
    }

    <script>
        tinymce.init({
            selector: '.form-control',
            height: 300,
            plugins: 'advlist autolink lists link image charmap print preview anchor textcolor',
            toolbar: 'undo redo | bold italic underline | fontsizeselect | forecolor backcolor | alignleft aligncenter alignright alignjustify | bullist numlist outdent indent | removeformat | help',
            menubar: false
        });
    </script>
</body>
</html>

