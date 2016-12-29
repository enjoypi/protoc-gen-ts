# protoc-gen-ts
Typescript support for Protocol Buffers

```protobuf
syntax = "proto3";

import "languages.proto";

package proto;

message Mail {
    Languages subjects = 1; // <language, subject>
    Languages bodies = 2; // <language, body>
    map<uint64, uint32> assets = 3; // <assetID, amount>
    repeated uint64 maps = 4; // mapID list
    string reason = 5;
    uint64 time = 6;
    string creator = 7;
}
```

```ts
import {Languages} from "./languages";

export class Mail {
	subjects:	Languages;
	bodies:		Languages;
	assets:		Array<[number,number]>;
	maps:		Array<number>;
	reason:		string;
	time:		number;
	creator:	string;
}
```