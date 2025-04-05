# OrchardCore Liquid AdminTemplate
A liquid admin template for OrchardCore

## Possible use case
You want to rapidly prototype admin design iterations without round-tripping to Visual Studio, or, if you are a front-end dev but want more control.

## Versions supported
The minimum OC version is 2.0.0, but there are layout changes in later versions. As such, I have introduced folders indicating which layout offers the best starting point. 
Please note that there are missing bits in these layouts. Take a look at the 'Known Issues' section below.

## How to use
- Enable Admin Templates via Tools >> Admin Templates
- Go to Design >> Admin Templates and create a new template called 'Layout'
- Navigate to the folder that best suits your version of OC, the copy and paste the contents of Layout.liquid 

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

## Known Issues
### OC 2.0.0 Layout
As you can see from the image below, the create New Blogpost button is missing, indicating that since the start off point was 3.0.0-preview- ... there is a section I haven't added to this earlier version's layout yet.
![image](https://github.com/user-attachments/assets/48436e5e-81bc-4f94-8fdb-bb563eecd0ea)


