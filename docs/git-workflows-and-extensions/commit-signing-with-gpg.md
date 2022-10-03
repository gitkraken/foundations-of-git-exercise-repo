---

title: Commit Signing with gpg
description: Learn how to create GPG keys and sign your commits in GitKraken Client

---

##What is Commit Signing?

In Git, you may commit using any name and email address. However, Git supports signing commits and annotated tags using a GPG key pair.

By signing a commit, other users with your public key can verify the commit was created by the owner of that key. Users can also share their public key with their remote hosting service, such as GitHub, so that commits appear as verified on their website.

###Commit Signing Requirements

Before you start signing your commits, you will first need to install and configure GPG. GPG download files can be found [here](https://www.gnupg.org/download/index.html). Our recommendations to get GPG installed quickly are below.

<div class='callout callout--warning'>
    <p><strong>Note:</strong> If you have GitKraken Client open, we recommend closing the application before installing GPG. </p>
</div>


+ **Windows:** [Gpg4win](https://gpg4win.org/download.html), simply follow the installer.

+ **Mac:** We recommend downloading GPG on Mac through [Brew](https://brew.sh/). Once you have brew, simply run `brew install gpg`.

+ **Linux:**  Install gpg through your distribution’s package manager.

	+ **Debian/Ubuntu:** `apt install gnupg`
	+ **Fedora:** `dnf install gnupg2`
	+ **CentOS/RHEL:** `yum install gnupg2`

Once you have installed GPG to your machine, you can verify it is installed and check the version by opening your terminal and running `gpg --version`.

<div class='callout callout--success'>
    <p><strong>Note:</strong> You may need to replace `gpg` with `gpg2` if you installed GPG2 without an alias. If you have both gpg and gpg2, you will need to prefix with gpg2 if you wish to use the latter. </p>
</div>

<img src="/img/documentation/commit-signing-gpg/gpg-verify.png" srcset="/img/documentation/commit-signing-gpg/gpg-verify@2x.png 2x" class="img-bordered img-responsive center">


###Generating a GPG Key In GitKraken

If you have GPG installed on your local machine, you will be able to generate a GPG key pair from within GitKraken Client. 
<div class='callout callout--success'>
    <p><strong>Note:</strong> Make sure that you have [configured GPG inside of GitKraken Client](/git-workflows-and-extensions/commit-signing-with-gpg/#configure-gpg-in-gitkraken).</p>
</div>

Under `Preferences` → `GPG Preferences`, there is an option to `Generate new GPG Key`. If you wish to enter a passphrase, make sure you do so prior to selecting `Generate`.

<img src="/img/documentation/commit-signing-gpg/generate-new-gpg-key.png" srcset="/img/documentation/commit-signing-gpg/generate-new-gpg-key@2x.png 2x" class="img-bordered img-responsive center">

###Configure GPG in GitKraken

Once you have GPG installed on your machine, you will need to configure GitKraken to use GPG. Launch GitKraken Client and navigate to Preferences → GPG Preferences.

<img src="/img/documentation/commit-signing-gpg/gpg-preferences.png" srcset="/img/documentation/commit-signing-gpg/gpg-preferences@2x.png 2x" class="img-bordered img-responsive center">

+ **Signing Key:** This dropdown list will contain all of your local keys. Select the key you wish GitKraken Client to use when signing your commits and annotated tags. **If this list is blank you can try the following troubleshoots:** 
    * You may need to configure the GPG Program setting first. 
    + If you installed GPG while GitKraken Client was open, you may need to fully close GitKraken Client and re-launch it.

+ **GPG Program:** This is the location of where GPG is installed on your local machine. If GPG is on your path, GitKraken Client should automatically detect the GPG program. However, it is possible to have multiple installations of GPG so you can specify which one GitKraken Client should point to by using the 
<button class='button button--primary button--ui button--nolink'><span style='color:#E9EEFF;'>Browse</span></button>
button.

<img src="/img/documentation/commit-signing-gpg/gpg-browse-button.png" srcset="/img/documentation/commit-signing-gpg/gpg-browse-button.png 2x" class="img-bordered img-responsive center">

 If you do not know where GPG is installed on your local machine, launch a terminal and enter: `which gpg` for Mac & Linux. On Windows, use: `where gpg`

+ **Sign Commits by Default:** Enabling this checkbox will have GitKraken Client sign any commit you create going forward.

+ **Sign Tags by Default:** Enabling this checkbox will have GitKraken Client sign any annotated tags you create going forward.

+ **Generate new GPG Key:** GitKraken Client will generate a new GPG key for you, see [Generating a GPG Key In GitKraken](/git-workflows-and-extensions/commit-signing-with-gpg/#generating-a-gpg-key-in-gitkraken).

###Verifying a Local Commit is Signed

You can verify a commit has been signed by selecting a commit and viewing the commit panel. An icon will appear to the left of the commit SHA on signed commits only.

<img src="/img/documentation/commit-signing-gpg/verified-commit.png" srcset="/img/documentation/commit-signing-gpg/verified-commit@2x.png 2x" class="img-bordered img-responsive center">

If you hover over the badge, you will see a tooltip which displays the Signature details.

<img src="/img/documentation/commit-signing-gpg/gpg-signature-details.png" srcset="/img/documentation/commit-signing-gpg/gpg-signature-details@2x.png 2x" class="img-bordered img-responsive center">

Below is a list of possible signature codes and what they mean:

+ `GOODSIG` -- The signature with the keyid is good.
+ `EXPSIG` -- The signature with the keyid is good, but the signature is expired. 
+ `EXPKEYSIG` -- The signature with the keyid is good, but the signature was made by an expired key.
+ `REVKEYSIG` -- The signature with the keyid is good, but the signature was made by a revoked key.
+ `BADSIG` -- The signature with the keyid has not been verified.
+ `ERRSIG` -- It was not possible to check the signature. This may be caused by a missing public key or an unsupported algorithm.


###Uploading Your GPG Key to a Remote Hosting Service

To upload your GPG public key to your remote hosting service, we recommend viewing the documentation for the respective hosting service:

* <em class='context-menu'><i class="fab fa-github"></i></em> [GitHub](https://help.github.com/articles/adding-a-new-gpg-key-to-your-github-account/)
* <em class='context-menu'><i class="fab fa-gitlab" aria-hidden="true"></i></em> [GitLab](https://docs.gitlab.com/ee/user/project/repository/gpg_signed_commits/#adding-a-gpg-key-to-your-account)
* <em class='context-menu'><i class="fab fa-bitbucket" aria-hidden="true"></i></em> [Bitbucket](https://confluence.atlassian.com/bitbucketserver/using-gpg-keys-913477014.html#UsingGPGkeys-AddaGPGkeytoBitbucketServer)

To copy your GPG public key in GitKraken Client, navigate to Preferences → GPG Preferences and below your Signing Key, select `Copy GPG Public Key`.

###Editing Your GPG Key

Editing your gpg key is helpful when you wish to add another email address to a key or renew an expired key. To edit a GPG key, navigate to your terminal and enter `gpg --list-secret-keys --keyid-format LONG`. This command will output a list of your GPG keys, take note of the ID of the key you wish to edit.

<img src="/img/documentation/commit-signing-gpg/list-secret-keys.png"  class="img-bordered img-responsive center">

Now that you have the key ID, you can edit the key. To do so enter `gpg --edit-key FFFFFF` where `FFFFFF` is your key ID. You will then enter an editing session with your GPG key. After you update your key, execute a `save` to record changes and quit editing the key.

Below is a list of useful commands to edit your key:

+ `adduid`- Add a new user ID to the GPG key
+ `deluid` - Delete a user ID from the GPG key
+ `trust` - Change the owner trust value. This updates the trust database immediately and no save is required.
+ `expire` - Change a key expiration time
+ `save` - Save all changes to the current key and quit
+ `quit` - Quit without updating the current key

For a complete list you can review [GNU’s documentation](https://www.gnupg.org/gph/en/manual/r899.html).

Make sure to upload the updated key on your hosting service once you have saved. See [Uploading Your GPG Key to a Remote Hosting Service](/git-workflows-and-extensions/commit-signing-with-gpg/#uploading-your-gpg-key-to-a-remote-hosting-service).

###Deleting your GPG Key

You can delete your key via terminal with the command `gpg --delete-secret-keys` simply append your username or key ID. 
<img src="/img/documentation/commit-signing-gpg/delete-key.png" class="img-bordered img-responsive center">

There will be several prompts to make sure that you *really* want to delete your GPG key:
<img src="/img/documentation/commit-signing-gpg/delete-key-for-sure.png"  class="img-bordered img-responsive center">

