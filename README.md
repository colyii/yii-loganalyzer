#Yii LogAnalyzer - Log file analyzer yii

## Features:
- Easy connection to the project
- Output messages from the log file
- Filter log messages (Remove unwanted messages from issuance)
- Filter log output (output only error, warning or info)
- Cleaning the log file

## Example:

Print out the widget in the view:

```php
<?php
$this->widget('ext.loganalyzer.LogAnalyzerWidget', array(
        'filters' => array('Text filtering','One more'),
        'title'   => 'Title of the widget' ,
        // 'log_file_path' => 'Absolute path of the Log File',
    ));  
?>
```
In addition:

Also in the expansion is extended to marshurt logs, which adds to the message logger ip client. Connect as follows:

```php
<?php
'log'=>array(
    'class'=>'CLogRouter',
    'routes'=>array(
        ....
        array(
            'class'=>'ext.loganalyzer.LALogRoute',
            'levels'=>'info, error, warning',
            ... 
        ),
        ...
    ),
),
?>
```

## Screenshot:

![Log output](https://raw.github.com/tonybolzan/yii-loganalyzer/master/screenshot.jpg "Display log")