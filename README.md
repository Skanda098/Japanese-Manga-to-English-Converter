<h1>Japanese Manga to English Converter</h1>

<b><h2> Requirements : (Works best with the following versions)</h2></b>
Microsoft C++ Build Tools - MSBuild version 18.3.0-release-26070-10+3972042b7 for .NET Framework  <a href="https://visualstudio.microsoft.com/downloads/?q=build+tools"> Download </a> <br>
Python 3.11.7 <a href="https://www.python.org/ftp/python/3.11.7/python-3.11.7-amd64.exe">Download</a> <br>
rustc 1.93.1  <a href="https://win.rustup.rs/x86_64">Download</a> <br><br>
<b><h3>❗️ Python Should be of 3.11 version because of modification of some of the libraries of numpy in the latest version of python ❗️</h3></b><br>

<h2>Process : <b>(For First Time)</b><br></h2>

Cmd (run as administrator) --> then type the following commands

```
git clone https://github.com/Skanda098/Japanese-Manga-to-English-Converter.git

cd Japanese-Manga-to-English-Converter

python -m venv venv

venv\Scripts\activate

pip install -r requirements.txt

exit
```

<p>
<h2>Process : <b>(After the first time is done)</b><br></h2>

Cmd (run as administrator) --> then type the following commands <br>
```
cd Japanese-Manga-to-English-Converter

venv\Scripts\activate
```
There are two methods to proceed :<br>
1. Using CMD <br>
2. Using the Server local host to get a UI form in the browser and upload the images directly (Easy for Beginners) <br><br>

For CMD Method (Edit to your desired input and output folder address) :
```
python -m manga_translator local -v -i "INPUT FOLDER ADDRESS" --dest "OUTPUT FOLDER ADDRESS" --config-file examples\config-example.json
```
<br>For Server Method :
```
cd server
python main.py
```
</p>
<br><br>

<h2><b>⚠️ Errors & Troubleshooting :</b><br></h2>
<p>
This specific error—ImportError: DLL load failed... An Application Control policy has blocked this file—is a strict Windows security block.

When you installed the pydensecrf package earlier, it compiled a C++ library (specifically the eigen library) into a .dll or .pyd file so Python could run it quickly. Because this compiled file does not have an official, paid digital signature from a verified software corporation, Windows is treating it as a suspicious, unauthorized script and forcefully killing the process.

This is almost always caused by Windows Smart App Control, Windows Defender, or a strict third-party antivirus (like McAfee or Norton).

Here is how to clear the blockade so your script can run.
<br><br>

<b><h3>Method 1 :</h3></b> Add a Windows Defender Exclusion (Most Common)
You need to tell Windows that your project folder is safe to execute unsigned code.

Click the Windows Start Menu and type Windows Security, then press Enter.

Click on Virus & threat protection.

Under "Virus & threat protection settings," click Manage settings.

Scroll all the way down to the "Exclusions" section and click Add or remove exclusions.

Click the + Add an exclusion button and select Folder.

Navigate to your project folder and select this exact directory:
C:\Users\skand\Desktop\Sample 2\Japanese-Manga-to-English-Converter

Accept the administrator prompt.
<br><br>

<b><h3>Method 2 : </h3></b> Disable Smart App Control (Windows 11)
If you are on Windows 11, a feature called Smart App Control is notorious for blocking perfectly safe Python developer libraries.

Open Windows Security.

Click on App & browser control on the left sidebar.

Click on Smart App Control settings.

If it is set to "On" or "Evaluation", change it to Off.
(Note: Windows will warn you about turning this off, but it is often necessary for programming environments that compile local code. Once turned off, you cannot turn it back on without reinstalling Windows, so use this as a secondary option).
</p>
