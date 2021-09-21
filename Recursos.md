# Link Video explicando los métodos para base 64
https://drive.google.com/file/d/1sg3VUU9DQ3S_OHeol4gvfoEM3-zGiqty/view?usp=sharing

## CONVERTIR DE BASE64 COMO STRING A UN ARCHIVO

```plain

dataURItoBlob(dataURI: string) {
    const byteString = window.atob(dataURI);
    const arrayBuffer = new ArrayBuffer(byteString.length);
    const int8Array = new Uint8Array(arrayBuffer);
    for (let i = 0; i < byteString.length; i++) {
      int8Array[i] = byteString.charCodeAt(i);
    }
    const blob = new Blob([int8Array], { type: 'image/png' });    
    return blob;
 }



```

## CONVERTIR UN ARCHIVO A BASE64

```plain


 convertFileToBase64(){
    let reader= new FileReader();
    reader.readAsDataURL(this.fileSelected as Blob);
    reader.onloadend=()=>{
      this.base64=reader.result as string;
      
    } 


```
