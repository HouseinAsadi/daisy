# daisy

## Forms
### Plugins used:

**Contact Form 7**: https://daisy.ukbonn.de/wp-admin/plugin-install.php?tab=plugin-information&plugin=contact-form-7&TB_iframe=true&width=600&height=550

**Contact Form CFDB7**: https://daisy.ukbonn.de/wp-admin/plugin-install.php?tab=plugin-information&plugin=contact-form-cfdb7&TB_iframe=true&width=600&height=550

**CF7 Smart Grid Design Extension**: https://daisy.ukbonn.de/wp-admin/plugin-install.php?tab=plugin-information&plugin=cf7-grid-layout&TB_iframe=true&width=600&height=550

**Contact Form 7 - Dynamic Text Extension**: https://daisy.ukbonn.de/wp-admin/plugin-install.php?tab=plugin-information&plugin=contact-form-7-dynamic-text-extension&TB_iframe=true&width=600&height=550

Before working with forms, get familiar yourself with WordPress and above plugins and their terminology.

#### How to Create an Editable quiz form 

To create a new form. Login with an admin user and open WP dashboard.in "Contact" "tab, you will see the list of forms.

**Create a new form from the scratch:**
1. press "Add New".
2. name the form. 
3. on the right panel, under information fill the 'from key' field with a unique name. If you want this form to be pre populated by the last record of logged-in users, this label should contain the [Form Key String](#form-key-string) (e.g. "ukb-form") in the name. For example: nice-ukb-form-12
4. design your form by deleting/adding new fields and changing the layout. 
5. add a dynamic hidden field and name it "userID" and enter "CF7_get_current_user key='ID'" as value.
7. update the form.

**duplicate and edit template form:**
1. hover over template form and press "duplicate"
2. rename the form.
3. on the right panel, under information edit the 'from key' field and choose a unique name. If you want this form to be pre populated by the last record of logged-in user, this label should contain the [Form Key String](#form-key-string) (e.g. "ukb-form") in the name. For example: nice-ukb-form-12
4. design you form by deleting/adding new fields and changing the layout. 
5. leave the hidden as they are. especially userID and form_key.
6. update the form.

#### Redirect on Submission ##
You can define the page to redirect after clicking on the submit button. In order to populate the form with the user's last record, you need to reload the form by refreshing the page. So if you want to see the content after submission, redirect to the same page. 


Back to the forms list. Copy the new form's short code (e.g. [cf7form cf7key="ukb-form-1"]).</br>
Go to "Pages" tab and create a new page. Paste the short code and publish the page.


### Form Key String

In WordPress admin, you should now see a "Theme Settings" menu item. Navigate to this page to change the Form Key String. It is used to detecting CF7 forms that should be editable and pre-populated for logged-in users. cf7 form keys must contain this string to function as desired.


### Styling
If you want a big header as the form title, add a label as the first element in the form. Go to <HTML/> tab and add "form-title" as class name to the label tag. </br>
example: \<div class="field text  form-title">\<label for="">Form Title\</label>

## Nomenclature

### Modules
Therapy modules IDs start with "m" and the module number (initially 1-99) followed by sub-module letter (A-Z) </br>
m\[number]\[letter]</br>
examples: m3b, m1a, m26j</br>

### Form keys
**A part of the form key must contain the Form Key String ([Form Key String](#form-key-string)) in order to make it editable.**</br>
It contains the fixed string, module id from the previous section, and the number of the form in its module (1-99). For instance, if we have 4 forms in module: m2a, the form id number of the third form will be 3.</br>
use this pattern to create form keys:</br>
\[form key string ]-\[module id ]-\[form id number]</br>
examples: ukb-form-m2c-5, ukb-form-m1a-1, ukb-form-m26m-24</br>


## Corporate Identity ##
### Color Pallet 

#### Primary Color Variations:
**Elm** rgb(27,105,112)  #1B6970 </br>
**Hippie** Blue rgb(79,156,163) #4F9CA3 </br>
**Morning** Glory rgb(144,210,216) #90D2D8 </br>
**Mint Tulip** rgb(185,236,241) #B9ECF1 </br>
**Iceberg** rgb(220,238,244) #DCEEF4 </br>

#### Accent Color Variations:
**Macaroni and Cheese** rgb(255,193,133) #FFC185 </br>
**Colonial White** rgb(255,236,184) #FFECB8 </br>
 
#### Background Color:
**Romance** rgb(255,254,252) #FFFEFC </br>

#### Gray Range:
**Tuatara** hsl(30,2%,20%) #343332 </br>
**Ironside Gray** hsl(30,2%,40%) #686664 </br>
**Dawn** hsl(30,2%,60%) #9B9997 </br>
**Cloud** hsl(30,2%,80%) #CDCCCB </br>
**Quill Gray** hsl(30,2%,90%) #E6E6E5 </br>

#### Others:


plugin: **Central Color Palette**

### Font Family
Lato: https://fonts.google.com/specimen/Lato

## Pages
title the page using this pattern: m[module number]w[week number]: [title]
example:
m3w1: Was ist Stress überhaupt?

## Users
### Add new user
login with your adminstrator account, and click on "Benutzer" on the left side panel. 
press "Neue Benutzer hinzufügen" to create a new user.
compose the username in following pattern: [module][participant ID] for example m3008
in new user page add the username created with mentioned pattern. 
add email : [username]@daisy.de
set the password.
uncheck "Benutzer Benachrichtigen" 
set the user role to "Abonnent"
press "nueuen benutzer hinzufügen" 
