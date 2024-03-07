# daisy

# Forms
# Plugins used:

**Contact Form 7**: https://daisy.ukbonn.de/wp-admin/plugin-install.php?tab=plugin-information&plugin=contact-form-7&TB_iframe=true&width=600&height=550

**Contact Form CFDB7**: https://daisy.ukbonn.de/wp-admin/plugin-install.php?tab=plugin-information&plugin=contact-form-cfdb7&TB_iframe=true&width=600&height=550

**CF7 Smart Grid Design Extension**: https://daisy.ukbonn.de/wp-admin/plugin-install.php?tab=plugin-information&plugin=cf7-grid-layout&TB_iframe=true&width=600&height=550

**Contact Form 7 - Dynamic Text Extension**: https://daisy.ukbonn.de/wp-admin/plugin-install.php?tab=plugin-information&plugin=contact-form-7-dynamic-text-extension&TB_iframe=true&width=600&height=550

Before working with forms, get familiar yourself with WordPress and above plugins and their terminology.

# How to Create an Editable quiz form 

To create a new form. Login with an admin user and open WP dashboard.in "Contact" "tab, you will see the list of forms.

**Create a new form from the scratch:**
1. press "Add New".
2. name the form. 
3. on the right panel, under information fill the 'from key' field with a unique name. If you want this form to be pre populated by the last record of logged-in users, this label should contain the [Form Key String](#form-key-string) (e.g. "ukb-form") in the name. For example: nice-ukb-form-12
4. design your form by deleting/adding new fields and changing the layout. 
5. add a dynamic hidden field and name it "userID" and enter "CF7_get_current_user key='ID'" as value.
6. add a dynamic hidden field and name it "form_key", then copy/past the form key in value field.
7. update the form.

**duplicate and edit template form:**
1. hover over template form and press "duplicate"
2. rename the form.
3. on the right panel, under information edit the 'from key' field and choose a unique name. If you want this form to be pre populated by the last record of logged-in user, this label should contain the [Form Key String](#form-key-string) (e.g. "ukb-form") in the name. For example: nice-ukb-form-12
4. design you form by deleting/adding new fields and changing the layout. 
5. leave the hidden as they are. especially userID and form_key.
6. update the form.

## Redirect on Submission ##
You can define the page to redirect after clicking on the submit button. In order to populate the form with the user's last record, you need to reload the form by refreshing the page. So if you want to see the content after submission, redirect to the same page. 


Back to the forms list. Copy the new form's short code (e.g. [cf7form cf7key="ukb-form-1"]).
Go to "Pages" tab and create a new page. Paste the short code and publish the page.



# Form Key String

In WordPress admin, you should now see a "Theme Settings" menu item. Navigate to this page to change the Form Key String. It is used to detecting CF7 forms that should be editable and pre-populated for logged-in users. cf7 form keys must contain this string to function as desired.


## Styling
If you want a big header as the form title, add a label as the first element in the form. Go to <HTML/> tab and add "form-title" as class name to the label tag. 
example: <div class="field text  form-title"><label for="">Form Title</label>
