VMWare View Build for Fedora 19
===============================


Build and Installation Steps:


1. Create directory structure and cd into SOURCES:

        $ mkdir -p $HOME/rpmbuild/{SOURCES,BUILD}
        $ cd $HOME/rpmbuild/SOURCES

2. Clone this repo into vmware-view-client:

        $ git clone https://github.com/cvolny/vmware-view-client.git vmware-view-client

3. Download vmware.orig.tar.gz from Ubuntu repo[1]:

        $ wget http://archive.canonical.com/ubuntu/pool/partner/v/vmware-view-client/vmware-view-client_2.1.0.orig.tar.gz

4. Move relevant files into SOURCES:

	$ cp -t . vmware-view-client/vmware-view{-client.{desktop,png,spec},.sh}

5. Build rpm binary with rpmbuild:

        # on 32bit
        $ rpmbuild -ba vmware-view-client.spec
        # on 64bit
        $ linux32 rpmbuild -ba vmware-view-client.spec

6. If build succeeds, you should have an binary RPM to install, install with yum as root:

        $ sudo yum install $HOME/rpmbuild/RPMS/i686/vmware-view-client-2.1.0-1.fc19.i686.rpm



Remarks:

1. Canonical Repo: http://archive.canonical.com/ubuntu/pool/partner/v/vmware-view-client/
2. Instructions verified by cvolny on Fedora 19 x86_64 on updated system on 2013-10-16.

 
