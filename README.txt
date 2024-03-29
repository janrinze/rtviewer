RT viewer is a technology preview for RawTherapee.

The extensive use of OO with C++ can facilitate programmers
to keep their focus on functionality where most of the 'hard work' like
color transformations and memory management is done on the objects.

version 0.0.0

building:

  make rtviewer
  cd rtengine/plugins
  make all

usage:
  rtviewer <rawfile>
  
  With Ubuntu or Debian it is possible to associate raw files to rtviewer
  that way rtviewer will be used to (pre)view raw files with pp3
  
  Zoomin/out : scroll wheel
  panning: hold mouse button and move mouse.
  
  Since some filters like noise filtering are very slow the filterprocess
  will start after 3 seconds of mouse interaction.

  Changes in the corresponding pp3 file will be picked up automatically.
  Any pp3 editor that saves directly after a change is made can now be
  used as an interactive editor for the viewer.

works on:

  Ubuntu/Debian with 32bpp X desktop

depends on:

  $HOME/.config/RawTherapeeAlpha4/profiles/Default.pp3
  it will default to this pp3 file for raw files without a pp3 file.

requirements:

	liblcms2
	X libraries

	builds with -lXext -llcms2 -lgomp -lX11

(c) 2011 Jan Rinze Peterzon janrinze@gmail.com
 