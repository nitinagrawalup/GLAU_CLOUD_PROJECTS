# Title: Performance benchmarking of Type II Hypervisors.

<strong>Abstract:</strong>

<p>The virtualization is carried out by the software layer called as the Hypervisor or Virtual Machine Monitor (VMM). Hypervisor is widely used in cloud datacenters. Benchmark is the measurement of best practice performance. Benchmarking is very essential term for the discovery of the best performance given by the particular system. Benchmarking can provides you the external references and the best practices on which to base your evaluations and to design your system processes which can be very useful in finding the gaps in the system to achieve the desired performance. Your target hypervisors are Virtual Box, VMWare workstation as an hosted hypervisors and KVM. Performance analysis of network, cpu, ram, I/O need to carried out..</p>

<strong>Intended Outcome:</strong>
<br/>
<p>Analyzing the performance of the different hypervisors with the similar hardware configuration and operating system. </p>

<strong>Hardware Requirements:</strong>
<br/>
<ul>
	<li>
		Personal Computer with minimum 4GB RAM and 4 cores with VT Enabled. 
	</li>
</ul>
<strong>Software Requirements:</strong>
<br/>
<ul>
	<li>
		Linux OS (Any Open Source )
	</li> 
	<li>
		Stress and Glances tool(Open Source)
	</li> 
	<li>
		VmWare Workstation (Free Version) and Virtualbox latest version
	</li> 
</ul>
<hr/>
# Virtualization 
<p>
	Virtualization is technology that allows you to create multiple simulated environments or dedicated resources from a single, physical hardware system. Software called a hypervisor connects directly to that hardware and allows you to split 1 system into separate, distinct, and secure environments known as virtual machines (VMs). These VMs rely on the hypervisor’s ability to separate the machine’s resources from the hardware and distribute them appropriately. Virtualization helps you get the most value from previous investments.
</p>
<p>
	The physical hardware, equipped with a hypervisor, is called the host, while the many VMs that use its resources are guests. These guests treat computing resources—like CPU, memory, and storage—as a pool of resources that can easily be relocated. Operators can control virtual instances of CPU, memory, storage, and other resources, so guests receive the resources they need when they need them.
</p>
<p>
	In more practical terms, imagine you have 3 physical servers with individual dedicated purposes. One is a mail server, another is a web server, and the last one runs internal legacy applications. Each server is being used at about 30% capacity—just a fraction of their running potential. But since the legacy apps remain important to your internal operations, you have to keep them and the third server that hosts them, right?
</p>
<br/>
	<img src="img/1.png">
<br/>
<p>
	Traditionally, yes. It was often easier and more reliable to run individual tasks on individual servers: 1 server, 1 operating system, 1 task. It wasn’t easy to give 1 server multiple brains. But with virtualization, you can split the mail server into 2 unique ones that can handle independent tasks so the legacy apps can be migrated. It’s the same hardware, you’re just using more of it more efficiently
</p>
<br/>
	<img src="img/2.png">
<br/>
<p>
	Keeping security in mind, you could split the first server again so it could handle another task—increasing its use from 30%, to 60%, to 90%. Once you do that, the now empty servers could be reused for other tasks or retired altogether to reduce cooling and maintenance costs.
</p>
<br/>
<h2>How does virtualization work?</h2>
<p>
	Software called hypervisors separate the physical resources from the virtual environments—the things that need those resources. Hypervisors can sit on top of an operating system (like on a laptop) or be installed directly onto hardware (like a server), which is how most enterprises virtualize. Hypervisors take your physical resources and divide them up so that virtual environments can use them.
</p>
<br/>
	<img src ="img/3.png">
<br/>
<p>
	Resources are partitioned as needed from the physical environment to the many virtual environments. Users interact with and run computations within the virtual environment (typically called a guest machine or virtual machine). The virtual machine functions as a single data file. And like any digital file, it can be moved from one computer to another, opened in either one, and be expected to work the same.
</p>
<p>
	When the virtual environment is running and a user or program issues an instruction that requires additional resources from the physical environment, the hypervisor relays the request to the physical system and caches the changes—which all happens at close to native speed (particularly if the request is sent through an open source hypervisor based on KVM, the Kernel-based Virtual Machine).
</p>
<h2> Types of Virtualization</h2>
<strong>Data virtualization</strong>
<br/>
	<img src="img/4.png">
<br/>
<p>
	Data that’s spread all over can be consolidated into a single source. Data virtualization allows companies to treat data as a dynamic supply—providing processing capabilities that can bring together data from multiple sources, easily accommodate new data sources, and transform data according to user needs. Data virtualization tools sit in front of multiple data sources and allows them to be treated as single source, delivering the needed data—in the required form—at the right time to any application or user.
</p>
<strong>Desktop virtualization</strong>
<br/>
	<img src="img/5.png">
<br/>
<p>
	Easily confused with operating system virtualization—which allows you to deploy multiple operating systems on a single machine—desktop virtualization allows a central administrator (or automated administration tool) to deploy simulated desktop environments to hundreds of physical machines at once. Unlike traditional desktop environments that are physically installed, configured, and updated on each machine, desktop virtualization allows admins to perform mass configurations, updates, and security checks on all virtual desktops
</p>
<strong>Server virtualization</strong>
<br/>
	<img src="img/6.png">
<br/>
<p>
	Servers are computers designed to process a high volume of specific tasks really well so other computers—like laptops and desktops—can do a variety of other tasks. Virtualizing a server lets it to do more of those specific functions and involves partitioning it so that the components can be used to serve multiple functions.
</p>
<strong>Operating system virtualization</strong>
<br/>
	<img src="img/7.png">
<br/>
<p>
	Operating system virtualization happens at the kernel—the central task managers of operating systems. It’s a useful way to run Linux and Windows environments side-by-side. Enterprises can also push virtual operating systems to computers, which:
	<ul>
		<li>Reduces bulk hardware costs, since the computers don’t require such high out-of-the-box capabilities.</li>
		<li>Increases security, since all virtual instances can be monitored and isolated.</li>
		<li>Limits time spent on IT services like software updates.</li>
	</ul>
</p>
<strong>Network functions virtualization</strong>
<br/>
	<img src="img/8.png">
<br/>
<p>
	Network functions virtualization (NFV) separates a network's key functions (like directory services, file sharing, and IP configuration) so they can be distributed among environments. Once software functions are independent of the physical machines they once lived on, specific functions can be packaged together into a new network and assigned to an environment. Virtualizing networks reduces the number of physical components—like switches, routers, servers, cables, and hubs—that are needed to create multiple, independent networks, and it’s particularly popular in the telecommunications industry.
</p>
