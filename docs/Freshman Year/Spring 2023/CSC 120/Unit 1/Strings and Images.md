[[2023-01-10]]

1. Arithmetic of Text
	1. Text info is represented as a sequence of keyboard characters enclosed in double-quotes "..."
		1. Called a *string*
	2. string-append for strings is like + for numbers
		1. Ex: (string-append "hello " "world") = **"hello world"**
	3. (string-length s) consumes a string and produces its length
	4. (string-ith s i) extracts a one-character substring located at the i 'th position in s (counting from 0)
	5. (substring s i j) extracts a substring of characters from s, starting at position i up to but not including position j
		1. Includes position i
		2. Indexed from zero
		3. Excludes position j
	6. (number->string n) converts a numeric value to a string
2. Evaluating Operations on Strings
	1. Follows the rules of our [[Arthemetic]]
	2. (+ (string-length (string-append "a" "b")) 2)
		1. (+ (string-length "ab") 2)
		2. (+ 2 2)
		3. = **4**
	3. (+ (string-length (number->string 42)) 1)
		1. (+ (string-length "42") 1)
		2. (+ 2 1)
		3. = **3**
3. Arithmetic of Images 
	1. Images can be easily inserted into your program (using the "Insert"->"Insert Image..." menu item, or just copy-paste from anywhere)
	2. Some primitive operations create new images
		1. Do do this, you must enter (require 2htdp/image) and run on DrRacket
		2. Primitive operations include...
			1. circle
			2. ellipse
			3. line
			4. rectangle
			5. text
			6. triangle
			7. Lots more...
		3. Properties of images
			1. image-width
			2. image-height
		4. Combining images
			1. overlay
			2. above
			3. below