Domain - ORM and migrations
Api - the external callings (to external APIs)
Service - the exposed services (Bussiness logic)
Client - endpoint to user
Interface - the interfaces invoked by Service
DataMapping - maps the gathered (received data) through Service and give mapped to Service

To run the project on Linux check more about the dotnet commandline https://learn.microsoft.com/en-us/dotnet/core/tools/
To sign commits with Assimetric Encryption: https://docs.github.com/en/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent
	generate the key: gpg --full-generate-key #preferred RSA default type
	then find the keyid (what identifies the key in GPG): gpg --list-secret-keys --keyid-format LONG
	git config --global user.signingkey keyid_here
	signing: git commit -S -m "comment" #do it by adding the -S option
	adding to GitHub, get your public key: gpg --armor --export keyid_here 
	*PS: Signing a commit with `sudo` may not work 
