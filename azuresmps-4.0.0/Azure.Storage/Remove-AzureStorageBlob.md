---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 03EC0D20-C737-4B2B-B8D9-71D06A938FAD
online version: ''
schema: 2.0.0
ms.openlocfilehash: b40585f584cc8c2634acab54e6862e4163c6b7a7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93426014"
---
# Remove-AzureStorageBlob

## Sinopse
Remove o blob de armazenamento especificado.

## SYNTAX

### NamePipeline (padrão)
```
Remove-AzureStorageBlob [-Blob] <String> [-Container] <String> [-DeleteSnapshot] [-Force] [-PassThru]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### BlobPipeline
```
Remove-AzureStorageBlob -CloudBlob <CloudBlob> [-DeleteSnapshot] [-Force] [-PassThru]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ContainerPipeline
```
Remove-AzureStorageBlob -CloudBlobContainer <CloudBlobContainer> [-Blob] <String> [-DeleteSnapshot] [-Force]
 [-PassThru] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Remove-AzureStorageBlob** remove o blob especificado de uma conta de armazenamento no Azure.

## EXEMPLOS

### Exemplo 1: remover um blob de armazenamento por nome
```
PS C:\>Remove-AzureStorageBlob -Container "ContainerName" -Blob "BlobName"
```

Esse comando Remove um blob identificado pelo nome.

### Exemplo 2: remover um blob de armazenamento usando o pipeline
```
PS C:\>Get-AzureStorageBlob -Container "ContainerName" -Blob "BlobName" | Remove-AzureStorageBlob
```

Esse comando usa o pipeline.

### Exemplo 3: remover blobs de armazenamento usando o pipeline
```
PS C:\>Get-AzureStorageContainer -Container container* | Remove-AzureStorageBlob -Blob "BlobName"
```

Esse comando usa o caractere curinga asterisco (*) e o pipeline para recuperar o BLOB ou BLOBs e, em seguida, remove-os.

## OS

### -Blob
Especifica o nome do blob que você deseja remover.

```yaml
Type: String
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
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CloudBlob
Especifica um blob na nuvem.
Para obter um objeto **CloudBlob** , use o cmdlet Get-AzureStorageBlob.

```yaml
Type: CloudBlob
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
Você pode usar o cmdlet Get-AzureStorageContainer para obtê-lo.

```yaml
Type: CloudBlobContainer
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
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Contêiner
Especifica o nome do contêiner.

```yaml
Type: String
Parameter Sets: NamePipeline
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Contexto
Especifica o contexto de armazenamento do Azure.
Você pode usar o cmdlet New-AzureStorageContext para criá-lo.

```yaml
Type: IStorageContext
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -DeleteSnapshot
Especifica que todos os instantâneos serão excluídos, mas não o blob base.
Se esse parâmetro não for especificado, o blob base e seus instantâneos serão excluídos juntos.
O usuário será solicitado a confirmar a operação de exclusão.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force
Indica que esse cmdlet Remove o blob e seu instantâneo sem confirmação.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PassThru
Indica que esse cmdlet retorna um **booliano** que reflete o sucesso da operação.
Por padrão, esse cmdlet não retorna um valor.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ServerTimeoutPerRequest
Especifica o perfil do Azure para o cmdlet ler.
Se não for especificado, o cmdlet lerá do perfil padrão.

```yaml
Type: Int32
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
Type: SwitchParameter
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
Type: SwitchParameter
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

## EXIBE

## INFORMA

## LINKS RELACIONADOS

[Get-AzureStorageBlob](./Get-AzureStorageBlob.md)

[Get-AzureStorageBlobContent](./Get-AzureStorageBlobContent.md)

[Set-AzureStorageBlobContent](./Set-AzureStorageBlobContent.md)
