<h1 align="center" style="line-height: 50%;"><a data-from-md="" href="#"></a> <img src="images/image2.png" align="bottom" width="20" height="18" border="0" id="image2.png"> <span style="color: #3c78d8;"><u><b>RsyncBack</b></u></span><u> Godot Plugin Documentation </u></h1>
<h1 align="center" style="line-height: 50%;"><a data-from-md="" href="#"></a> <u>For Linux, MacOSX and Windows(*)</u></h1>
<h2 class="western"><a data-from-md="" href="#"></a><span style="color: #3c78d8;"><u><span style="background: #ffffff;"><a data-from-md="" href="#" title="">Quick Setup and Run Rsync</a>Back</span></u></span></h2>
<p><b>RsyncBack</b> is a plugin addon that allows you to create <u>fast</u> incremental <i>date-stamped</i> backups of your Godot project with a simple click of a button. For more detailed description see <a data-from-md="" href="#" title=""><span style="color: #1155cc;"><u>What is </u></span></a><a data-from-md="" href="#" title=""><span style="color: #1155cc;"><u><b>rsync</b></u></span></a></p>
<p>The following is a quick setup and run.</p>
<ol>
<li>
<p>Download and install the RsyncBack plugin from the Godot AssetLib of your project or clone directly from Github to the<u> ..</u><i>/addons </i>folder of your project.</p>
</li>
<li>
<p>Enable the <b>RsyncBack</b> plugin in Godot&rsquo;s Project Settings &gt; Plugins</p>
</li>
<li>
<p>To start a backup, click on the <img src=":/036370265f61449d9db65019f36c8398" align="bottom" width="16" height="16" border="0" id="Image1"> <span style="color: #ffffff;"><b><span style="background: #363d4a;">RsyncBack</span></b></span> link at the top of the editor to see the main screen. Here you select the rsync executable path, the backup path as well as some other options. The first time, you see a screen similar to <b>Fig 1</b></p>
</li>
</ol>
<p><img src=":/f3b8be1d5665474a8281697bd5200683" align="bottom" width="1908" height="965" border="0" id="image3.png"></p>
<p><b>Fig 1.</b></p>
<p>&nbsp;</p>
<ol start="4">
<li>
<p>If <b>rsync</b> is installed and in the $PATH environment (usually /usr/local/bin/ or /usr/bin/), the <span style="color: #ffffff;"><u><b><span style="background: #363d4a;">Rsync Cmd Path</span></b></u></span> label will show the path and version. If not you can manually choose it by clicking on <span style="color: #ffffff;"><u><b><span style="background: #363d4a;">Rsync Cmd Path</span></b></u></span> (see the section below <a data-from-md="" href="#"><span style="color: #1155cc;"><u>Finding the rsync command,</u></span></a>)</p>
</li>
<li>
<p>Click on <span style="color: #ffffff;"><u><b><span style="background: #363d4a;">Backup Destination Path</span></b></u></span> and pick a folder to use for backup. At this point you will see your screen changed similar to <b>Fig 2</b>. and the <span style="color: #ffffff;"><span style="background: #363d4a;">Run Rsync</span></span> button enabled.</p>
</li>
</ol>
<p><img src=":/5fe5171c2a27451bae1fa2dcdb98b8e1" align="bottom" width="1913" height="1047" border="0" id="image2.png"></p>
<p><b>Fig 2.</b></p>
<p>&nbsp;</p>
<ol start="6">
<li>
<p>Click on the <span style="color: #ffffff;"><u><b><span style="background: #363d4a;">Exclude File</span></b></u></span> and edit any patterns of files you want to exclude from backup. One line per pattern</p>
</li>
</ol>
<ul>
<li>
<p>Example. to exclude .godot, or any .git folders or any files with an extension of .import.<br><i>.godot</i> <br><i>.git*</i><br><i>*.import<br></i></p>
</li>
</ul>
<ol start="7">
<li>
<p>To start the backup, click on the <span style="color: #ffffff;"><b><span style="background: #363d4a;">Run Rsync</span></b></span> button and a popup report will show your project files backed up. The first backup is the longest as the complete project folder is backed up. See example <b>Fig 3</b>.</p>
</li>
</ol>
<p><img src=":/74747d20956a45b795be750f11ac247c" align="bottom" width="1913" height="1047" border="0" id="image6.png"> <b>Fig 3.</b></p>
<p>&nbsp;</p>
<ol start="8">
<li>
<p>Click on <span style="color: #ffffff;"><u><b><span style="background: #363d4a;">View Backup Destination Path</span></b></u></span> to review your backup and the log file. You should see the backup folders similar to <b>Fig 4</b></p>
</li>
<li>
<p><img src=":/767395ceedac475990d11168254fab86" align="bottom" width="555" height="515" border="0" id="image4.png"></p>
</li>
</ol>
<p><b>Fig 4</b></p>
<p><br><br></p>
<ol start="10">
<li>
<p>Go back to editing your project (e.g. clicking on Script). When ready to backup again click on <img src=":/036370265f61449d9db65019f36c8398" align="bottom" width="16" height="16" border="0" id="Image2"> <span style="color: #ffffff;"><b><span style="background: #363d4a;">RsyncBack</span></b></span> link to open the plugin screen and then click the <span style="color: #ffffff;"><b><span style="background: #363d4a;">Run Rsync</span></b></span> button. A new report will show only the files that were backed up.</p>
</li>
</ol>
<h2 class="western"><a data-from-md="" href="#"></a><a data-from-md="" href="#"><span style="color: #1155cc;"><span style="font-size: x-large;"><u>What is </u></span></span></a><a data-from-md="" href="#"><span style="color: #1155cc;"><span style="font-size: x-large;"><u><b>rsync</b></u></span></span></a><span style="color: #1155cc;"><span style="font-size: x-large;"><u>?</u></span></span></h2>
<p><b>Rsync</b> is one of the most popular and stable open source backup tools <u>included</u> with <i>Linux and MacOSX</i>. It is a terminal run tool with numerous options and arguments for backing up your computer folders incremental/differential, It has been battle tested for years now, is very reliable and has great community support. In its basic form it is a copy/sync tool, in that it copies files from source folder to a destination folder. Rsync backs up files using the native file system of your computer. It does not have its own compressed or proprietary database. You can easily use your <b>File Manager</b> to restore with drag and drop any backup folder or individual files. You can of course view them as regular files using your favorite File Manager. For Linux it could be <u>Dolphin/Nemo/etc</u> and Mac it could be <u>Finder</u>. Or it could be the command line using <u>ls</u>.</p>
<h2 class="western"><a data-from-md="" href="#"></a><a data-from-md="" href="#"><span style="color: #1155cc;"><u>What is the purpose </u></span></a><a data-from-md="" href="#"><span style="color: #1155cc;"><u><b>RsyncBack</b></u></span></a><a data-from-md="" href="#"><span style="color: #1155cc;"><u> Plugin</u></span></a>.</h2>
<p>The main usage for <b>RsyncBack </b>plugin is to be a Godot GUI front end and to make it simple to quickly setup and incrementally backup your project. Once installed and configured, the plugin can be run with just the press of a button to make date-stamped incremental backups of your project source files. Each date-stamped backup is its own folder, having the name <b>[YYYY-MM-DD[HH-MM-SS]</b>. In addition, it saves storage, because the destination will not contain files that have not been modified but rather a <u>hardlink</u> to the last one modified. When you look or use any of the backup folders, it will look like a complete backup of your source. More on this later.</p>
<h2 class="western"><a data-from-md="" href="#"></a>Finding the rsync command</h2>
<p>Before you begin, check that <span style="color: #6aa84f;"><b>rsync</b></span> is installed on your system. You can easily check from the command line by running the following terminal commands: $ <span style="color: #6aa84f;"><b>which rsync</b></span> to show you the default path or $ <span style="color: #6aa84f;"><b>whereis rsync</b></span> to check if there are more than one installed. RsyncBack requires version 3.2.4 or above. See <b>Fig A1</b>. To choose the desired rsync path, click on the label <span style="color: #ffffff;"><b><span style="background: #363d4a;">Rsync Cmd Path</span></b></span></p>
<p>&nbsp;</p>
<p><span style="font-family: Courier New, serif;"><span style="font-size: small;"><b>~$ which rsync<br></b></span></span><span style="font-family: Courier New, serif;"><span style="font-size: small;"><b>/usr/local/bin/rsync</b></span></span></p>
<p><span style="font-family: Courier New, serif;"><span style="font-size: small;"><b>~$ rsync -V<br></b></span></span><span style="font-family: Courier New, serif;"><span style="font-size: small;"><b>rsync version 3.2.7 protocol version 31<br></b></span></span><span style="font-family: Courier New, serif;"><span style="font-size: small;"><b>Copyright (C) 1996-2022 by Andrew Tridgell, Wayne Davison, and others.</b></span></span></p>
<p><span style="font-family: Courier New, serif;"><span style="font-size: small;"><b>.......</b></span></span></p>
<p><span style="font-family: Courier New, serif;"><span style="font-size: small;"><b>~$ whereis rsync<br></b></span></span><span style="font-family: Courier New, serif;"><span style="font-size: small;"><b>rsync: /usr/bin/rsync /usr/local/bin/rsync /usr/share/rsync /usr/share/man/man1/rsync.1.gz</b></span></span></p>
<p>&nbsp;</p>
<p><i><b>Fig A1</b></i></p>
<h2 class="western"><a data-from-md="" href="#"></a><u>**For Windows Users: Installing and running the rsync command.</u></h2>
<p>The RsyncBack addon is installed as usual. However you need to tell it where the rsync.exe command is located. To do that you would need to install MSYS2 which is a list of Linux commands that run as native to Windows. An open source consortium called MSYS2 created popular Linux commands that run natively on Windows. There is no need to install Linux to do that!</p>
<p>&nbsp;</p>
<p>From their documentation page at <a data-from-md="" href="https://www.msys2.org/"><span style="color: #1155cc;"><u>https://www.msys2.org</u></span></a>/:</p>
<ul>
<li>
<p><span style="color: #3a3a3a;"><span style="font-family: Roboto, serif;"><span style="font-size: small;"><i><b><span style="background: #fafafa;">MSYS2</span></b></i></span></span></span><span style="color: #3a3a3a;"><span style="font-family: Roboto, serif;"><span style="font-size: small;"><i><span style="background: #fafafa;"> is a collection of tools and libraries providing you with an easy-to-use environment for building, installing and running native Windows software.</span></i></span></span></span></p>
</li>
</ul>
<p>&nbsp;</p>
<p><span style="color: #3a3a3a;"><span style="font-family: Roboto, serif;"><span style="font-size: small;"><span style="background: #fafafa;">Additional docs here: </span></span></span></span><a data-from-md="" href="https://www.msys2.org/docs/what-is-msys2/"><span style="color: #1155cc;"><span style="font-family: Roboto, serif;"><span style="font-size: small;"><u><span style="background: #fafafa;">https://www.msys2.org/docs/what-is-msys2/</span></u></span></span></span></a></p>
<p>&nbsp;</p>
<p><span style="color: #3a3a3a;"><span style="font-family: Roboto, serif;"><span style="font-size: small;"><span style="background: #fafafa;">On your Windows box, follow this link </span></span></span></span><a data-from-md="" href="https://www.msys2.org/#installation"><span style="color: #1155cc;"><span style="font-size: medium;"><u><span style="background: #fafafa;">https://www.msys2.org/#installation:</span></u></span></span></a><span style="color: #3a3a3a;"><span style="font-family: Roboto, serif;"><span style="font-size: small;"><span style="background: #fafafa;"> and the instructions to install the msys2 executable. </span></span></span></span></p>
<p><span style="color: #3a3a3a;"><span style="font-family: Roboto, serif;"><span style="font-size: small;"><span style="background: #fafafa;">This will create a native windows folder followed by the path to Linux exe commands. </span></span></span></span></p>
<p><span style="color: #3a3a3a;"><span style="font-family: Roboto, serif;"><span style="font-size: small;"><span style="background: #fafafa;">You can then install rsync from the terminal that opens up as follows:</span></span></span></span></p>
<p>&nbsp;</p>
<p><span style="color: #0c0d0e;"><span style="font-size: medium;"><span style="background: #fafafa;">rsync.exe can be installed via </span></span></span></p>
<p><span style="color: #0c0d0e;"><span style="font-family: Courier New, serif;"><span style="font-size: small;"><span style="background: #f6f6f6;">pacman -S rsync</span></span></span></span></p>
<p><span style="color: #0c0d0e;"><span style="font-size: medium;"><span style="background: #fafafa;">It then runs natively under Windows as </span></span></span></p>
<p><span style="color: #0c0d0e;"><span style="font-family: Courier New, serif;"><span style="font-size: small;"><span style="background: #e3e6e8;">c:/msys64/usr/bin/rsync.exe</span></span></span></span></p>
<p><span style="color: #0c0d0e;"><span style="font-size: medium;"><span style="background: #fafafa;">So in this case, you would choose the path above the RsyncBack screen as the path for rsync. </span></span></span></p>
<p><span style="color: #0c0d0e;"><span style="font-size: medium;"><span style="background: #fafafa;">Note: There are a few articles online on how to install MSYS2 and rsync. </span></span></span></p>
<p><span style="color: #0c0d0e;"><span style="font-size: medium;"><span style="background: #fafafa;">In fact here is one explaining how to do it if you are using Git. </span></span></span><a data-from-md="" href="https://tlundberg.com/installing-rsync-on-windows"><span style="color: #1155cc;"><span style="font-size: medium;"><u><span style="background: #fafafa;">https://tlundberg.com/installing-rsync-on-windows</span></u></span></span></a></p>
<p><span style="color: #0c0d0e;"><span style="font-size: medium;"><span style="background: #fafafa;">From the article: </span></span></span><span style="color: #111111;"><span style="font-family: Roboto, serif;"><span style="font-size: large;"><span style="background: #ffffff;">If you didn't already know, Git for Windows and its Git Bash environment is built using </span></span></span></span><a data-from-md="" href="http://msys2.org/"><span style="color: #111111;"><span style="font-family: Roboto, serif;"><span style="font-size: large;"><u><span style="background: #ffffff;">msys2</span></u></span></span></span></a><span style="color: #111111;"><span style="font-family: Roboto, serif;"><span style="font-size: large;"><span style="background: #ffffff;">, but it doesn't include all the binaries from that project.</span></span></span></span></p>
<h2 class="western"><a data-from-md="" href="#"></a><u>Backup Folders Layout and Restore</u></h2>
<p>As we said before, <b>RsyncBack</b> creates an rsync command that incrementally backs up your project to your chosen backup folder. The backup folder will always be called <b>&lt;project name folder&gt;-rsync</b>. Inside this folder the backups are copied with the name [YYYY-MM-DD][HH_MM_SS]. Also the backup folder includes another folder called logfiles, where each backup&rsquo;s report is kept. See <b>Fig A4</b></p>
<p>&nbsp;</p>
<p>The backup folders are exact ordinary folders of your project. To restore, you can copy or view using your system's File Manager.</p>
<p>&nbsp;</p>
<p><img src=":/767395ceedac475990d11168254fab86" align="bottom" width="544" height="638" border="0" id="image5.png"></p>
<p><b>Fig A4.</b></p>
<p>&nbsp;</p>
<p>Even though it may look to you that in your latest folder the complete project was copied, in fact what you are seeing is an image copy of the previous backup overwritten by the files that are different. This is the power of Linux/Mac file system and it is all done in the background using hardlinks. It allows for efficient disk storage and speed. Rsync does that by comparing your source folder (ie your project folder) with the latest backup then copies the changed files to the destination. The unchanged are hardlinked. The option that does this is <span style="font-family: Courier New, serif;"><span style="font-size: small;"><b>--link-dest=&rdquo;your/last/backup/folder&rdquo; See example command below.</b></span></span></p>
<p>&nbsp;</p>
<p>In fact every file you create is a hardlink to an <b>inode</b>. If you copy that file to another folder it does not duplicate it. It simply makes a directory entry pointing to what is called an <b>inode</b>. Inodes are beyond the scope of this document, but if you are curious about inodes read the short tutorial <a data-from-md="" href="https://digitalis.io/blog/linux/incremental-backups-with-rsync-and-hard-links/"><span style="color: #1155cc;"><u>rsync incremental and hard links backup concepts</u></span></a></p>
<h2 class="western"><a data-from-md="" href="#"></a><u>Customizing the Defaults of RsynBack.</u></h2>
<p>&nbsp;</p>
<p>A new install of RsyncBack initially reads the choices from a resource file called <i><b>config.tres</b></i>. The user then makes the selections and runs the backup. This config.tres can be manually edited in the Inspector. The simplest way to do that is to click on the Config File label link and select Edit In Inspector (Make sure Inspector is showing in the dock). The Godot Inspector will load the <i><b>config.tres</b></i> resource file and allow you to make the changes manually and save the config file. <u>Make sure you reload the plugin.</u></p>
<p>&nbsp;</p>
<p>Hover over each of the config.tres properties and read the tooltip for more info. The Rsync Arguments Template is where you would customize further the rsync command options.</p>
<p>It looks similar to this:</p>
<p>&nbsp;</p>
<p><code spellcheck="false">{dry_run_argument} -avih --mkpath --stats \</code><br><code spellcheck="false">--out-format="%M %15'l %5f" \</code><br><code spellcheck="false">--exclude-from="{exclude_file_path}" \</code><br><code spellcheck="false">--link-dest="{dest_path}/{project_name}/{prev_backup}" \</code><br><code spellcheck="false">--log-file-format="%M %15'l %5f" \</code><br><code spellcheck="false">--log-file="{log_file_path}/{current_datetime}{log_file_suffix}" \</code><br><code spellcheck="false">"{source_path}" \</code><br><code spellcheck="false">"{dest_path}/{project_name}/{current_datetime}"</code></p>
<p>&nbsp;</p>
<p>The curlies {} are properties replaced by RsyncBack when you run the project. In effect the above becomes something like this command which is what executes.</p>
<p>&nbsp;</p>
<p><strong><code spellcheck="false">/usr/local/bin/rsync -avih --mkpath --stats \</code></strong><br><strong><code spellcheck="false">--out-format="%M %15'l %5f" \</code></strong><br><strong><code spellcheck="false">--exclude-from="/home/user1/godot/tps-demo/addons/rsyncback/exclude.txt" \</code></strong><br><strong><code spellcheck="false">--link-dest="/home/user1/myback/tps-demo-rsync/[2024-10-16][13_22_37]" \</code></strong><br><strong><code spellcheck="false">--log-file-format="%M %15'l %5f" \</code></strong><br><strong><code spellcheck="false">--log-file="/home/user1/myback/tps-demo-rsync/logfiles/[2024-10-18][17_07_35]_log.txt" \</code></strong><br><strong><code spellcheck="false">"/home/user1/godot/tps-demo/" \</code></strong><br><strong><code spellcheck="false">"/home/user1/myback/tps-demo-rsync/[2024-10-18][17_07_35]"</code></strong></p>
<p>&nbsp;</p>
<p>In fact you will see this command in the Rsync Command window. You can click and copy it to the clipboard and run it directly in the command line if you wish!</p>
<p>&nbsp;</p>
<p>Notice the rsync command is added from the path you chose. Also <code spellcheck="false"><span style="font-family: Courier New, serif;"><span style="font-size: small;"><b>{dry_run_argument}</b></span></span></code>is not used in this case since we didn&rsquo;t check the box. Dry run does not make a backup but simply executes to see if your command is ok. It is always reset back.</p>
<p>&nbsp;</p>
<p>You can modify this template anyway you want. E.g. add a remote backup ssh keyfile or add <i>&ndash;delete</i> option. Study up on rsync if you plan to customize the template.</p>
<h2 class="western"><a data-from-md="" href="#"></a><u>References:</u></h2>
<p>&nbsp;</p>
<center>
<table width="805" cellpadding="7" cellspacing="0" style="break-before: auto; break-after: auto; height: 294.375px; border-collapse: collapse; width: 805px; border-width: 1pt; border-spacing: 0px; border-style: dashed;" border="1"><colgroup><col width="245"> <col width="530"> </colgroup>
<tbody>
<tr valign="top" style="height: 54.3958px;">
<td width="245" style="border: 1pt solid rgb(0, 0, 0); padding: 0.01px; height: 54.3958px;">
<p>Official Website</p>
</td>
<td width="530" style="border: 1pt solid rgb(0, 0, 0); padding: 0.01px; height: 54.3958px;">
<p><a data-from-md="" href="https://rsync.samba.org/" title=""><span style="color: #1155cc;"><u>https://rsync.samba.org</u></span></a></p>
</td>
</tr>
<tr valign="top" style="height: 54.3958px;">
<td width="245" style="border: 1pt solid rgb(0, 0, 0); padding: 0.01px; height: 54.3958px;">
<p>rsync man page</p>
</td>
<td width="530" style="border: 1pt solid rgb(0, 0, 0); padding: 0.01px; height: 54.3958px;">
<p><a data-from-md="" href="https://ss64.com/bash/rsync.html" title=""><span style="color: #1155cc;"><u>https://ss64.com/bash/rsync.html</u></span></a></p>
</td>
</tr>
<tr valign="top" style="height: 54.3958px;">
<td width="245" style="border: 1pt solid rgb(0, 0, 0); padding: 0.01px; height: 54.3958px;">
<p>Command line tutorial/Examples</p>
</td>
<td width="530" style="border: 1pt solid rgb(0, 0, 0); padding: 0.01px; height: 54.3958px;">
<p><a data-from-md="" href="https://www.geeksforgeeks.org/rsync-command-in-linux-with-examples/" title=""><span style="color: #1155cc;"><u>https://www.geeksforgeeks.org/rsync-command-in-linux-with-examples/</u></span></a></p>
</td>
</tr>
<tr valign="top" style="height: 76.7917px;">
<td width="245" style="border: 1pt solid rgb(0, 0, 0); padding: 0.01px; height: 76.7917px;">
<p>rsync incremental and hard links backup concepts</p>
</td>
<td width="530" style="border: 1pt solid rgb(0, 0, 0); padding: 0.01px; height: 76.7917px;">
<p><a data-from-md="" href="https://digitalis.io/blog/linux/incremental-backups-with-rsync-and-hard-links/" title=""><span style="color: #1155cc;"><u>https://digitalis.io/blog/linux/incremental-backups-with-rsync-and-hard-links/</u></span></a></p>
</td>
</tr>
<tr valign="top" style="height: 54.3958px;">
<td width="245" style="border: 1pt solid rgb(0, 0, 0); padding: 0.01px; height: 54.3958px;">
<p>Installing rsync for Windows.</p>
</td>
<td width="530" style="border: 1pt solid rgb(0, 0, 0); padding: 0.01px; height: 54.3958px;">
<p><a data-from-md="" href="https://www.msys2.org/"><span style="color: #1155cc;"><u>https://www.msys2.org/</u></span></a></p>
</td>
</tr>
</tbody>
</table>
</center>
<div title="footer">
<p>&nbsp;</p>
</div>