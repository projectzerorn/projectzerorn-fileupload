# projectzerorn-fileupload  [![NPM version](https://img.shields.io/npm/v/react-native-fileupload.svg?style=flat-square)](https://www.npmjs.com/package/projectzerorn-fileupload)


# Installation

```
npm install projectzerorn-fileupload --save
rnpm link react-native-file-uploader
```

# Usage
All you need is to export module `import {FileUpload} from 'NativeModules';` and direct invoke `FileUpload.upload`.

```javascript

		import {FileUpload} from 'NativeModules';

		var obj = {
            uploadUrl: 'http://file.testapi.dev.ipo.com/file/upload/',
            headers: {
                'referer': 'http://www.fangjiadp.com',
            },
            fields: {
                'file': 'file',
            },
            files: [
                {
                    filepath: '/sdcard/1.png',  //android文件支持: 1.content: 2.file: 3.绝对路径
                                                //iOS文件待测试 支持: 1.assets-library:  2.data:  3.file: 4.绝对路径
                },
            ]
        };
        
        FileUpload.upload(obj, (err, result)=> {
            console.log('upload:', err, result);
		})
```

# License

MIT
