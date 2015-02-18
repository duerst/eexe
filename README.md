e.exe
=====

What's this?
------------

A tool to invoke an editor for Windows.

+ e.exe can redirect the result of other command from Command Prompt, and pass it to the editor via a temporary file.
+ e.exe can pass the contents in the screen buffer of Command Prompt to the editor via a temporary file.
+ Of course, e.exe can open a file by the editor.


Initial setting
---------------

e.exe invokes the application associated to .txt filetype.
So, you have to associate your favorite editor to .txt filetype.
And, put e.exe to where Path environment variable indicates.


How to use?
-----------

Run e.exe from Command Prompt.

When running e.exe without any parameters, it saves the contents in the screen buffer to a temporary file, and opens the file by the editor.

And, when e.exe is kicked as the target of redirection, it reads the contents from pipe, saves to a temporary file, and opens the file by the editor.

These temporary files will be removed just after the editor is invoked (and e.exe will be end immediatelty.)
If you want to delay removing the files, pass `--wait` switch to e.exe.
If the switch is passed, e.exe will wait the termination of the editor.
These temporary files are created on the current directory.

If you want to open an existing / new file, simply specify the file name as the parameter to e.exe.
You can specify `--wait` switch in this case, too.
Of course, in this case, the file will not removed automatically.


License
-------

Copyright (c) 1998,1999,2003,2008,2013,2014 by U.Nakamura
All rights reserved.

Redistribution and use in source and binary forms, with or
without modification, are permitted provided that the following
conditions are met:

1. Redistributions of source code must retain the above copyright
   notice, this list of conditions and the following disclaimer.
2. Redistributions in binary form must reproduce the above
   copyright notice, this list of conditions and the following
  disclaimer in the documentation and/or other materials provided
  with the distribution.

THIS SOFTWARE IS PROVIDED BY THE AUTHOR AND CONTRIBUTORS ``AS IS''
AND ANY EXPRESS OR IMPLIED WARRANTIES, INCLUDING, BUT NOT LIMITED
TO, THE IMPLIED WARRANTIES OF MERCHANTABILITY AND FITNESS FOR A
PARTICULAR PURPOSE ARE DISCLAIMED.  IN NO EVENT SHALL THE AUTHOR
OR CONTRIBUTORS BE LIABLE FOR ANY DIRECT, INDIRECT, INCIDENTAL,
SPECIAL, EXEMPLARY, OR CONSEQUENTIAL DAMAGES (INCLUDING, BUT NOT
LIMITED TO, PROCUREMENT OF SUBSTITUTE GOODS OR SERVICES; LOSS OF
USE, DATA, OR PROFITS; OR BUSINESS INTERRUPTION) HOWEVER CAUSED
AND ON ANY THEORY OF LIABILITY, WHETHER IN CONTRACT, STRICT
LIABILITY, OR TORT (INCLUDING NEGLIGENCE OR OTHERWISE) ARISING
IN ANY WAY OUT OF THE USE OF THIS SOFTWARE, EVEN IF ADVISED OF
THE POSSIBILITY OF SUCH DAMAGE.
