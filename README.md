pasv-agrsv.py
===========

Passive recon / OSINT automation script:

- Runs passive recon tools specified in config file given a TLD
- Extracts email addresses, IP addresses, and DNS names from tool output using regex
- Queries various OSINT sites specified in config file for TLD and saves site in specified format
- Runs additional recon tools and website queries on IPs and DNS names found from initial TLD analysis

---------------------------------------------------------------------------------------------------
##Notes

All scan parameters are pulled from config files so multiple configurations can be developed and specified with the -c flag.
An example config file (default.example) is included and will be copied into the default path (default.cfg) upon initial launch. 

Script tested on Kali Linux as well as OSX and should function on UNIX-based systems with required dependencies.

---------------------------------------------------------------------------------------------------
##Dependencies

###Python Module Dependencies:
- none at this time

###Binary Dependencies (all installed on Kali Linux by default):
- cutycapt

---------------------------------------------------------------------------------------------------
##Todo

- HTML index page to summarize all output
- Subdirectory specifications in config file for tool output
- Direct output of tool output to file instead of command line output where supported (e.g. fierce)
- Catch keyboard interrupts and exit subprocesses without killing entire script
- Implement regex tool output cleanup (see example in metasploit email enum section)
- Add aggressive (non-passive) command section (for example, discover & screenshot / spider discovered websites associated with TLD)

---------------------------------------------------------------------------------------------------

Copyright 2015

Matthew C. Jones, CPA, CISA, OSCP

IS Audits & Consulting, LLC - <http://www.isaudits.com/>

TJS Deemer Dana LLP - <http://www.tjsdd.com/>

Concept based upon functionality observed in the OSINT portion of the Kali Discover script by leebaird: <https://github.com/leebaird/discover/>

---------------------------------------------------------------------------------------------------

This program is free software: you can redistribute it and/or modify it under the terms of the GNU General Public License as published by the Free Software Foundation, either version 3 of the License, or (at your option) any later version.

This program is distributed in the hope that it will be useful, but WITHOUT ANY WARRANTY; without even the implied warranty of MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE. See the GNU General Public License for more details.

You should have received a copy of the GNU General Public License along with this program. If not, see <http://www.gnu.org/licenses/>.