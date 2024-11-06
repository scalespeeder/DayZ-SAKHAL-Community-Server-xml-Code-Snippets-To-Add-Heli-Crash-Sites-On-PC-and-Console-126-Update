1.26 Sakhal Code Snippets To Bring Heli Crashes To The Winter Map Files README

Instructionss & code snippets to bring heli-crashes to Sakhal, on PC & PlayStation & Xbox Console COmmunity Servers..

A maximum of six heli crashes will spawn at a possible 21 locations.

Limited Testing on PC SAKHAL Local PC Server & Xbox Community Server Version 1.26 NOV 2024.

Edited by @scalespeeder. Please report bugs & errors to scalespeeder@gmail.com with screenshots.

TERMS OF USE
THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND,
EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS
OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN
AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH
THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.

------

INSTRUCTIONS

Stop your server & make back-ups of the files we're about to edit, events.xml & cfgeventspawns.xml.

It's best to download files & edit locally on your PC if you can.

Check all edits with an online XML validator: https://www.xmlvalidation.com/

Navigate to & open the events.xml file on your sever ( DayZServer\mpmissions\dayzOffline.sakhal\db )

Search for the StaticHeliCrash event, and edit the   <active>0</active> line to   <active>1</active>.

If you'd like to add more heli crashes, edit the    <nominal>3</nominal> line to    <nominal>6</nominal>

So the whole event will look like this:

<event name="StaticHeliCrash">
        <nominal>6</nominal><!--vanilla is 3 -->
        <min>0</min>
        <max>0</max>
        <lifetime>2100</lifetime>
        <restock>0</restock>
        <saferadius>1000</saferadius>
        <distanceradius>1000</distanceradius>
        <cleanupradius>1000</cleanupradius>
        <secondary>InfectedArmy</secondary>
        <flags deletable="1" init_random="0" remove_damaged="0"/>
        <position>fixed</position>
        <limit>child</limit>
        <active>1</active>
        <children>
            <child lootmax="15" lootmin="10" max="3" min="1" type="Wreck_Mi8_Crashed"/>
        </children>
    </event>
	

Save your file & validate to check for errors. Upload if OK.

Navigate to & open the cfgeventspawns.xml file on your sever ( DayZServer\mpmissions\dayzOffline.sakhal )

At the bottom of the file, above </eventposdef> paste the following XML code snippet:

<event name="StaticHeliCrash">
		<zone smin="1" smax="3" dmin="3" dmax="5" r="45" />
		<pos x="13009" y="7.668" z="5390.47" a="0"/>
		<pos x="12181.8" y="10.5047" z="2287.7" a="0"/>
		<pos x="8729.94" y="3.78844" z="1295.32" a="0"/>
		<pos x="8711.43" y="5.75681" z="5034.09" a="0"/>
		<pos x="6366.58" y="12.2439" z="4430.06" a="0"/>
		<pos x="5304.69" y="21.8725" z="3630.68" a="0"/>
		<pos x="5861.97" y="4.0401" z="2122.8" a="0"/>
		<pos x="2342.29" y="13.7784" z="3496.86" a="0"/>
		<pos x="3388.87" y="34.7114" z="2744.99" a="0"/>
		<pos x="1539.79" y="6.67053" z="1016.66" a="0"/>
		<pos x="1253.87" y="3.97934" z="2973.21" a="0"/>
		<pos x="2224.19" y="10.2983" z="6380.83" a="0"/>
		<pos x="7150.8" y="4.54445" z="7186.26" a="0"/>
		<pos x="7232.19" y="4.49401" z="7559.74" a="0"/>
		<pos x="10455.4" y="9.58835" z="6868.15" a="0"/>
		<pos x="13559.3" y="33.7447" z="8300.2" a="0"/>
		<pos x="5865.56" y="45.4615" z="9520.65" a="0"/>
		<pos x="8359.31" y="19.2851" z="9933.45" a="0"/>
		<pos x="11214.9" y="368.423" z="8682.2" a="0"/>
		<pos x="5579.99" y="7.68263" z="11322.1" a="0"/>
		<pos x="11816" y="340.969" z="11119.9" a="0"/>
		</event>
		
 Save your file & validate to check for errors. Upload if OK.
 
 Restart your server & enjoy!
 
Thanks, Rob.



