# Snippets für SCSS

```json
{
    "material breakpoints": {
        "prefix": "breakpoints (material)",
        "description": "The breakpoints used in Material Design.",
        "body": [
            "@media screen {",
            "    // All devices fallback",
            "    $1",
            "    // Extra-small",
            "    @media (max-width: 599px) {}",
            "    // Small (tablet)",
            "    @media (min-width: 600px) {}",
            "    @media (min-width: 905px) {}",
            "    // Medium (laptop)",
            "    @media (min-width: 1240px) {}",
            "    // Large (desktop)",
            "    @media (min-width: 1440px) {}",
            "}"
        ]
    },
    "long name of a snippets": {
        "prefix": "snippet name",
        "desciption": "description",
        "body": ["Line 1", "Line 2", "Line 3", "$1"]
    },
    "SCSS Doc Block and main comments": {
        "prefix": "docblock",
        "description": " Docblock Comment for SCSS Files",
        "body": [
            "// $1",
            "// ",
            "// @package Webapplication",
            "// @module $2",
            "// @author Michael Reichart <michael.reichart@gfu.net>",
            "// @since $CURRENT_YEAR-$CURRENT_MONTH-$CURRENT_DATE",
            "// @version 1.0.0",
            "// @see i.e. inspired by ... {link to}",
            "// @license MIT {https://opensource.org/licenses/MIT}",
            "// @copyright (c) $CURRENT_YEAR Michael Reichart, Cologne",
            "",
            "$3"
        ]
    },
    "SCSS Doc Block (rendered version) and main comments": {
        "prefix": "docblock",
        "description": "structure for components",
        "body": [
            "/** $1",
            "  *",
            "  * @package Webapplication",
            "  * @module i.e. header",
            "  * @author Michael Reichart <michael.reichart@gfu.net>",
            "  * @since $CURRENT_YEAR-$CURRENT_MONTH-$CURRENT_DATE",
            "  * @version 1.0.0",
            "  * @see i.e. inspired by ... {link to}",
            "  * @license MIT {https://opensource.org/licenses/MIT}",
            "  * @copyright (c) $CURRENT_YEAR Michael Reichart, Cologne",
            "  */",
            "",
            "$2"
        ]
    }
}
```
