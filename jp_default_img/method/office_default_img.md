## office_default_img

_v 1.0_

####位置
app-common/classes/bll/OfficeBll.php
####代码
```php
<?php
/**
 * 
 * @param int $office_id 	房源ID
 * @param string $office_type 	房源类型
 * @return Obj
 */

public function get_default_img($office_id, $office_type) {
	$DOfficeImg = false;
	try {
		$class = self::build_office_img_class($office_type);
		apf_require_class($class);
		$da = $class::data_access();
		$DOfficeImg = $da->filter($class::OFFICE_ID, $office_id)
		->filter($class::IS_DISPLAY, $class::ENUM_IS_DISPLAY_YES)
		->sort($class::IS_DEFAULT)
		->find_one();
		unset($da);
	} catch (Exception $e) {

	}
	return $DOfficeImg;
}  

	
}
```

