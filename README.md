VMWare View Build for Fedora 19
===============================


Build and Installation Steps:


1. Create directory structure and cd into SOURCES:

        $ mkdir -p $HOME/rpmbuild/{SOURCES,BUILD}
        $ cd $HOME/rpmbuild/SOURCES

2. Download vmware.orig from Ubuntu repo:

        $ wget http://archive.canonical.com/ubuntu/pool/partner/v/vmware-view-client/vmware-view-client_2.1.0.orig.tar.gz

3. Clone this repo into $HOME/rpmbuild/SOURCES

        $ git clone <repourl> .

4. Build rpm binary with rpmbuild

        \# on 32bit
        $ rpmbuild -ba $HOME/rpmbuild/SOURCES/vmware-view-client.spec
        \# on 64bit
        $ linux32 rpmbuild -ba $HOME/rpmbuild/SOURCES/vmware-view-client.spec

5. If build succeeds, you should have an binary RPM to install, install with yum.

        $ sudo yum install $HOME/rpmbuild/RPMS/i686/vmware-view-client-2.1.0-1.fc19.i686.rpm



Rem: Verified by cvolny on Fedora 19 x86_64 on updated system on 2013-10-16
