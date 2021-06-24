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
<h1>Virtualization</h1>
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
<h1>Hypervisors</h1>
<p>
	A hypervisor is a form of virtualization software used in Cloud hosting to divide and allocate the resources on various pieces of hardware. The program which provides partitioning, isolation or abstraction is called virtualization hypervisor. The hypervisor is a hardware virtualization technique that allows multiple guest operating systems (OS) to run on a single host system at the same time. A hypervisor is sometimes also called a virtual machine manager(VMM).
</p>
<h2>Types of Hypervisor </h2>
<img src="img/9.png">
<h3>TYPE-1 Hypervisor: </h3>
<br/>
<p>
	The hypervisor runs directly on the underlying host system. It is also known as “Native Hypervisor” or “Bare metal hypervisor”. It does not require any base server operating system. It has direct access to hardware resources. Examples of Type 1 hypervisors include VMware ESXi, Citrix XenServer and Microsoft Hyper-V hypervisor
</p>
<strong>Pros & Cons of Type-1 Hypervisor:</strong>
<br/>
<p>
	<strong>Pros:</strong>Such kind of hypervisors are very efficient because they have direct access to the physical hardware resources(like Cpu, Memory, Network, Physical storage). This causes the empowerment the security because there is nothing any kind of the third party resource so that attacker couldn’t compromise with anything. 
</p>
<p>
	<strong>Cons:</strong>One problem with Type-1 hypervisor is that they usually need a dedicated separate machine to perform its operation and to instruct different VMs and control the host hardware resources.
</p>
<h3>TYPE-2 Hypervisor: </h3>
<p>
	A Host operating system runs on the underlying host system. It is also known as ‘Hosted Hypervisor”. Such kind of hypervisors doesn’t run directly over the underlying hardware rather they run as an application in a Host system(physical machine). Basically, software installed on an operating system. Hypervisor asks the operating system to make hardware calls. Example of Type 2 hypervisor includes VMware Player or Parallels Desktop. Hosted hypervisors are often found on endpoints like PCs.  The type-2 hypervisor is are very useful for engineers, security analyst(for checking malware, or malicious source code and newly developed applications).
</p>
<strong>Pros & Cons of Type-2 Hypervisor:</strong>
<p>
	<strong>Pros: </strong>Such kind of hypervisors allows quick and easy access to a guest Operating System alongside the host machine running. These hypervisors usually come with additional useful features for guest machine. Such tools enhance the coordination between the host machine and guest machine.
</p>
<p>
	<strong>Cons: </strong>Here there is no direct access to the physical hardware resources so the efficiency of these hypervisors lags in performance as compared to the type-1 hypervisors, and potential security risks are also there an attacker can compromise the security weakness if there is access to the host operating system so he can also access the guest operating system.
</p>
<h2>Choosing the right hypervisor :</h2>
<p>
	<strong>Type 1 hypervisors offer much better performance than Type 2 </strong>ones because there’s no middle layer, making them the logical choice for mission-critical applications and workloads. But that’s not to say that hosted hypervisors don’t have their place – they’re much simpler to set up, so they’re a good bet if, say, you need to deploy a test environment quickly. One of the best ways to determine which hypervisor meets your needs is to compare their performance metrics. These include CPU overhead, amount of maximum host and guest memory, and support for virtual processors. The following factors should be examined before choosing a suitable hypervisor:
	<ol>
		<li><strong>Understand your needs:</strong>The company and its applications are the reason for the data centre (and your job). Besides your company’s needs, you (and your co-workers in IT) also have your own needs. Needs for a virtualization hypervisor are: 
			<ul>
				<li>Flexibility</li>
				<li>Scalability</li> 
				<li>Usability</li> 
				<li>Availability</li> 
				<li>Reliability</li> 
				<li>Efficiency</li> 
				<li>Reliable support</li> 
			</ul>
		</li>
		<li>
			<strong>The cost of a hypervisor: </strong>For many buyers, the toughest part of choosing a hypervisor is striking the right balance between cost and functionality. While a number of entry-level solutions are free, or practically free, the prices at the opposite end of the market can be staggering. Licensing frameworks also vary, so it’s important to be aware of exactly what you’re getting for your money. 
		</li>
		<li>
			<strong>Virtual machine performance: </strong>Virtual systems should meet or exceed the performance of their physical counterparts, at least in relation to the applications within each server. Everything beyond meeting this benchmark is profit.
		</li>
		<li>
			<strong>Ecosystem: </strong>It’s tempting to overlook the role of a hypervisor’s ecosystem – that is, the availability of documentation, support, training, third-party developers and consultancies, and so on – in determining whether or not a solution is cost-effective in the long term. 
		</li>
		<li>
			<strong>Test for yourself:</strong>You can gain basic experience from your existing desktop or laptop. You can run both VMware vSphere and Microsoft Hyper-V in either VMware Workstation or VMware Fusion to create a nice virtual learning and testing environment. 
		</li>
	</ol>
<p>
<h3>HYPERVISOR REFERENCE MODEL :</h3>

<p>There are 3 main modules coordinates in order to emulate the underlying hardware: </p>
<p>
	<ol>
		<li><strong>DISPATCHER: </strong></li>
		<br/>
			The dispatcher behaves like the entry point of the monitor and reroutes the instructions of the virtual machine instance to one of the other two modules. 
		<li><strong>ALLOCATOR</strong></li>
		<br/>
			The allocator is responsible for deciding the system resources to be provided to the virtual machine instance.It means whenever virtual machine tries to execute an instruction that results in changing the machine resources associated with the virtual machine, the allocator is invoked by the dispatcher. 
		<li><strong>INTERPRETER</strong></li>
		<br/>
			The interpreter module consists of interpreter routines.These are executed, whenever virtual machine executes a priviliged instruction
	</ol>
</p>
<h1>Virtual Machine (VM)</h1>
<p>
	A virtual machine (VM) is a virtual environment that functions as a virtual computer system with its own CPU, memory, network interface, and storage, created on a physical hardware system (located off- or on-premises). Software called a hypervisor separates the machine’s resources from the hardware and provisions them appropriately so they can be used by the VM.
</p>
<p>
	The physical machines, equipped with a hypervisor such as Kernel-based Virtual Machine (KVM), is called the host machine, host computer, host operating system, or simply host. The many VMs that use its resources are guest machines, guest computers, guest operating systems, or simply guests. The hypervisor treats compute resources—like CPU, memory, and storage—as a pool of resources that can easily be relocated between existing guests or to new virtual machines.
</p>
<p>
	VMs are isolated from the rest of the system, and multiple VMs can exist on a single piece of hardware, like a server. They can be moved between host servers depending on demand or to use resources more efficiently.
</p>
<p>
	VMs allow multiple different operating systems to run simultaneously on a single computer—like a Linux® distro on a MacOS laptop. Each operating system runs in the same way an operating system or application normally would on the host hardware, so the end user experience emulated within the VM is nearly identical to a real-time operating system experience running on a physical machine.
</p>
<img src ="img/10.png">
<br/>	
<h2>How do VMs work?</h2>
<p>
	Virtualization technology allows you to share a system with many virtual environments. The hypervisor manages the hardware and separates the physical resources from the virtual environments. Resources are partitioned as needed from the physical environment to the VMs.
</p>
<p>
	When the VM is running and a user or program issues an instruction that requires additional resources from the physical environment, the hypervisor schedules the request to the physical system’s resources so that the virtual machine’s operating system and applications can access the shared pool of physical resources.
</p>
<h2>Why use a VM?</h2>
<p>
	Server consolidation is a top reason to use VMs. Most operating system and application deployments only use a small amount of the physical resources available when deployed to bare metal. By virtualizing your servers, you can place many virtual servers onto each physical server to improve hardware utilization.
</p>
<p>
	This keeps you from needing to purchase additional physical resources, like hard drives or hard disks, as well as reducing the need for power, space, and cooling in the datacenter. VMs provide additional disaster recovery options by enabling failover and redundancy that could previously only be achieved through additional hardware.
</p>
<p>
	A VM provides an environment that is isolated from the rest of a system, so whatever is running inside a VM won’t interfere with anything else running on the host hardware
</p>
<p>
	Because VMs are isolated, they are a good option for testing new applications or setting up a production environment. You can also run a single purpose VM to support a specific process.
</p>	
<h1>Linux</h1>
<p>
	Linux® is an open source operating system (OS). An operating system is the software that directly manages a system’s hardware and resources, like CPU, memory, and storage. The OS sits between applications and hardware and makes the connections between all of your software and the physical resources that do the work.
</p>
<p>
	Think about an OS like a car engine. An engine can run on its own, but it becomes a functional car when it’s connected with a transmission, axles, and wheels. Without the engine running properly, the rest of the car won’t work.
</p>
<h2>How does Linux work?</h2>
<p>
	Linux was designed to be similar to UNIX, but has evolved to run on a wide variety of hardware from phones to supercomputers. Every Linux-based OS involves the Linux kernel—which manages hardware resources—and a set of software packages that make up the rest of the operating system.
</p>
<p>
	The OS includes some common core components, like the GNU tools, among others. These tools give the user a way to manage the resources provided by the kernel, install additional software, configure performance and security settings, and more. All of these tools bundled together make up the functional operating system. Because Linux is an open source OS, combinations of software can vary between Linux distributions.
</p>
<h2>What's a command line?</h2>
<p>
	The command line is your direct access to a computer. It's where you ask software to perform hardware actions that point-and-click graphical user interfaces (GUIs) simply can't ask. 
</p>
<p>
	Command lines are available on many operating systems—proprietary or open source. But it’s usually associated with Linux, because both command lines and open source software, together, give users unrestricted access to their computer.
</p>
<h2>Top 10 Flavor of linux</h2>
<ol>
	<li>Fedora</li>
	<li>Ubuntu</li>
	<li>CentOS</li>
	<li>Debian</li>
	<li>Kali Linux</li>
	<li>Red Hat Enterprise Linux</li>
	<li>Arch Linux</li>
	<li>OpenSUSE</li>
	<li>Gentoo</li>
	<li>Linux Mint</li>
</ol>
<h1>ISO File</h1>
<p>
	ISO stands for International Organization for Standardization but it isn’t what the .iso file extension stands for. The extension was derived out standard patented by the International Organization for Standardization, for filesystems in optical (CD/DVD) disks. The file system standard is under the name ISO 9660, where the former term is used as the extension .iso for CD/DVD disk image files. But, ISO files represented with the .iso extension isn’t mandatory, as ISO files with file extensions such as .img, .udf also exists.
</p>
<img src= "img/11.png">
<br/>
<p>
	<strong>ISO files are also referred to as image files</strong> as they use the exact format as a disk and could be mounted on one’s operating system as if it were a discrete disk. An ISO image is an archive file of an optical disc, a type of disk image composed of the data contents from every written sector on an optical disc, including the optical disc file system.
</p>
<h3>Characteristics of an ISO Image</h3>
<p>
	ISO image format is uncompressed, containerless, and are stored in binary format. They are a sector-by-sector copy of the contents of an optical drive. Upon encountering an ISO image, the system expects the binary data of format specified under ISO 9660 or UDF (Universal Disk Format), optical media file system standard. ISO files like a regular file, aren’t opened, but rather they are mounted (as if they are a volume/device). This behavior is similar to when an operating system recognizes an optical drive. When ISO images are created from optical disks, then ISO files store only the user data from each sector on an optical disc, ignoring the control headers and error correction data, and are therefore slightly smaller than a raw disc image of optical media. The file format isn’t exclusive to CD/DVD drives, as one could create an ISO image file with custom files, where the ISO would act as a Physical Disk Drive when mounted.
</p>
<h3>Advantages of ISO</h3>
<p>
	<ul>
		<li>
			Allows quick access of files contained within, as the file is mounted (as opposed to other similar formats where contents need to be extracted).
		</li>
		<li>
			Gives deception of a virtual drive, and therefore could be used as a backward compatibility option for the application that requires a disk drive
		</li>
		<li>
			Most operating systems provide native support for ISO image files, therefore no utility is required for using this file format
		</li>
	</ul>
</p>
<h3>Disadvantages of ISO</h3>
<p>
	<ul>
		<li>
			The files inside an ISO image could be edited, but the whole ISO needs to be recompiled again which is time-consuming (as opposed to other formats such as ZIP, etc)
		</li>
		<li>
			Performance may not be the most optimal, as the file format follows as optical drive structure which isn’t much efficient
		</li>
		<li>
			No significant error resilience or integrity preserving protocols are enforced in the format
		</li>
		<li>
			Small corruption in any sector of the data, leads to unmountable ISO image files (since the file must be mounted in order to access the data inside, it consequently leads to the data becoming unreadable or not accessible)
		</li>
	</ul>
</p>
<h3>Applications of ISO</h3>
	<ul>	
		<li>
			ISO image files are used in emulating a optical drives in Video Game Console emulators such as RPCS3, PCSX2, Zenia, PPSSPP etc
		</li>
		<li>
			<strong>The format is used extensively for storing copies of Operating systems like Windows, linux, Disk Operating System (DOS) etc.</strong>
		</li>
		<li>
			Used by backup programs to create backup disks
		</li>
	</ul>

