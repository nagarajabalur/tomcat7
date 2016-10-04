tomcat Cookbook
===============

Requirements
------------
Yum Based Linux (RHEL, Centos, Fedora, Amazon)

#### Packages
OpenJDK-1.7.0
Tomcat7

Attributes
----------

#### tomcat::default
<table>
  <tr>
    <th>Key</th>
    <th>Type</th>
    <th>Description</th>
    <th>Default</th>
  </tr>
  <tr>
    <td><tt>['tomcat']['port']</tt></td>
    <td>Int</td>
    <td>What port for tomcat to listen on</td>
    <td><tt>8080</tt></td>
  </tr>
  <tr>
    <td><tt>['tomcat']['proxy_port']</tt></td>
    <td>Int</td>
    <td>Tomcat Proxy Port</td>
    <td><tt>nil</tt></td>
  </tr>
  <tr>
    <td><tt>['tomcat']['max_threads']</tt></td>
    <td>Int</td>
    <td>Tomcat's Max Threads</td>
    <td><tt>nil</tt></td>
  </tr>
  <tr>
    <td><tt>['tomcat']['ssl_proxy_port']</tt></td>
    <td>Int</td>
    <td>Tomcat's SSL Proxy Port</td>
    <td><tt>nil</tt></td>
  </tr>
  <tr>
    <td><tt>['tomcat']['catalina_options']</tt></td>
    <td>String</td>
    <td>Tomcat's Catalina Options</td>
    <td><tt></tt></td>
  </tr>
  <tr>
    <td><tt>['tomcat']['java_options']</tt></td>
    <td>String</td>
    <td>Options to the JVM</td>
    <td><tt>-Xmx128M -Djava.awt.headless=true</tt></td>
  </tr>

  <tr>
    <td><tt>['tomcat']['extras']['jmx']</tt></td>
    <td>Boolean</td>
    <td>Add the JMX Jar to the tomcat bin</td>
    <td><tt>True</tt></td>
  </tr>
  <tr>
    <td><tt>['tomcat']['valves']</tt></td>
    <td>List</td>
    <td>A list of Hashes describing valves to put into the server.xml</td>
    <td></td>
  </tr>
  <tr>
    <td><tt>['tomcat']['libs']</tt></td>
    <td>List</td>
    <td>A list of Hashes describing artifacts to retreive from Nexus for the Tomcat lib directory</td>
    <td></td>
  </tr>
</table>

Usage
-----
#### tomcat::default

e.g.
Just include `tomcat` in your node's `run_list`:

:


```json
{
  "name":"my_node",
  "run_list": [
    "recipe[tomcat]"
  ]
}
```
