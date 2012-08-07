cacti_game_server_scripts_and_xml
=================================

scripts and xml to monitor game servers via cacti

this is a import of the original files created by hangy and posted by him to the cacti forums (http://forums.cacti.net/viewtopic.php?p=70958#p70958)








ORIGINAL README BY hangy
========================

About
-----
The idea and the graphs were taken from a thread on the Cacti forums [1].
However, unlike the original version posted in that thread, this script doesn't
use different techniques (Perl + PHP) but just PHP (PHP4 and PHP5 should work IMHO),
utilizing the excellent game classes of Phgstats 0.6.9 [2].

[1] http://forums.cacti.net/about3735.html
[2] http://phgstats.sourceforge.net

Installation
------------
1. Copy all files from the "scripts" folder into your Cacti's "scripts" folder
   which could be /var/www/cacti/scripts/.
   However, be sure to keep that folder structure intact, *.class.php files should
   be in scripts/classes/ and gameserver.php should be in scripts/

2. Import all graph templates
     cacti_graph_template_game_server_status_players.xml
     cacti_graph_template_game_server_status_players_without_maximum.xml
     cacti_graph_template_game_server_status_players_per_server.xml
   into your Cacti. (Use Cacti's "Import Templates" page for that!)
   
3. Import the data template
     cacti_data_template_game_server_status.xml
   into your Cacti. (Use Cacti's "Import Templates" page for that!)
   
You're done, you should now be able to create a new graph using those templates!


Supported games
(as of Phgstats 0.6.9)
----------------------
aa:			America's Army
atron:			Armagetronad
bf:			Battlefield 1942
bfv:			Battlefield Vietnam
bf2:			Battlefield 2
cod:			Call of Duty
cod2:			Call of Duty 2
d3:			Doom 3
descent3:		Descent 3
des3gs:			Descent 3 (Gamespy)
et:			Enemy Territory
fear:			FEAR
halo:			HALO
hd2:			Hidden & Dangerous 2
hl_old:			Half-Life / CS OLD
hl:			Half-Life / CS
hl2:			Half-Life 2 / CS:S
jedi:			Jedi Knight: Jedi Academy
jedi2:			Jedi Knight II
mohaa:			Medal of Honor
nolf:			No One Lives Forever
pk:			Painkiller
ro:			Red Orchestra
rune:			Rune
rtcw:			Return to Castle Wolfenstein
sof2:			Soldier of Fortune 2
swat:			SWAT 4
ts:			Teamspeak
ut:			Unreal Tournament
ut2003:			Unreal Torunament 2003
ut2004:			Unreal Tournament 2004
qw:			Quakeworld
q1:			Quake 1
q2:			Quake 2
q3:			Quake 3
q4:			Quake 4
warsow:			Warsow

License
-------
The rights for the original templates and the phgstats classes belong
to their original authors! The rest is available as "Public Domain" good.

/*
* THIS SOFTWARE IS PROVIDED BY THE COPYRIGHT HOLDERS AND CONTRIBUTORS
* "AS IS" AND ANY EXPRESS OR IMPLIED WARRANTIES, INCLUDING, BUT NOT
* LIMITED TO, THE IMPLIED WARRANTIES OF MERCHANTABILITY AND FITNESS
* FOR A PARTICULAR PURPOSE ARE DISCLAIMED. IN NO EVENT SHALL THE
* COPYRIGHT OWNER OR CONTRIBUTORS BE LIABLE FOR ANY DIRECT, INDIRECT,
* INCIDENTAL, SPECIAL, EXEMPLARY, OR CONSEQUENTIAL DAMAGES (INCLUDING,
* BUT NOT LIMITED TO, PROCUREMENT OF SUBSTITUTE GOODS OR SERVICES;
* LOSS OF USE, DATA, OR PROFITS; OR BUSINESS INTERRUPTION) HOWEVER
* CAUSED AND ON ANY THEORY OF LIABILITY, WHETHER IN CONTRACT, STRICT
* LIABILITY, OR TORT (INCLUDING NEGLIGENCE OR OTHERWISE) ARISING IN
* ANY WAY OUT OF THE USE OF THIS SOFTWARE, EVEN IF ADVISED OF THE
* POSSIBILITY OF SUCH DAMAGE.
*/
