# CMB2-Tab
### CMB2 Tab. Ready to use with a theme

## Use

```php
$cmb2_options = array(
	'id'           => '_titlebox',
	'title'       => __( 'CMB2 Tabs Example', 'cmb2' ),
	'object_types' => array( 'page'), // Post type
	'show_names'   => true, // Show field names on the left
	'closed'     => false, // true to keep the metabox closed by default	
);

// Setup meta box
$cmb2 = new_cmb2_box( $cmb2_options );

new CMB2_Tabs();

$tabs_holder = array(
	'config' => $cmb_options,
	'layout' => 'vertical', // Default : horizontal
	'tabs'   => array()
);

$tabs_holder['tabs'][] = array(
	'id'     => 'tab1',
	'title'  => __( 'Example Tab 1', 'cmb2' ),
	'fields' => array(
		array(
			'name' => __( 'Set Title', 'cmb2' ),
			'id'   => 'header_title',
			'type' => 'text'
		),
		array(
			'name' => __( 'Set Subtitle', 'cmb2' ),
			'id'   => 'header_subtitle',
			'type' => 'text'
		)			
	)
);

$tabs_holder['tabs'][] = array(
	'id'     => 'tab2',
	'title'  => __( 'Example Tab 2', 'cmb2' ),
	'fields' => array(
		array(
			'name' => __( 'Set Author name', 'cmb2' ),
			'id'   => 'name',
			'type' => 'text'
		),
		array(
			'name'    => __( 'Set Background image', 'cmb2' ),
			'id'      => 'header_background2',
			'type'    => 'file',
			'options' => array(
				'url' => false
			)
		)
	)
);


$cmb2->add_field( array(
	'id'   => 'tabs',
	'type' => 'tabs',
	'tabs' => $tabs_holder
));
  
```
## Screenshots
<img src="https://github.com/improy/CMB2-Tab/raw/master/CMB2-Tab-meta.jpg" alt="Image" style="max-width:100%;">

## Tutorial on how to integrate CMB2 Tab in to a WordPress theme 
https://www.proy.info/how-to-create-cmb2-tabs/
