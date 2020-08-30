# Restore from Server without Unlimited Extension   
 
 Replace this (Tested on version 7.26) :   
    
    /* eslint-disable no-unused-vars */
		if (Ai1wm.MultisiteExtensionRestore) {
			var restore = new Ai1wm.MultisiteExtensionRestore($(this).data('archive'), $(this).data('size'));
		} else if (Ai1wm.UnlimitedExtensionRestore) {
			var _restore = new Ai1wm.UnlimitedExtensionRestore($(this).data('archive'), $(this).data('size'));
		} else if (Ai1wm.FreeExtensionRestore) {
			var _restore2 = new Ai1wm.FreeExtensionRestore($(this).data('archive'), $(this).data('size'));
		} else {
			var _restore3 = new Ai1wm.Restore($(this).data('archive'), $(this).data('size'));
		}
		/* eslint-enable no-unused-vars */
 
 With this :   
 
		/* eslint-disable no-unused-vars */
		var storage = Ai1wm.Util.random(12),
        restoore = Ai1wm.Util.form("#ai1wm-backups-form").concat({ name: "storage", value: storage }).concat({ name: "archive", value: $(this).data('archive') }),
        restooore = new Ai1wm.Import();
        restooore.setParams(restoore), restooore.start();	
		/* eslint-enable no-unused-vars */
