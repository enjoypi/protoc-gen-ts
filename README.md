## protoc-gen-ts
Typescript support for Protocol Buffers

// ** USAGE:
// go get github.com/enjoypi/protoc-gen-ts
// cd $YOUR_GOPATH/src/github.com/enjoypi/protoc-gen-ts
// go install && protoc --ts_out=. languages.proto
// ** it will generate a languages.ts file

// languages.proto
syntax = "proto3";

package proto;

message Languages {
    string en = 1; // English
    string es = 2; // Spanish
    string de = 3; // German
    string fr = 4; // French
    string it = 5; // Italian
    string ja = 6; // Japanese
    string ko = 7; // Korean
    string pt = 8; // Portuguese
    string zhs = 9; // zh-Hans Simplified Chinese
    string zht = 10; // zh-Hant Traditional Chinese
    string ru = 11; // Russian
}

// languages.ts

export class Languages {
	en:		string;
	es:		string;
	de:		string;
	fr:		string;
	it:		string;
	ja:		string;
	ko:		string;
	pt:		string;
	zhs:		string;
	zht:		string;
	ru:		string;
	
	constructor() {
		this.en = "";
		this.es = "";
		this.de = "";
		this.fr = "";
		this.it = "";
		this.ja = "";
		this.ko = "";
		this.pt = "";
		this.zhs = "";
		this.zht = "";
		this.ru = "";
	}
}

interface LanguagesConstructor {
	new (): Languages;
}


