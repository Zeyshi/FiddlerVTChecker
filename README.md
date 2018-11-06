# Fiddler-VTChecker
C# Script which queries VirusTotal for the response body's hash, and returns the detection rate


Installation:
  1) Copy CustomRules.cs and System.Web.Extensions.dll to %user%\Documents\Fiddler2\Scripts
  2) Open CustomRules.cs with your favorite text editor, and add your VirusTotal API Key where it says "ENTER YOUR API KEY HERE"
  3) Open Fiddler, and go to Tools -> Options -> Scripting <br>
    a) Add %user%\Documents\Fiddler2\Scripts\System.Web.Extensions.dll to References <br>
    b) Change Language to C#
  4. Restart Fiddler

Usage:

Simply click the new "Check VT" button added to your toolbar, and wait for the queries to complete.<br>
Depending on how many sessions you have, this could take a while (TODO: implement async queries).<br>
When the process is done, you'll see the results in the Comments column in a Positives/Total format. "VT: N/A" means the hash was not found on VirusTotal, or the API has ran into an issue. "Error" usually means VirusTotal has returned a 403 Unauthorized response, in which case your API Key has, most likely, run out of queries
