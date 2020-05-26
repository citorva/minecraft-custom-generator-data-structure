# Minecraft custom world configuration schema
JSON schema v7 compatible schema for minecraft custom world generation configuration

## How to use

In your world definition file, set in top-level fields the field:

```json
"$schema": "https://raw.githubusercontent.com/citorva/minecraft-custom-generator-data-structure/master/1.16/20w21a.json"
```

Schema files are compatible with these following text-editors:
 * [Altova XMLSpy 2019r3](https://www.altova.com/xmlspy-xml-editor#json_schema)
 * [JSONBuddy](https://www.json-buddy.com/)
 * [JSONEditor Online](https://jsoneditoronline.org/)
 * [Oxygen JSON Editor](https://www.oxygenxml.com/xml_editor/json.html)
 * [Stoplight Studio](https://stoplight.io/)
 * **[Visual Studio Code](https://code.visualstudio.com/)**
 * [JetBrains IDEs](https://www.jetbrains.com/products.html?fromMenu#type=ide)
 * [Eclipse IDE](https://www.eclipse.org/downloads/eclipse-packages)
 
A more-complete compatible editor list is available at the [JSON-Schema official website](https://json-schema.org/implementations.html#editors)

## Example

```json
{
    "$schema": "https://raw.githubusercontent.com/citorva/minecraft-custom-generator-data-structure/master/1.16/20w21a.json",
    "bonus_chest": false,
    "generate_features": true,
    "seed": 0,
    "dimensions": {
        "minecraft:overworld": {
            "type": "minecraft:overworld",
            "generator": {
                "type": "minecraft:noise",
                "seed": 0,
                "biome_source": {
                    "type": "minecraft:vanilla_layered",
                    "seed": 0
                },
                "settings": "minecraft:overworld"
            }
        },
        "minecraft:the_nether": {
            "type": "minecraft:the_nether",
            "generator": {
                "type": "minecraft:noise",
                "seed": 0,
                "biome_source": {
                    "type": "minecraft:multi_noise",
                    "preset": "minecraft:nether",
                    "seed": 0
                },
                "settings": "minecraft:nether"
            }
        },
        "minecraft:the_end": {
            "type": "minecraft:the_end",
            "generator": {
                "type": "minecraft:noise",
                "seed": 0,
                "biome_source": {
                    "type": "minecraft:the_end",
                    "seed": 0
                },
                "settings": "minecraft:end"
            }
        }
    }
}
```

This file do **exactly** the same work than the default world generator with the seed 0. The advantage of the schema is the auto-completion in compatible text editors and the ability to easily make forms from the file.