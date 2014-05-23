myBB Bot Class
================

Little Class for writing bots for myBB in PHP. Currently is really badly put together and doesn't do much :)

```php
try{
  $b = new mybbBot("http://example.com/","Username","pass");
  $b->quickReply("showthread.php?tid=1","Post content!");
}
catch(myBBException $e){
  switch ($e->getCause()) {
    case FORUM_NOT_FOUND:
      die("Forum could not be reached");
      break;
    case AUTH_ERROR:
      die("Bad login");
      break;
    default:
      die("Unknown error.");
      break;
  }
}
```
