---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: F20A5FD3-6EC3-4EFE-988C-75F8583961A4
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azstorageblobcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageBlobContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageBlobContent.md
ms.openlocfilehash: d9a602e3e946e28dd04b67c030aeec2aecc3ec93
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93598544"
---
# Set-AzStorageBlobContent

## Sinopse
Carrega um arquivo local em um blob de armazenamento do Azure.

## SYNTAX

### SendManual (padrão)
```
Set-AzStorageBlobContent [-File] <String> [-Container] <String> [-Blob <String>] [-BlobType <String>]
 [-Properties <Hashtable>] [-Metadata <Hashtable>] [-PremiumPageBlobTier <PremiumPageBlobTier>] [-Force]
 [-AsJob] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ContainerPipeline
```
Set-AzStorageBlobContent [-File] <String> [-Blob <String>] -CloudBlobContainer <CloudBlobContainer>
 [-BlobType <String>] [-Properties <Hashtable>] [-Metadata <Hashtable>]
 [-PremiumPageBlobTier <PremiumPageBlobTier>] [-Force] [-AsJob] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### BlobPipeline
```
Set-AzStorageBlobContent [-File] <String> -CloudBlob <CloudBlob> [-BlobType <String>] [-Properties <Hashtable>]
 [-Metadata <Hashtable>] [-PremiumPageBlobTier <PremiumPageBlobTier>] [-Force] [-AsJob]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **set-AzStorageBlobContent** carrega um arquivo local em um blob de armazenamento do Azure.

## EXEMPLOS

### Exemplo 1: carregar um arquivo nomeado
```
PS C:\>Set-AzStorageBlobContent -Container "ContosoUpload" -File ".\PlanningData" -Blob "Planning2015"
```

Esse comando carrega o arquivo chamado PlanningData para um blob chamado Planning2015.

### Exemplo 2: carregar todos os arquivos na pasta atual
```
PS C:\>Get-ChildItem -File -Recurse | Set-AzStorageBlobContent -Container "ContosoUploads"
```

Esse comando usa o cmdlet principal do Windows PowerShell Get-ChildItem para obter todos os arquivos na pasta atual e em subpastas e, em seguida, passá-los para o cmdlet atual usando o operador pipeline.
O cmdlet **set-AzStorageBlobContent** carrega os arquivos para o contêiner chamado ContosoUploads.

### Exemplo 3: substituir um blob existente
```
PS C:\>Get-AzStorageBlob -Container "ContosoUploads" -Blob "Planning2015" | Set-AzStorageBlobContent -File "ContosoPlanning"
```

Esse comando obtém o blob chamado Planning2015 no contêiner ContosoUploads usando o cmdlet Get-AzStorageBlob e, em seguida, passa esse blob para o cmdlet atual.
O comando carrega o arquivo chamado ContosoPlanning como Planning2015.
Esse comando não especifica o parâmetro *Force* .
O comando solicitará confirmação.
Se você confirmar o comando, o cmdlet substituirá o blob existente.

### Exemplo 4: carregar um arquivo em um contêiner usando o pipeline
```
PS C:\>Get-AzStorageContainer -Container "ContosoUpload*" | Set-AzStorageBlobContent -File "ContosoPlanning" -Blob "Planning2015"
```

Esse comando obtém o contêiner que começa com a cadeia de caracteres ContosoUpload usando o cmdlet **Get-AzStorageContainer** e, em seguida, passa esse blob para o cmdlet atual.
O comando carrega o arquivo chamado ContosoPlanning como Planning2015.

### Exemplo 5: carregar um arquivo no BLOB da página com metadados e PremiumPageBlobTier como P10
```
PS C:\>$Metadata = @{"key" = "value"; "name" = "test"}
PS C:\> Set-AzStorageBlobContent -File "ContosoPlanning" -Container "ContosoUploads" -Metadata $Metadata -BlobType Page -PremiumPageBlobTier P10
```

O primeiro comando cria uma tabela de hash que contém metadados para um blob e armazena essa tabela de hash na variável $Metadata.
O segundo comando carrega o arquivo chamado ContosoPlanning para o contêiner chamado ContosoUploads.
O blob inclui os metadados armazenados no $Metadata e tem PremiumPageBlobTier como P10.

### Exemplo 6: carregar um arquivo para blob com propriedades de blob especificadas
```
PS C:\> Set-AzStorageBlobContent -File "ContosoPlanning" -Container "ContosoUploads" -Properties @{"ContentType" = "image/jpeg"; "ContentMD5" = "i727sP7HigloQDsqadNLHw=="}
```

Esse comando carrega o arquivo chamado ContosoPlanning para o contêiner chamado ContosoUploads com as propriedades de blob especificadas.

## OS

### -AsJob
Execute o cmdlet em segundo plano.

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

### -Blob
Especifica o nome de um blob.
Esse cmdlet carrega um arquivo para o blob de armazenamento do Azure que esse parâmetro especifica.

```yaml
Type: System.String
Parameter Sets: SendManual, ContainerPipeline
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -BlobType
Especifica o tipo do blob que esse cmdlet carregará.
Os valores aceitáveis para esse parâmetro são:
- Block
- Página o valor padrão é bloquear.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Block, Page, Append

Required: False
Position: Named
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
Especifica um objeto **CloudBlob** .
Para obter um objeto **CloudBlob** , use o cmdlet Get-AzStorageBlob.

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
Esse cmdlet carrega o conteúdo em um blob no contêiner que esse parâmetro especifica.
Para obter um objeto **CloudBlobContainer** , use o cmdlet Get-AzStorageContainer.

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
Esse cmdlet carrega um arquivo em um blob no contêiner que esse parâmetro especifica.

```yaml
Type: System.String
Parameter Sets: SendManual
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Contexto
Especifica um contexto de armazenamento do Azure.
Para obter um contexto de armazenamento, use o cmdlet New-AzStorageContext.
Para usar um contexto de armazenamento criado a partir de um token SAS sem permissão de leitura, é necessário o parâmetro Add-Force para ignorar a verificação de BLOB.

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
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Arquivo
Especifica um caminho de arquivo local para o carregamento de um arquivo como conteúdo BLOB.

```yaml
Type: System.String
Parameter Sets: SendManual
Aliases: FullName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ContainerPipeline, BlobPipeline
Aliases: FullName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Force
Indica que esse cmdlet substitui um blob existente sem solicitar confirmação.

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

### -Metadados
Especifica metadados para o blob carregado.

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PremiumPageBlobTier
Camada de blob de página

```yaml
Type: Microsoft.WindowsAzure.Storage.Blob.PremiumPageBlobTier
Parameter Sets: (All)
Aliases:
Accepted values: Unknown, P4, P6, P10, P20, P30, P40, P50, P60

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Propriedades
Especifica as propriedades do blob carregado. As propriedades com suporte são: CacheControl, ContentDisposition, ContentEncoding, ContentLanguage, ContentMD5, ContentType.

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

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

### -Confirme
Solicita confirmação antes de executar o cmdlet.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Mostra o que aconteceria se o cmdlet fosse executado.
O cmdlet não é executado.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

### System. String

### Microsoft. WindowsAzure. Storage. blob. CloudBlobContainer

### Microsoft. WindowsAzure. Storage. blob. CloudBlob

### Microsoft. Azure. Commands. Common. Authentication. Abstractings. IStorageContext

## EXIBE

### Microsoft. WindowsAzure. Commands. Common. Storage. ResourceModel. AzureStorageBlob

## INFORMA

## LINKS RELACIONADOS

[Get-AzStorageBlobContent](./Get-AzStorageBlobContent.md)

[Get-AzStorageBlob](./Get-AzStorageBlob.md)

[Remove-AzStorageBlob](./Remove-AzStorageBlob.md)
