[[2023-01-26]]

1.  *Rendering* = the process of generating an image from a model, by means of a computer program
2. Big-bang operator
	1. Uses (require 2htdp/universe)
	2. Takes an initial piece of data and several arguments (labeled)
	3. One argument is (on-tick ...) 
		1. Ex: (on-tick advance-cat)
	4. Another is (to-draw)
		1. Ex: (to-draw render)
	5. Ex: (big-bang 10 (on-tick advance-cat) (to-draw render))
		1. 10 = initial position of image
	6. Ex: (big-bang "red" (on-tick next-color 1) (to-draw make-traffic-light))
		1. "red" = initial color
		2. 1 = one second pause before switich colors
3. Key presses
	1. Ex: (handle-key 120 " ")
		1. 120 = initial position
		2. If " " = cat moves to position 0
	2. Updates state of world based on the key pressed
	3. Ex: (big-bang 10 (on-tick advance-cat) (to-draw render) (on-key handle-key))
		1. When " " is pressed, cat is sent back to position 0
			1. Like resetting the animation
		2. 10 = initial position of animation
4. User Interface Framework
	2. Integrate pieces of functionality
	3. Similar to real world frameworks
5. Designing World Programs
	1. Domain analysis (pencil + paper)
		1. Sketch program scenarios
			1. Three or more pics of program at different stages of execution
			2. Drawing animation stages
				1. Ex: cat on left side of screen, cat in middle, cat on right side
		2. Identify constant info
			1. What stays the same in each frame of the animation stages?
				1. Ex: width or height of screen, cat image and y-coordinate 
		3. Identify changing info
			1. What changes throughout the animation?
				1. Ex: x-coordinate of cat
		4. Identify big-bang options
			1. (on-tick)
				1. Change as time goes by (nearly all do)
			2. (to-draw)
				1. Display something (nearly all do)
			3. (on-key)
				1. Change in response to key presses
			4. (on-mouse)
				1. Change in response to mouse activity
			5. (stop-when)
				1. Stop automatically
			6. More options available as well
	2. Build the actual program
		1. There is a template available for building world programs on the Designing Worlds page
		2. Constants
			1. Based on constant info (see above)
		3. Data definitions
			1. Based on changing info (see above)
		4. Functions
			1. main first 
				1. Based on changing info, big-bang options, and data definitions (see above)
			2. wish list entries for big-bang handlers
			3. !!! = functions that are apart of our wish list
		5. Work through wish list until done
