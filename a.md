## CM3D2 Tool
##### by Usagirei @ Hongfire 
>CM3D2 Tool is a Command-line Utility to work with KISS CM3D2 Data Files

---
##### **Current Features**
* Unpacking .ARC Files
* Re-Injecting Content into .ARC Files[1]
* Converting Files[2]

[1] Original file required
[2] See conversion table

---
##### **Usage**
	CM3D2Tool <Flags> <Files|Folders>
	Brackets mean [optional] flags

|Mode|Flag|Description|
|-|-|-|
|Extract|-e|Pass one or more **arc** files to unpack|
||[-F]|Extract matching *PATHS* (RegExp)|
||[-f]|Extract matching *FILENAMES* (RegExp)|
|Inject|-i|Pass one or more **arcs or directories** to repack *(original .arc required)*|
|Convert|-c|Pass one or more **files or directories** to convert|
||-f|Converts matching *FILENAMES* in directory (RegExp)|
||-m|Conversion mode *(see table below)*|

###### **Conversion Modes**

|Mode|Description|
|-|-|
|TEX|Converts between TEX and PNG|

##### **Example Commands**

>***SomeArc*** and ***SomeDirectory*** are its .arc and directory counterparts

##### Extracting an Arc
	CM3D2Tool -e <SomeArc>
	
##### Extracting files containing *mizugi* in the name
	CM3D2Tool -e -f ".*mizugi.*" <SomeArc>

##### Converting **.tex** files inside a directory to their containing data
	CM3D2Tool -c -f "\.tex" -m TEX <SomeDirectory>
	
##### Converting **.png** files inside a directory back to their **.tex** counterparts
	CM3D2Tool -c -f "\.png" -m TEX <SomeDirectory>

##### Injecting files back inside **.arc** (Both produce same results)
	CM3D2Tool -i <SomeArc>
	CM3D2Tool -i <SomeDirectory>
	

---
##### **License / Disclaimer**

Copyright (C) Usagirei 2015

>THIS SOFTWARE IS PROVIDED BY THE COPYRIGHT HOLDERS AND CONTRIBUTORS "AS IS" AND ANY EXPRESS OR IMPLIED WARRANTIES,
>INCLUDING, BUT NOT LIMITED TO, THE IMPLIED WARRANTIES OF MERCHANTABILITY AND FITNESS FOR A PARTICULAR PURPOSE ARE DISCLAIMED.
>IN NO EVENT SHALL THE COPYRIGHT HOLDER OR CONTRIBUTORS BE LIABLE FOR ANY DIRECT, INDIRECT, INCIDENTAL, SPECIAL, EXEMPLARY,
>OR CONSEQUENTIAL DAMAGES (INCLUDING, BUT NOT LIMITED TO, PROCUREMENT OF SUBSTITUTE GOODS OR SERVICES; LOSS OF USE, DATA,
>OR PROFITS; OR BUSINESS INTERRUPTION) HOWEVER CAUSED AND ON ANY THEORY OF LIABILITY, WHETHER IN CONTRACT, STRICT LIABILITY,
>OR TORT (INCLUDING NEGLIGENCE OR OTHERWISE) ARISING IN ANY WAY OUT OF THE USE OF THIS SOFTWARE,
>EVEN IF ADVISED OF THE POSSIBILITY OF SUCH DAMAGE.
