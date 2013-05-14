## shop_default_img

_v 1.0_

####位置
app-common/classes/bll/ShopBll.php
####代码
```php
<?php
  
/**
* 
* @param int $shop_id 房源ID
* @param string $shop_type 房源类型
* @return obj
*/
public function get_default_img($shop_id, $shop_type) {
	$DShopImg = false;
	$class = self::build_img_class($shop_type);
	apf_require_class($class);
	$da    = $class::data_access();
	try {
	    $DShopImg = $da->filter($class::SHOP_ID, $shop_id)
	                     ->filter($class::IS_DISPLAY, $class::ENUM_IS_DISPLAY_YES)
	                     ->sort($class::IS_DEFAULT)
	                     ->sort($class::ID, 'asc')
	                     ->find_one();
	    unset($da);
	} catch (Exception $e) {}
	return $DShopImg;
}

	
}
```

