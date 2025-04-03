# OrchardCore Liquid AdminTemplate
A liquid admin template for OrchardCore

## Possible use case
You want to rapidly prototype admin design iterations without round-tripping to Visual Studio, or, if you are a front-end dev but want more control.

## How to use
- Enable Admin Templates via Tools >> Admin Templates
- Go to Design >> Admin Templates and create a new template called 'Layout'
- Copy and paste the contents of Layout.liquid

## Caution
Edit the file with caution (preferably not on the live), because some errors will break your admin, and you might have to edit the database directly, or restore App_Data from a backup.

## Todos
- Add liquid version of ``` data-bs-theme="@await ThemeTogglerService.CurrentTheme()" data-tenant="@ThemeTogglerService.CurrentTenant" ```
- ~~Add liquid version of ``` @if (Orchard.IsRightToLeft())
    {
        <style asp-name="bootstrap-rtl" version="5" at="Head"></style>
        <style media="all" asp-name="the-admin" version="1" depends-on="bootstrap-rtl,TheAdminLayout" at="Head"></style>
    }
    else
    {
        <style asp-name="bootstrap" version="5" at="Head"></style>
        <style media="all" asp-name="the-admin" version="1" depends-on="bootstrap,TheAdminLayout" at="Head"></style>
    } ```~~
- Test to ensure everything works as expected
