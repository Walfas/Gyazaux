Gyazaux
=======

Version of [Gyazo client][G] with naming and file extension (PNG or 
JPG) options for upload. Intended for use with [Gyazaux-server][GS].

### Features

Simple image uploading via rectangular selection (see [Gyazo][G]). 
After selecting a screen region, you can choose the name of the file and the 
image type (PNG/JPG) before it gets sent to the server.

Options are available in the `gyazaux.ini` file. Defaults:

	[host]
	upload_server=gyazo.com
	upload_path=/upload.cgi

	[file]
	default_jpg=0
	default_name=
	ask=1
	save_local=.

* `upload_server`: The host that the images will be sent to
* `upload_path`: If using [Gyazaux-server][GS] or [Ben Alman's PHP script][Ben], 
	set this to	point to the PHP file.
* `default_jpg`: If nonzero, JPG will be selected as the default image option
* `default_name`: The file name that shows up in the popup box. 
	* The actual file name that gets sent to the server will be whatever you 
		enter in the box, postfixed with `.png` or `.jpg`. 
	* Leaving this blank is fine too; the naming will be left up to the server.
* `ask`: If zero, the default options will be used each time, without 
	a popup window (like standard Gyazo). Otherwise, popup. 
* `save_local`: If not blank, the image will be saved in the given local 
	directory. Relative directories can be specified with a `.` (e.g., 
	`.\images`). The directory must exist, or there will be an error message.

### Acknowledgements
* Gyazo for Mac was first developed by Toshiyuki Masui
* Gyazowin was developed by [tnj](http://nothing.sh/blog/archives/44)
* Ben Alman's "[Gyazo.. on your own server][Ben]"

[Ben]: http://benalman.com/news/2009/10/gyazo-on-your-own-server/
[G]: http://gyazo.com
[GS]: https://github.com/Walfas/Gyazaux-server

