# Javascript Codefragmente für Visual Studio Code

```json
{
  "separator line": {
    "prefix": "--",
    "description": "just a single comment line with 10 dashes",
    "body": ["// - - - - - - - - - -"]
  },
  "class": {
    "prefix": "class scaffold",
    "description": "default class",
    "body": [
      "/**",
      " * @desc      $1",
      " * @package   Webapplication",
      " * @module    $1",
      " * @author    Michael <michael.reichart@gfu.net>",
      " * @version   v1.0.0",
      " * @since     $CURRENT_YEAR-$CURRENT_MONTH-$CURRENT_DATE",
      " * @license   MIT {https://opensource.org/licenses/MIT}",
      " * @copyright (c) $CURRENT_YEAR Michael Reichart, Cologne",
      " */",
      "export default class $1 {",
      "    // - - -",
      "",
      "    /**",
      "     * @desc    constructor",
      "     * @returns {boolean}",
      "     */",
      "    constructor() {",
      "        try {",
      "            // - - -",
      "            $2",
      "            // - - -",
      "        } catch (error) {",
      "            console.log(\"constructor error.\", error.message, error.name)",
      "            return undefined",
      "        }",
      "    }",
      "",
      "    /**",
      "     * @desc    init",
      "     * @returns {boolean}",
      "     */",
      "    init() {",
      "        try {",
      "            // - - -",
      "            return true",
      "            // - - -",
      "        } catch (error) {",
      "            console.log(\"init error.\", error.message, error.name)",
      "            return undefined",
      "        }",
      "    }",
      "}"
    ]
  },
  "method": {
    "prefix": "method scaffold",
    "description": "default method for a class",
    "body": [
      "/**",
      " * @desc    $1",
      " * @param   {type} desc",
      " * @returns {boolean}",
      " */",
      "$1 (a = undefined) {",
      " try {",
      " // - - -",
      "   let a ",
      "",
      "   $2",
      "",
      "   return true",
      " // - - -",
      " } catch (error) {",
      "   console.log(\"$1 error.\", error.message, error.name)",
      "",
      "   return undefined",
      " }",
      "}"
    ]
  },
  "function": {
    "prefix": "function scaffold",
    "description": "default function",
    "body": [
      "/**",
      " * @desc    $1",
      " * @param   {type} desc",
      " * @returns {boolean}",
      " */",
      "function $1 (a = undefined) {",
      " try {",
      " // - - -",
      "   let a ",
      "",
      "   $2",
      "",
      "   return true",
      " // - - -",
      " } catch (error) {",
      "   console.log(\"$1 error.\", error.message, error.name)",
      "",
      "   return undefined",
      " }",
      "}"
    ]
  },
  "try catch": {
    "prefix": "try catch scaffold",
    "description": "default try catch statement with message and name",
    "body": [
      "try {",
      "// - - -",
      "",
      "$1",
      "",
      " return true",
      "// - - -",
      "} catch (error) {",
      "console.log(\"$2 error.\", error.message, error.name)",
      " return undefined",
      "}"
    ]
  }
}
```
