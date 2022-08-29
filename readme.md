![header](https://capsule-render.vercel.app/api?type=waving&color=0:d70a84,100:51127f&height=300&section=header&fontSize=90&text=AniOSP&fontAlign=75&fontColor=ffffff&desc=for%20otakus,%20by%20otakus&descAlign=80)
### Welcome to the AniOSP manifest! Here, you can find some simple guides to get started.
# THIS PROJECT IS ACTUALLY NOT FINISHED, DON'T EVEN TRY TO BUILD IT
-----------------------------------------------------------------------------------------

### Downloading:
To download, you will need around 100GB of free space, so clearing out some of your hentai folder may be required.

Make a directory, as this is where the flaming piece of garbage will reside, and you don't want that spreading to other parts of your system. Once you're in that directory, run:

`repo init -u http://github.com/AniOSP/manifest -b aiko-13 --depth=1`

This will go ahead and download some neccesary files for running repo commands, but you have one more thing to run. It may crash ask you for your github username and email, if so, it will provide commands for setting it, and you can rerun the command after you do said credential setting. After a minute or so, assuming nothing goes wrong, the command will finish, and the repo will be initialized.

Once your hentai folder has been cleared out a bit, run (in the directory that you made for AniOSP):

`repo sync -c -j$(nproc --all) --force-sync --no-clone-bundle --no-tags`

The above command can take between several minutes to several hours, potentially days if you have a slow internet connection/on a Hard Disk Drive. Once it completes, you can get to building
-----------------------------------------------------------------------------------------

### Building
```sh
. build/envsetup.sh
lunch aniosp_$device-userdebug
mka aniosp
```

This can take several hours to complete, depending on how many CPU cores you have and if you have `ccache` installed or not.

Once the build is complete, you can find your sideloadable OTA zip file in `out/target/product/$device/$version.zip`
