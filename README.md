To add actual content to each field group in WordPress using **Advanced Custom Fields (ACF)**, follow these steps:

### 1. **Create or Edit a Field Group:**
   - Go to **Custom Fields > Field Groups**.
   - Either create a new field group or edit an existing one.
   - Add individual fields you want (e.g., text, image, WYSIWYG editor) and define where they will appear on the site (post, page, CPT, etc.).

### 2. **Assign the Field Group to a Post/Page:**
   - Go to the post or page where you want to use the custom fields.
   - When editing the post/page, you'll see your custom fields as input areas. Fill in the actual content for each field.

### 3. **Display Field Group Contents in Templates:**
   - To show the content from your custom fields on the front end, you'll need to modify your theme template files.
   - Open the relevant template file (e.g., single.php for posts, page.php for pages, or a custom template for CPT).
   - Use ACF’s function `the_field()` or `get_field()` to display the content. Here's an example:

   ```php
   <?php if ( have_posts() ) : while ( have_posts() ) : the_post(); ?>
      <h1><?php the_title(); ?></h1>
      <div><?php the_field('your_custom_field_name'); ?></div>
   <?php endwhile; endif; ?>
   ```

   Replace `'your_custom_field_name'` with the actual name of the field you created.

### 4. **Save and Test:**
   - Save the changes to your template.
   - Preview the post/page to ensure the field group content displays as expected.

This is how you can add and display actual contents for field groups in WordPress.
