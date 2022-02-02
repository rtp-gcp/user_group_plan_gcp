


# set the default goal.
.DEFAULT_GOAL := list_docs
#.phony: list_docs gitupdate clean



list_docs:
	ls -l



gitupdate: clean
	git add .; git commit -m "update secrets/urls dir"; git push

clean:
	echo "docs: make clean"
	#-find . -name "*.backup" -print | xargs rm
	#-rm *.md
	-rm *.backup *.BACKUP *.swp *.key *.md



encrypt:
	gpg --output README.md.gpg --encrypt --recipient davisjf@gmail.com --recipient sedrick@10ronline.net README.md



decrypt:
	gpg --decrypt README.md.gpg

decrypt_tofile:
	gpg --output README.md --decrypt README.md.gpg
