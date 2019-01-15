# list-nodes
List nodes in CSV format, grouped by App, Tier

In its initial form, this Python script extracts all Applications, Tiers and Nodes from a Controller and produces a CSV output with the form:
<pre>
<code>
Application,Tier,AgentType,Node
</code>
</pre>

You can then import this output into Excel and build a pivot table to see how many nodes you have per type of agent, per application, etc.

### Usage
```
Usage: list-nodes.py [options] controller username password

Options:
  -h, --help            show this help message and exit
  -o FILE, --outfile=FILE
                        write report to FILE.  If not provided, output to
                        STDOUT
  -p PORT, --port=PORT  Controller port
  -s, --ssl             Use SSL
```
Notice that if you do not provide an output file, the results will be sent to STDOUT, along with the names of the applications as they are being processed.  So copying this into a file afterward will have a different result than if you sent the results directly into a file.
### Pre-requisites
list-nodes is written in Python3 and uses the <code>requests</code> module.
