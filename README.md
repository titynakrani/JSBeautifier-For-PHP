# JSBeautifier-For-PHP
CSS, JavaScript (and JSON), HTML And Decryption Forked From Old Version Of JSBeautifier And Stuff I've Built 10 Years Ago

##Usage is quite easy##

```PHP
  /**
   * beautify a JSON/JavaScript like string.
   *
   * @param string $raw_input
   *
   * @return string
   */
  function beautify_json($raw_input) {
    require_once('./beautifier_js.php');
    $result = "";
    try {
      $opts = new BeautifierOptions();
      $opts->indent_size = 2;
      $opts->indent_char = ' ';
      $opts->preserve_newlines = true;
      $opts->jslint_happy = false;
      $opts->keep_array_indentation = true;
      $opts->brace_style = "collapse"; //end-expand
      $jsbeautifier = new JSBeautifier();

      $result = (string)$jsbeautifier->beautify($raw_input, $opts);
    } catch (Exception $e) {

    }

    return $result;
  }


?>
```
