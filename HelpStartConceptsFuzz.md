# Fuzzing #

Fuzzing is a technique of submitting lots of invalid or unexpected data to a target.

ZAP allows you to fuzz any request still using a built in set of payloads.
To fuzz a request string:


 *  Select a request in the Sites or History tab
 *  Highlight the string you wish to fuzz in the Request tab
 *  Right click in the Request tab and select 'Fuzz...'
 *  Select the Fuzz Category and one or more Fuzzers
 *  Press the Fuzz button
 *  The results will then be listed in the [Fuzzer tab][] select them to see the full requests and responses.

You can also search for strings in the fuzz results using the [Search tab][].

Fuzzing is configured using the [Options Fuzzing screen][]. Additional fuzzing files can be added via this screen or can be put manually into the "fuzzers" directory where ZAP was installed - they will then become available after restarting ZAP.

This functionality is based on code from the OWASP JBroFuzz project and includes files from the fuzzdb project.
Note that some fuzzdb files have been left out as they cause common anti virus scanners to flag them as containing viruses.
You can replace them (and upgrade fuzzdb) by downloading the latest version of fuzzdb and expanding it in the 'fuzzers' library.

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
   <td> <a href="HelpStartConceptsConcepts" rel="nofollow">Caracteristicas</a></td>
   <td>proporcionado por ZAP</td>
  </tr> 
 </tbody>
</table>


[Fuzzer tab]: HelpUiTabsFuzz
[Search tab]: HelpUiTabsSearch
[Options Fuzzing screen]: HelpUiDialogsOptionsFuzz