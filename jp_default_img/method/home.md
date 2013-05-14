## 取默认图方法001

_v 1.0_

### 业务层方法如下：
####存方位置
app-common/classes/bll/OfficesBll.php
####代码
```php
<?php
  
  /**
   * @param int $office_id 房源ID
   * @return Obj 
   */
   
  public function get_default_img_rent($office_id) {
  	return $this->get_default_img($office_id, 'Rent');
	}
	
}
```

### 底层方法：
####存方位置
app-common/classes/bll/OfficesBll.php
####代码

[ get_default_img](./office_default_img.md)
