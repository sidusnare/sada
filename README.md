# sada
ScAvenge DAta: Simple key value store for use when scripting.
Backended by simple JSON files

## Instalation

### Requirements
* Python 3
* \*NIX-ish OS ?

### Installing
Just drop it into your path, and have a directory $HOME/usr/var/sada , the script will make folders and files inside that path on its own. 

## Usage

All modes of operation are selected by how many arguments you provide the script

* No arguments - List buckets
  * Example: sada
  * This lists the buckets available
  * In this version, it ammounts to a ls in $HOME/usr/var/sada

* One argument - List keys
  * Example: sada phone_numbers
  * This will be matched to a bucket and list all the keys in that bucket
  * Would be similar to ls $HOME/usr/var/sada/phone_numbers/

* Two arguments - Read key
  * Example: sada phone_numbers bob
  * This will read the current value for that key
  * If the key is non-existant, it will give you a blank value
  * Output format is similar to input format \(\<bucket\> \<key\> \<value\>\)

* Three arguments - Write key
  * Example: sada phone_numbers bob 1-900-876-5309
  * This will set the key bob to 1-900-876-5309
  * Any existing value will be appended to an array in the file named history, that you can look at manually.
