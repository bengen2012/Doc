## 取默认图方法001

_aka Rec 1.0_

### 方法位置：
 app-common/classes/bll/OfficesBll.php


### 方法如下：

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
  [get_default_img](./office_default_img.md)
