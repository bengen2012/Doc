## shop_default_img

_v 1.0_

####位置
app-common/classes/bll/ShopBll.php
####代码
```php
<?php
  
   
  public function get_default_img_rent($office_id) {
  	return $this->get_default_img($office_id, 'Rent');
	}
	
}
```

