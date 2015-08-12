# ServiceSmsc Module
SMSC.RU API (smsc.ru) версия 3.4 (05.03.2015)

# Usage examples:
```
$module = wire()->modules->get("ServiceSmsc");
list($sms_id, $sms_cnt, $cost, $balance) = $module->send_sms("79999999999", "Ваш пароль: 123", 0);
list($sms_id, $sms_cnt, $cost, $balance) = $module->send_sms("79999999999", "http://smsc.ru\nSMSC.RU", 0, 0, 0, 0, false, "maxsms=3");
list($sms_id, $sms_cnt, $cost, $balance) = $module->send_sms("79999999999", "0605040B8423F0DC0601AE02056A0045C60C036D79736974652E72750001036D7973697465000101", 0, 0, 0, 5, false);
list($sms_id, $sms_cnt, $cost, $balance) = $module->send_sms("79999999999", "", 0, 0, 0, 3, false);
list($sms_id, $sms_cnt, $cost, $balance) = $module->send_sms("dest@mysite.com", "Ваш пароль: 123", 0, 0, 0, 8, "source@mysite.com", "subj=Confirmation");
list($cost, $sms_cnt) = $module->get_sms_cost("79999999999", "Вы успешно зарегистрированы!");
$module->send_sms_mail("79999999999", "Ваш пароль: 123", 0, "0101121000");
list($status, $time) = $module->get_status($sms_id, "79999999999");
$balance = get_balance();
```
