# Seafile_WebAPI
Seafile_webapi is the Web api of Seafile implemented by java,all of them base on the Seafile Web API V2.1

## List of the API
 - Account
    - ping()
    - obtainAuthToken()
    - checkAccountInfo()
    - getServerInformation()
    - createNewAccount()
    - deleteAccount()
 - Starred Files
    - listStarredFiles()
 - Library
    - listLibraries()
    - getLibraryInfo()
    - getLibraryHistory()
    - createLibrary()
    - deleteLibrary()
 - File
    - getFileDownloadLink()
    - getFileDetail()
    - getFileHistory()
    - createFile()
    - renameFile()
    - moveFile()
    - revertFile()
    - deleteFile()
    - upload File
        - getUploadLink()
        - uploadFile()
    - update File
        - getUpdateLink()
        - updateFile()
 - Directory
     - List Directories
        - listDirEntriesByP()
        - listAllDirEntries()
     - createNewDir()
     - renameDir()
     - deleteDir()
     - downloadDirectory
         - getDirDownloadToken()
         - queryZipProgress()
         - getDirDownloadLink()
     - ~~revertDirectory()~~
 
 
## Examples

    String SERVICE_URL= "https://cloud.seafile.com";
    String FILE_SERVER_ROOT = "https://cloud.seafile.com/seafhttp";
    
    OkHttpClient client = new OkHttpClient();
    
    com.aitlp.impl.SeafileApi api = new com.aitlp.impl.SeafileApi(SERVICE_URL, FILE_SERVER_ROOT);
    String token = api.obtainAuthToken(client, Account.username, Account.password);
    
    System.out.println("token = " + token);

## Dependency
 - fastjson-1.2.36
 - okhttp-3.8.1
    - okio-1.13.0
    
## Complete documentation
 - You can see the Complete documentation of Seafile Web Api in [Seafile-WebAPI-V2.1](https://manual.seafile.com/develop/web_api_v2.1.html), 
 - The more examples of Seafile_WebAPI_JAVA , you can see in `com.aitlp.test.SeafileApiTest.java`