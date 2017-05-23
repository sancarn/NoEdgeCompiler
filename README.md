# NoEdgeCompiler
Aim - To build an alternative to Edge-JS for C# and VB compilation on Windows-Only systems, using primitive console manipulation.

You can download the current version of the compiler (20160524-Release.rar), this just contains the compiler. Currently no JS-wrapper has been created for the application. This will be next job.

## Compiler Usage:

    Compiler.exe [<Options...>] <Code path...> [<References path...>] [<Exe path...>]
	
## Options [optional]:

	/? = Help
	/C = Compile only. This is the default flag.
	/R = Compile & Run
	/L:{c#/vb} = Language
	
**Note:**
The language flag is normally not required. It is only ever required if C# or VB code is stored in a file other than a .cs and .vb file (respectively).

## Code path:

This file contains VB.NET or C#.NET code to be compiled.
E.G. C:\Programming\Hello.cs
**Example Contents:**

	using System;
	public class HelloWorld
	{
		static public void Main ()
		{
			Console.WriteLine ("Hello World");
		}
	}

## References path:

This is a file path (relative or otherwise) to a file containing paths to references.
If left blank this file defaults to codepath with the extension '.def'.
E.G. C:\Programming\Hello_Refs.txt
**Example Contents:**

	system.dll
	system.windows.forms.dll
	C:\my\awesome\dlls\areAwesome.dll

## Exe path:

This is the path where you want the compiled .exe file to be produced.
If left blank this file defaults to codepath with the extension '.exe'.
E.G. C:\Programming\Hello.exe
	
## Dependencies:
Microsoft Common Language Runtime (CLR) / .NET Framework.
