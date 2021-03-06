junos-sublime-pkg
=================

**Junos Config Syntax Highlighting for Sublime Text**  

### Description  
This is a Sublime Text 2/3 package to highlight the syntax for configurations on Juniper Junos (EX, MX, SRX) devices. It will work for configurations both in set mode and stanza form.  This syntax will automatically associate to a file with any of these extensions: `.conf`, and `.conf.1` through `.conf.49`. This accounts for the maximum number of rollback configs. To set the syntax for a file ending in any other extension, use the syntax menu in the bottom right, or press Cmd+Shift+P and type `Junos` to set the syntax for an open file.

### Installation
The easiest method of installation is using [Package Control](https://sublime.wbond.net/installation). Simply press Cmd+Shift+P and type `pcin` to get to `Package Control: Install Package`, then search for `Junos`.  

To install manually, simply download the lastest release [here](https://github.com/nprintz/junos-sublime-pkg/releases/latest), and drop the two `.tmLanguage` files into your `Packages/User` folder. The Packages folder can be found by going to the `Sublime Text 2` > `Preferences` > `Browse Packages` menu option. 

### Matches  
Name  | Description  
------|------------  
Comment Block or Annotation | For annotations in stanza mode: `/* Some Text */`  
Control Keywords | Highlights set/stanza mode keywords (`set`, `delete`, `activate`, `protect`, `inactive:`, `edit`, `show`, etc) as keyword.control.junos  
Interface names | Highlights interface names, and their corresponding unit numbers if in shortened format (ge-0/0/0.12)  
IPv4 and IPv6 addresses | All IP addresses get highlighted as a number  
Line Comment | Anything after a number sign, `#`, on a line  
MAC addresses | All MAC addresses get highlighted as a number  
Major Sections | Matches major sections of the config. For example, `system`, `interfaces`, `routing-instances`, are all  major categories (entity.name.function.junos)  
Minor Sections | Same as major sections, just for more of the less common sections of Junos config  
Policy Actions | Denial Actions (deny, reject, discard) are highlighted as invalid.illegal.junos. Acceptance actions (accept, permit) are highlighted as constant.language.junos.  
Routing Tables | Routing Table names are captured as a control keyword (inet.0, mytable.inet.2, mpls.0, etc)  
Strings | Anything between single- or double-quotes ( ' or " ) gets marked as a string. This also includes any word block after the keyword `description`, which may not be quoted  
Unit numbers | Unit numbers get highlighted as a number  
URLs | Any http://, https://, ftp://, tftp://, sftp://, or scp:// URL string will be highlighted as an operator. This includes IPv4 addresses (i.e. http://10.0.0.10/index.php)  
User defined arbitrary names | These get highlighted as a variable. Examples include the names of logical-systems, filters, prefix-lists, policies, NAT rules, security zones, policers, etc  

### Examples  
Examples with the built-in `Twilight` color scheme:

Set mode:  
![Set Mode](https://cloud.githubusercontent.com/assets/7231007/3803665/5fb3e326-1c1d-11e4-80fd-9b222f8a1abf.png)

Stanza mode:  
![Stanza Mode](https://cloud.githubusercontent.com/assets/7231007/3803687/81b640e0-1c1d-11e4-9dd6-f228e4c4275d.png)
