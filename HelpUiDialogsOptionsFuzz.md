# Options Fuzzer screen #

Esta pantalla permite configurar las [fuzzing][] opciones:

### Default category ###

The category that will be initially selected shown when the [Fuzz dialog][] is displayed.

### Concurrent scanning threads per host ###

The number of threads the scanner will use per host.
Increasing the number of threads will speed up the scan but may put extra strain on the computer ZAP is running on and the target host.

### Add custom Fuzz file ###

Allows you to add your own files to be used when fuzzing.
These should be text files with one attack per line.
Files are added to the 'fuzzers' directory underneath the ZAP home directory.

## Vease también ##

<table> 
 <tbody>
  <tr>
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td>
   <td> <a href="HelpUiOverview" rel="nofollow">UI Overview</a></td>
   <td>Para una vista general sobre la interfaz de usuario</td>
  </tr> 
  <tr>
   <td>&nbsp;&nbsp;&nbsp;&nbsp;</td>
   <td> <a href="HelpUiDialogsOptionsOptions" rel="nofollow">Options dialogs</a></td>
   <td>for details of the other Options dialog screens</td>
  </tr> 
 </tbody>
</table>


[fuzzing]: HelpStartConceptsFuzz
[Fuzz dialog]: HelpUiDialogsFuzz