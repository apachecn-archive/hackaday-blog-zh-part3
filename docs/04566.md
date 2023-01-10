# 圣诞老人知道你的联系方式是否使用 PHPMailer < 5.2.18

> 原文：<https://hackaday.com/2016/12/25/santa-knows-if-your-contact-form-uses-phpmailer-5-2-18/>

PHPMailer 是 PHP 中最常用的发送电子邮件的类之一，在低于 5.2.18(当前版本)的版本中有一个严重的漏洞。安全研究人员[Dawid Golunski]刚刚发布了一个有限的建议,指出 PHPMailer 存在一个严重缺陷，该缺陷可能会导致攻击者在 web 服务器用户的上下文中远程执行代码。PHPMailer 被几个开源项目使用，其中有:WordPress、Drupal、1CRM、SugarCRM、Yii 和 Joomla。修补程序已经发布，PHP mailer[敦促所有用户升级他们的系统。](https://github.com/PHPMailer/PHPMailer/blob/master/changelog.md)

要触发此漏洞(CVE-2016-10033)，攻击者似乎只需让 web 应用程序使用易受攻击的 PHPMailer 类发送一封电子邮件。根据应用程序本身的不同，这可以通过不同的方式完成，如联系/反馈表单、注册表单、密码电子邮件重置等。

通过快速比较分析，我们发现易受攻击的代码似乎位于 class.phpmailer.php 的以下行中:

*版本 5.2.17*

```
if (!empty($this->Sender)) {
  $params = sprintf('-f%s', $this->Sender);
}
if ($this->Sender != '' and !ini_get('safe_mode')) {
  $old_from = ini_get('sendmail_from');
  ini_set('sendmail_from', $this->Sender);
}
```

*版本 5.2.18*

```
if (!empty($this->Sender) and $this->validateAddress($this->Sender)) {
  $params = sprintf('-f%s', escapeshellarg($this->Sender));
}
if (!empty($this->Sender) and !ini_get('safe_mode') and $this->validateAddress($this->Sender)) {
  $old_from = ini_get('sendmail_from');
  ini_set('sendmail_from', $this->Sender);
}
```

从上面的代码中，我们可以知道错误来自哪里。研究人员[Dawid Golunski]声称已经开发了一个工作的远程代码执行(RCE)概念证明(PoC)漏洞，他将在稍后的日期发布它，以便给用户时间来升级他们的系统。

所以…系统管理员们，你们还在等什么？去升级吧，如果圣诞老人不睡觉，你也不应该…