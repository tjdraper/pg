# PG 1.2.0

A plugin to retrieve GET/POST parameters in ExpressionEngine.

## Usage

Example URL: www.domain.com/test?key=value&key2=value2

### Single Tag

	{exp:pg:param key="key2"}

#### Output

	value2

### Tag pair:

*Please note, the old {exp:pg} tag pair is deprecated and replaced by the following tag pair. Your existing code should be updated because a future version of PG will remove the {exp:pg} tag.*

	{exp:pg:pair}
		{key}: {value}<br>
	{/exp:pg:pair}

#### Output:

	key: value
	key2: value2

### Method Parameter

Optional parameter for both the single tag and the tag pair: method="post"  
This will fetch POST data instead of GET data.

#### Example:

	{exp:pg:pair method="post"}
		{key}: {value}<br>
	{/exp:pg:pair}

### Get data from a one dimensional array with param tag

Example URL: www.domain.com/test?key[values]=my_value&key2=value2

#### Tag

	{exp:pg:param key="key" array_key="values"}

#### Output

	Output: my_value

## License

Copyright 2015 Caddis Interactive, LLC

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

	http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.