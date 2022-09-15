# netcorejenkin

github is deployed to Jenkin server for CI/CD 

deploy successfully

<table><tr><td><pre>
Started by user david lizhong huang
Running as SYSTEM
Building on the built-in node in workspace <b>C:\ProgramData\Jenkins\.jenkins\workspace\netcoreoctopusway</b>
The recommended git tool is: NONE
No credentials specified
 > git.exe rev-parse --resolve-git-dir C:\ProgramData\Jenkins\.jenkins\workspace\netcoreoctopusway\.git # timeout=10
Fetching changes from the remote Git repository
 > git.exe config remote.origin.url https://github.com/pythonlhugithub/netcorejenkin.git # timeout=10
Fetching upstream changes from https://github.com/pythonlhugithub/netcorejenkin.git
 > git.exe --version # timeout=10
 > git --version # 'git version 2.32.0.windows.2'
 > git.exe fetch --tags --force --progress -- https://github.com/pythonlhugithub/netcorejenkin.git +refs/heads/*:refs/remotes/origin/* # timeout=10
 > git.exe rev-parse "refs/remotes/origin/master^{commit}" # timeout=10
Checking out Revision 20971e6e681ccded1a83de813e640bdb20327bf0 (refs/remotes/origin/master)
 > git.exe config core.sparsecheckout # timeout=10
 > git.exe checkout -f 20971e6e681ccded1a83de813e640bdb20327bf0 # timeout=10
Commit message: "Create README.md"
 > git.exe rev-list --no-walk 20971e6e681ccded1a83de813e640bdb20327bf0 # timeout=10
[netcoreoctopusway] $ cmd /c call C:\Users\PYTHON~1\AppData\Local\Temp\jenkins13468615806350773329.bat

C:\ProgramData\Jenkins\.jenkins\workspace\netcoreoctopusway>dotnet test 
  Determining projects to restore...
  Restored C:\ProgramData\Jenkins\.jenkins\workspace\netcoreoctopusway\netcorejenkin.csproj (in 266 ms).

C:\ProgramData\Jenkins\.jenkins\workspace\netcoreoctopusway>exit 0 
[netcoreoctopusway] $ cmd /c call C:\Users\PYTHON~1\AppData\Local\Temp\jenkins10001633711602240806.bat

C:\ProgramData\Jenkins\.jenkins\workspace\netcoreoctopusway>dotnet publish -c Release 
MSBuild version 17.3.0+92e077650 for .NET
  Determining projects to restore...
  All projects are up-to-date for restore.
  netcorejenkin -> C:\ProgramData\Jenkins\.jenkins\workspace\netcoreoctopusway\bin\Release\net6.0\netcorejenkin.dll
  netcorejenkin -> C:\ProgramData\Jenkins\.jenkins\workspace\netcoreoctopusway\bin\Release\net6.0\publish\

C:\ProgramData\Jenkins\.jenkins\workspace\netcoreoctopusway>exit 0 
[netcoreoctopusway] $ C:\OctopusTools.9.0.0.win-x64\octo.exe pack --id netcorejenkin --version 1.0.10 --format nuget --basePath C:\ProgramData\Jenkins\.jenkins\workspace\netcoreoctopusway\bin\Release\net6.0\publish --include ** --outFolder C:\ProgramData\Jenkins\.jenkins\workspace\netcoreoctopusway --overwrite
Packing netcorejenkin version "1.0.10"...
Saving "netcorejenkin.1.0.10.nupkg" to "C:\ProgramData\Jenkins\.jenkins\workspace\netcoreoctopusway"...
Done.
INFO: Octopus CLI exit code: 0
[netcoreoctopusway] $ C:\OctopusTools.9.0.0.win-x64\octo.exe push --server http://localhost:8055 --apiKey ******** --space Spaces-2 --package C:\ProgramData\Jenkins\.jenkins\workspace\netcoreoctopusway\netcorejenkin.1.0.10.nupkg --package C:\ProgramData\Jenkins\.jenkins\workspace\netcoreoctopusway\netcorejenkin.1.0.4.nupkg --package C:\ProgramData\Jenkins\.jenkins\workspace\netcoreoctopusway\netcorejenkin.1.0.5.nupkg --package C:\ProgramData\Jenkins\.jenkins\workspace\netcoreoctopusway\netcorejenkin.1.0.6.nupkg --package C:\ProgramData\Jenkins\.jenkins\workspace\netcoreoctopusway\netcorejenkin.1.0.7.nupkg --package C:\ProgramData\Jenkins\.jenkins\workspace\netcoreoctopusway\netcorejenkin.1.0.8.nupkg --package C:\ProgramData\Jenkins\.jenkins\workspace\netcoreoctopusway\netcorejenkin.1.0.9.nupkg --ignoreSslErrors --debug
Octopus CLI, version 9.0.0

Detected automation environment: "Jenkins"
Found space: octopusjenkin (Spaces-2)
Space name specified, process is now running in the context of space: octopusjenkin
Handshaking with Octopus Server: http://localhost:8055
GET http://localhost:8055/api
Handshake successful. Octopus version: 2022.2.7965; API version: 3.0.0
GET http://localhost:8055/api/Spaces-2
GET http://localhost:8055/api/users/me
Authenticated as: pythonlhu <pythonlhu@gmail.com> 
Pushing package: C:\ProgramData\Jenkins\.jenkins\workspace\netcoreoctopusway\netcorejenkin.1.0.10.nupkg...
Requesting signature for delta compression from the server for upload of a package with id 'netcorejenkin' and version '1.0.10'
GET http://localhost:8055/api/Spaces-2/packages/netcorejenkin/1.0.10/delta-signature
No package with the same ID exists on the server
Falling back to pushing the complete package to the server
POST http://localhost:8055/api/Spaces-2/packages/raw?overwriteMode=FailIfExists
Pushing package: C:\ProgramData\Jenkins\.jenkins\workspace\netcoreoctopusway\netcorejenkin.1.0.4.nupkg...
Requesting signature for delta compression from the server for upload of a package with id 'netcorejenkin' and version '1.0.4'
GET http://localhost:8055/api/Spaces-2/packages/netcorejenkin/1.0.4/delta-signature
Calculating delta
The delta file (16,263 bytes) is 1.24% the size of the original file (1,312,492 bytes), uploading...
POST http://localhost:8055/api/Spaces-2/packages/netcorejenkin/1.0.10/delta?overwriteMode=FailIfExists
Delta transfer completed
Pushing package: C:\ProgramData\Jenkins\.jenkins\workspace\netcoreoctopusway\netcorejenkin.1.0.5.nupkg...
Requesting signature for delta compression from the server for upload of a package with id 'netcorejenkin' and version '1.0.5'
GET http://localhost:8055/api/Spaces-2/packages/netcorejenkin/1.0.5/delta-signature
Calculating delta
The delta file (16,263 bytes) is 1.24% the size of the original file (1,312,492 bytes), uploading...
POST http://localhost:8055/api/Spaces-2/packages/netcorejenkin/1.0.10/delta?overwriteMode=FailIfExists
Delta transfer completed
Pushing package: C:\ProgramData\Jenkins\.jenkins\workspace\netcoreoctopusway\netcorejenkin.1.0.6.nupkg...
Requesting signature for delta compression from the server for upload of a package with id 'netcorejenkin' and version '1.0.6'
GET http://localhost:8055/api/Spaces-2/packages/netcorejenkin/1.0.6/delta-signature
Calculating delta
The delta file (16,264 bytes) is 1.24% the size of the original file (1,312,493 bytes), uploading...
POST http://localhost:8055/api/Spaces-2/packages/netcorejenkin/1.0.10/delta?overwriteMode=FailIfExists
Delta transfer completed
Pushing package: C:\ProgramData\Jenkins\.jenkins\workspace\netcoreoctopusway\netcorejenkin.1.0.7.nupkg...
Requesting signature for delta compression from the server for upload of a package with id 'netcorejenkin' and version '1.0.7'
GET http://localhost:8055/api/Spaces-2/packages/netcorejenkin/1.0.7/delta-signature
Calculating delta
The delta file (16,263 bytes) is 1.24% the size of the original file (1,312,492 bytes), uploading...
POST http://localhost:8055/api/Spaces-2/packages/netcorejenkin/1.0.10/delta?overwriteMode=FailIfExists
Delta transfer completed
Pushing package: C:\ProgramData\Jenkins\.jenkins\workspace\netcoreoctopusway\netcorejenkin.1.0.8.nupkg...
Requesting signature for delta compression from the server for upload of a package with id 'netcorejenkin' and version '1.0.8'
GET http://localhost:8055/api/Spaces-2/packages/netcorejenkin/1.0.8/delta-signature
Calculating delta
The delta file (16,263 bytes) is 1.24% the size of the original file (1,312,492 bytes), uploading...
POST http://localhost:8055/api/Spaces-2/packages/netcorejenkin/1.0.10/delta?overwriteMode=FailIfExists
Delta transfer completed
Pushing package: C:\ProgramData\Jenkins\.jenkins\workspace\netcoreoctopusway\netcorejenkin.1.0.9.nupkg...
Requesting signature for delta compression from the server for upload of a package with id 'netcorejenkin' and version '1.0.9'
GET http://localhost:8055/api/Spaces-2/packages/netcorejenkin/1.0.9/delta-signature
Calculating delta
The delta file (16,263 bytes) is 1.24% the size of the original file (1,312,492 bytes), uploading...
POST http://localhost:8055/api/Spaces-2/packages/netcorejenkin/1.0.10/delta?overwriteMode=FailIfExists
Delta transfer completed
Push successful
INFO: Octopus CLI exit code: 0
Finished: SUCCESS</pre>
</td></tr></table>

<p>Octopus runbook</p>

<table><tr><td>
<pre>
9 additional lines not shown
September 16th 2022 07:25:10Info
Site "webrunbook" does not exist, creating... 
September 16th 2022 07:25:10Info
Name         : webrunbook 
September 16th 2022 07:25:10Info
ID           : 5 
September 16th 2022 07:25:10Info
State        : Started 
September 16th 2022 07:25:10Info
PhysicalPath : C:\Octopus\Applications\development\netcorejenkin\1.0.16_2 
September 16th 2022 07:25:10Info
Bindings     : Microsoft.IIs.PowerShell.Framework.ConfigurationElement 
September 16th 2022 07:25:10Info
Assigning "IIS:\Sites\webrunbook" to application pool "netcorejenkin1"... 
September 16th 2022 07:25:10Info
Setting physical path of IIS:\Sites\webrunbook to C:\Octopus\Applications\development\netcorejenkin\1.0.16_2 
September 16th 2022 07:25:10Info
Comparing existing IIS bindings with configured bindings... 
September 16th 2022 07:25:10Info
Found existing non-configured binding: http :81:od-temp.example.com 
September 16th 2022 07:25:10Info
Existing IIS bindings do not match configured bindings. 
September 16th 2022 07:25:10Info
Clearing IIS bindings 
September 16th 2022 07:25:10Info
Assigning binding: http *:8035: 
September 16th 2022 07:25:11Info
Anonymous authentication enabled: False 
September 16th 2022 07:25:11Info
Applied configuration changes to section "system.webServer/security/authentication/anonymousAuthentication" for "MACHINE/WEBROOT/APPHOST/webrunbook" at configuration commit path "MACHINE/WEBROOT/APPHOST" 
September 16th 2022 07:25:11Info
Basic authentication enabled: False 
September 16th 2022 07:25:11Info
Applied configuration changes to section "system.webServer/security/authentication/basicAuthentication" for "MACHINE/WEBROOT/APPHOST/webrunbook" at configuration commit path "MACHINE/WEBROOT/APPHOST" 
September 16th 2022 07:25:11Info
Windows authentication enabled: True 
September 16th 2022 07:25:12Info
Applied configuration changes to section "system.webServer/security/authentication/windowsAuthentication" for "MACHINE/WEBROOT/APPHOST/webrunbook" at configuration commit path "MACHINE/WEBROOT/APPHOST" 
September 16th 2022 07:25:12Info
IIS configuration complete 
</pre>
</td></tr></table>
