# VÖLUNDR 

## <img src="https://raw.githubusercontent.com/8an3/midgardr-notes/main/utils/vulknut.png" width="32"  style="vertical-align: middle; margin-bottom: 4px;"> Format JSON

Avialable to trigger via the second registered json formatter or by using 'ocrmnavigator.format.json.file' in a bifrost config item, featuring the following formatting options:
- any object within the array that does not contain children will be converted from multi line to single line
- removes all trailing commas that are followed by a closing bracket
- adds trailing commas to any object that is not followed by a closing bracket
- removes all inline comments
- removes all block comments

For some reason I just couldn't get the inline conversion to work right before but now it finally it works flawlessly as I hate how much space multiline objects waste, and personally I find it way easier to not only read by following inline objects instead of objects that take up the massive amount of space they typically do


## <img src="https://raw.githubusercontent.com/8an3/midgardr-notes/main/utils/vulknut.png" width="32"  style="vertical-align: middle; margin-bottom: 4px;"> Organize Objects by Value Property

- triggered via the editors context menu contained in the root level
- once triggered it will take each arrays objects and sort each of them by the value property contained within each object, alphatically

> [!NOTE]
> The following sections were lost during the last documentation overhaul. Be that as it may till they can be created again, here is a placeholder since each feature is obvious to what it does, you only really need to know how to trigger it.
> 
> Each of the following features can be found in the editors context menu, either in the root level or contained within the formatters sub menu, except for one 'json validator' which is found among [midgardr's tool set](https://catalyst-software.vercel.app/asgard/midgardr/home/JSON-Formatter-and-Validator).

## <img src="https://raw.githubusercontent.com/8an3/midgardr-notes/main/utils/vulknut.png" width="32"  style="vertical-align: middle; margin-bottom: 4px;"> Trailing Commas
## <img src="https://raw.githubusercontent.com/8an3/midgardr-notes/main/utils/vulknut.png" width="32"  style="vertical-align: middle; margin-bottom: 4px;"> Comment Killer
## <img src="https://raw.githubusercontent.com/8an3/midgardr-notes/main/utils/vulknut.png" width="32"  style="vertical-align: middle; margin-bottom: 4px;"> Unused Imports
## <img src="https://raw.githubusercontent.com/8an3/midgardr-notes/main/utils/vulknut.png" width="32"  style="vertical-align: middle; margin-bottom: 4px;"> Inline Imports
## <img src="https://raw.githubusercontent.com/8an3/midgardr-notes/main/utils/vulknut.png" width="32"  style="vertical-align: middle; margin-bottom: 4px;"> JSON Validator


