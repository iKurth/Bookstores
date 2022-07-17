# Bookstores PocketMine-MP API 4

- FormAPI
- InvMenu
- Bossbar
- Scoreboard

# Links download

- https://github.com/Vecnavium/FormsUI
- https://github.com/Muqsit/InvMenu
- https://github.com/sky-min/bossbarapi

# How to use FormsUI (SimpleForm)

```php
$form = new SimpleForm(function (Player $player, int $data) {
    if ($data === null) {
        return;
    }
    switch($data) {
        case 0:
        $sender->sendMessage("FormsUI");
        break;
    }
});

$form->setTitle("FormsUI");
$form->setContent("github.com/iKurth");
$form->addButton("FormsUI");
$player->sendForm($form);
return $form;
```

# How to use FormsUI (CustomForm)

```php
$form = new CustomForm(function (Player $player, array $data) {
    if ($data === null) {
        return;
    }
    if ($data[0] === 0) {
        $sender->sendMessage("FormsUI");
    }
});

$form->setTitle("FormsUI");
$form->addContent("github.com/iKurth");
$form->addStepSlider("FormsUI", ["FormsUI"]);
$player->sendForm($form);
return $form;
```