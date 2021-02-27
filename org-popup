#!/bin/bash

usage(){
	echo "Usage: org-popup template [title?]"
	exit 0
}

if [[ "$1"  = "-h" ]]; then
	usage
elif [[ "$1" ]]; then

	if [[ $2 ]]; then
		DEF="** \n\t`xsel`"
	else
		DEF="** `xsel`"
	fi

	DATA=$(yad --form --field '!:TXT' "$DEF" --undecorated --width 700 --height 300 --center --no-buttons|tr -d "|")
	if [[ $DATA ]]; then
		echo -e "$DATA" > ~/.emacs.d/.org-popup
		emacsclient "org-protocol://capture?template=$1"
	fi
fi