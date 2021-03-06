# GameMaker Language Functions :: A comprehensive digest of every single function

A single JSON file containing every single GameMaker 8, GameMaker: Studio 1, and GameMaker Studio 2 function.

![GameMaker Language Functions](https://github.com/zbanack/GameMaker-Language-Functions/blob/master/promo.jpg?raw=true)

_Please note that this data has not been curated by hand and may be inaccurate as a result._

Each function contains:

* "name" The name of the function
* "versions": A list of what versions of GameMaker this function can be used in ["GM8", "GMS1", "GMS2"]
* "args": A list of arguments (parameters) it accepts ['a', 'b', 'c']
* "url": A link to the official YoYo Games documentation, if available
* "description":A single-sentence description, sourced from the documentation

## Instructions

To use the docs JSON file, first add the following line of code to the `<head>` of your document. Be sure to change the `path/to/` directory to reflect the file location.
```
<script type="text/javascript" src="path/to/docs.json"></script>
```

You can add the following to the very start of the docs.json file to make the data a constant.

```
const gm_functions = 
```

*Don't forget the semi-colon at the end ;)*

Lastly, simply read the JSON whichever way you prefer. As a quick example, the snippet below will return a list of arguments for a given function, string function_name.

```
function get_args(function_name) {
	for(let i = 0; i < gm_functions.length; i++) {
		if (gm_functions[i].name === function_name) {
			return gm_functions[i].args;
		}
	}
	return -1;
}
 ```

## Usefulness

[GMLsnip.com](https://www.GMLsnip.com), my dependency-free GameMaker Language syntax highlighter, code pretty-printer, and docs-linker relies heavily on this JSON file to help make learning GameMaker Language effortless.

## Authors

* **Zack Banack** - *Initial work* - [Zack Banack](https://github.com/zbanack)

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details

## Acknowledgments

* [YoYo Games, Ltd.](https://yoyogames.com) for writing the official documentation and GameMaker Language
* This project is in no way affiliated with YoYo Games Ltd., GameMaker: Studio, GameMaker Studio 2, or any related products. All documentation and written word belong to YoYo Games, Ltd. or the respective copyright holders.
