---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: CBD157D2-37C5-491F-A806-6B39F1D0415A
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/get-azurestorageblobcopystate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageBlobCopyState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageBlobCopyState.md
ms.openlocfilehash: 619f909ab794b5531d15d89343ea6263bea7ce03
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93426530"
---
# Get-AzureStorageBlobCopyState

## Sinopse
Obtém o status da cópia de um blob de armazenamento do Azure.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

### NamePipeline (padrão)
```
Get-AzureStorageBlobCopyState [-Blob] <String> [-Container] <String> [-WaitForComplete]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### BlobPipeline
```
Get-AzureStorageBlobCopyState -CloudBlob <CloudBlob> [-WaitForComplete] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### ContainerPipeline
```
Get-AzureStorageBlobCopyState -CloudBlobContainer <CloudBlobContainer> [-Blob] <String> [-WaitForComplete]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Get-AzureStorageBlobCopyState** Obtém o status da cópia de um blob de armazenamento do Azure.

## EXEMPLOS

### Exemplo 1: obter o status da cópia de um blob
```
C:\PS>Get-AzureStorageBlobCopyState -Blob "ContosoPlanning2015" -Container "ContosoUploads"
```

Esse comando obtém o status da cópia do blob chamado ContosoPlanning2015 na ContosoUploads do contêiner.

### Exemplo 2: obter o status da cópia de um BLOB usando o pipeline
```
C:\PS>Get-AzureStorageBlob -Blob "ContosoPlanning2015" -Container "ContosoUploads" | Get-AzureStorageBlobCopyState
```

Esse comando obtém o blob chamado ContosoPlanning2015 no contêiner chamado ContosoUploads usando o cmdlet **Get-AzureStorageBlob** e, em seguida, passa o resultado para o cmdlet atual usando o operador pipeline.
O cmdlet **Get-AzureStorageBlobCopyState** Obtém o status de cópia desse blob.

### Exemplo 3: obter o status da cópia de um blob em um contêiner usando o pipeline
```
C:\PS>Get-AzureStorageContainer -Name "ContosoUploads" | Get-AzureStorageBlobCopyState -Blob "ContosoPlanning2015"
```

Esse comando obtém o contêiner nomeado usando o cmdlet **Get-AzureStorageBlob** e, em seguida, passa o resultado para o cmdlet atual.
O cmdlet **Get-AzureStorageContainer** Obtém o status de cópia do blob chamado ContosoPlanning2015 nesse contêiner.

## OS

### -Blob
Especifica o nome de um blob.
Esse cmdlet obtém o estado da operação de cópia de BLOB para o blob de armazenamento do Azure que esse parâmetro especifica.

```yaml
Type: System.String
Parameter Sets: NamePipeline, ContainerPipeline
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ClientTimeoutPerRequest
Especifica o intervalo de tempo limite do lado do cliente, em segundos, para uma solicitação de serviço.
Se a chamada anterior falhar no intervalo especificado, esse cmdlet tentará novamente a solicitação.
Se esse cmdlet não receber uma resposta bem-sucedida antes do intervalo ser decorrido, esse cmdlet retornará um erro.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CloudBlob
Especifica um objeto **CloudBlob** da biblioteca de cliente de armazenamento do Azure.
Para obter um objeto **CloudBlob** , use o cmdlet Get-AzureStorageBlob.

```yaml
Type: Microsoft.WindowsAzure.Storage.Blob.CloudBlob
Parameter Sets: BlobPipeline
Aliases: ICloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -CloudBlobContainer
Especifica um objeto **CloudBlobContainer** da biblioteca de cliente de armazenamento do Azure.
Esse cmdlet obtém o status da cópia de um blob no contêiner que esse parâmetro especifica.
Para obter um objeto **CloudBlobContainer** , use o cmdlet Get-AzureStorageContainer.

```yaml
Type: Microsoft.WindowsAzure.Storage.Blob.CloudBlobContainer
Parameter Sets: ContainerPipeline
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ConcurrentTaskCount
Especifica o número máximo de chamadas de rede simultâneas.
Você pode usar esse parâmetro para limitar a simultaneidade a limitar o uso de CPU e largura de banda local especificando o número máximo de chamadas de rede simultâneas.
O valor especificado é uma contagem absoluta e não é multiplicado pela contagem principal.
Esse parâmetro pode ajudar a reduzir problemas de conexão de rede em ambientes com pouca largura de banda, como 100 kilobits por segundo.
O valor padrão é 10.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Contêiner
Especifica o nome de um contêiner.
Esse cmdlet obtém o status da cópia de um blob no contêiner que esse parâmetro especifica.

```yaml
Type: System.String
Parameter Sets: NamePipeline
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Contexto
Especifica um contexto de armazenamento do Azure.
Para obter um contexto de armazenamento, use o cmdlet New-AzureStorageContext.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -DefaultProfile
As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ServerTimeoutPerRequest
Especifica o intervalo de tempo limite do serviço, em segundos, para uma solicitação.
Se o intervalo especificado decorrer antes de o serviço processar a solicitação, o serviço de armazenamento retornará um erro.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WaitForComplete
Indica que esse cmdlet aguarda a conclusão da cópia.
Se você não especificar esse parâmetro, esse cmdlet retornará um resultado imediatamente.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

### Microsoft. WindowsAzure. Storage. blob. CloudBlob

### Microsoft. WindowsAzure. Storage. blob. CloudBlobContainer

### Microsoft. Azure. Commands. Common. Authentication. Abstractings. IStorageContext

## EXIBE

### Microsoft. WindowsAzure. Commands. Common. Storage. ResourceModel. AzureStorageBlob

## INFORMA

## LINKS RELACIONADOS

[Start-AzureStorageBlobCopy](./Start-AzureStorageBlobCopy.md)

[Parar-AzureStorageBlobCopy](./Stop-AzureStorageBlobCopy.md)


