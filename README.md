
**Sandbox AppImages installed by AM easily with the help of aisap**

The default location for the sandboxed homes is at $HOME/.local/am-sandboxes. That location can be changed by setting the `$SANDBOXDIR` env variable.

aisap: https://github.com/mgord9518/aisap

AM/AppMan: https://github.com/ivan-hc/AM

aisap can be installed by AM as well using `am -i aisap` or `appman -i aisap`

By default the following location are given access to, edit each resulting script if needed (The default permissions might change in the future): 

```
--add-file "$DATADIR"/themes \
--add-file "$DATADIR"/icons \
--add-file "$CONFIGDIR"/gtk3.0 \
--add-file "$CONFIGDIR"/gtk4.0 \
--add-file "$CONFIGDIR"/kdeglobals \
--add-file "$CONFIGDIR"/qt5ct \
--add-file "$CONFIGDIR"/qt6ct \
--add-file "$CONFIGDIR"/Kvantum \
--add-file "$HOME"/.local/lib \
--add-socket x11 \
--add-socket wayland \
--add-socket pulseaudio \
--add-socket network \
--add-device dri \
```

Also be aware that aisap has its own set of rules for some appimages that give extra access to things like `~/Downloads`: https://github.com/mgord9518/aisap/blob/main/profiles/profile_database.json
