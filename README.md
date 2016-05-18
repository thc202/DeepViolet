<h1>DeepViolet, SSL/TLS Introspection Tool</h1><br/>
==========
<p/>
DeepViolet is a Java tool for introspection of SSL\TLS sessions.  DeepViolet can be run from the **command line**, **GUI desktop application**, or you can include the **DeepViolet API** within your own Java projects.  The tool was originally inspired by the work of Qualys SSL Labs and Ivan Ristić.  Original blog article post describing this project, http://www.securitycurmudgeon.com/2014/07/ssltls-introspection.html<br/>
<p/>
<b>BENEFITS</b>
This tool helps you understand state of X.509 certificates run on servers.  Some ideas you may find useful.
<ul>
<li>Certificates that don't chain to trusted roots</li>
<li>Examine trust relationships, flag self-signed roots, etc</li>
<li>Assess revocation status</li>
<li>Certificates signed with weak signing algorithms</li>
<li>Weak cipher suits on the web server</li>
<li>Warn on certificates with approaching expiration</li>
<li>View X.509 certificate metadata</li>
<li>Easily visualize X.509 trust chains</li>
<li>Information to support forensics</li>
</ul>
<p/>
Use certificate metadata along with your own shell scripts in new and creative ways.
<p/>
<b>INSTALLATION & USE INSTRUCTIONS</b>, 1) make sure Java 8+ installed, 2) download dvUI.jar to your desktop from the Release tab near the top of the screen, double-click to run 3) alternatively, download dvCMD.jar and run in your shell scripts.  
<p/>
<b>CAUTION</b>, use care to review reports for sensitive information prior to distribution or posting to the Internet.
<p/>
<b>RUNNING FROM DESKTOP</b>, Simply double-click on the dvGUI.jar on your desktop or launch the desktop application from the command line.  Note: there are no command line options when staring the DeepViolet GUI from the command line.<br/>
<code>java -jar dvUI.jar</code>
<p/>
![deepviolet-git](https://cloud.githubusercontent.com/assets/8450615/14919921/e04f22c4-0ddf-11e6-9d16-2b15e1a57c37.jpg)
<p/>
<b>RUNNING FROM COMMAND LINE</b>, The following command line executes a scan against www.github.com and includes all reporting sections.  The output of the report is the same as the sample included in this file.<br/>
<code>java -jar dvCMD.jar -serverurl https://www.github.com/</code>
<p/>
The following command line produces the same report but specifies each report section individually.  Including less sections increases the speed of the scan.<br/>
<code>java -jar dvCMD.jar -serverurl https://www.github.com/ -s thrcisn</code>
<p/>
The following command line produces exports the certificate on www.github.com to a PEM encoded file for offline use.
<code>java -jar dvCMD.jar -serverurl https://www.github.com/ -wc ~/milton/DeepViolet/github.pem</code><br/>
<p/>
Conversely the following command line reads a PEM encoded certificate and generates a report ('s' option) by default.  Note: the -rc option is mututually exclusive with other options.  The primary reason is that -rc is an offline reporting function.  Whereas other options are applicable for online servers.<br/>
<code>java -jar dvCMD.jar -rc ~/milton/DeepViolet/github.pem</code>
<p/>
If you need some help while your in the shell, command line help is available.<br/>
<code> java -jar dvCMD.jar -h</code>
<p/>
The previous help command produces output like the following.<br/>
![dvcmd-snapshot](https://cloud.githubusercontent.com/assets/8450615/15344407/8209d2ba-1c5b-11e6-9321-3397ba35359d.png)
<p/>
<b>FEATURE REQUESTS & BUG REPORTS</b>, [See DeepViolet Wiki](https://github.com/spoofzu/DeepViolet/wiki)
<p/>
<b>WANT TO HELP?</b>, want to help make this into a full featured project?  See the following GitHub document for more details, [Contributing to Open Source on GitHub](https://guides.github.com/activities/contributing-to-open-source/). 
<p/>
<i>This program is provided for educational purposes.  Use at your own risk.<br/>
This project leverages the works of other open source community projects.  This program is only available in US English.</i>
