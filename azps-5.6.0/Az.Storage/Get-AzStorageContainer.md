---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 90C3DF13-0010-49B6-A8CD-C6AC34BC3EFA
online version: https://docs.microsoft.com/powershell/module/az.storage/get-azstoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageContainer.md
ms.openlocfilehash: 15aefebea30e829371c57c3c1cd575a604b81eaf
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889077"
---
# Get-AzStorageContainer

## SYNOPSIS
Lista os contêineres de armazenamento.

## SINTAXE

### ContainerName (Padrão)
```
Get-AzStorageContainer [[-Name] <String>] [-MaxCount <Int32>] [-ContinuationToken <BlobContinuationToken>]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### ContainerPrefix
```
Get-AzStorageContainer -Prefix <String> [-MaxCount <Int32>] [-ContinuationToken <BlobContinuationToken>]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## DESCRIPTION
O cmdlet **Get-AzStorageContainer** lista os contêineres de armazenamento associados à conta de armazenamento no Azure.

## EXEMPLOS

### Exemplo 1: Obter blob de armazenamento do Azure pelo nome
```
PS C:\>Get-AzStorageContainer -Name container*
```

Este exemplo usa um caractere curinga para retornar uma lista de todos os contêineres com um nome que começa com contêiner.

### Exemplo 2: Obter contêiner de armazenamento do Azure pelo prefixo de nome do contêiner
```
PS C:\>Get-AzStorageContainer -Prefix "container"
```

Este exemplo usa o *parâmetro Prefix* para retornar uma lista de todos os contêineres com um nome que começa com contêiner.

## PARÂMETROS

### -ClientTimeoutPerRequest
Especifica o intervalo de tempo de tempo do lado do cliente, em segundos, para uma solicitação de serviço.
Se a chamada anterior falhar no intervalo especificado, esse cmdlet recuperará a solicitação.
Se esse cmdlet não receber uma resposta bem-sucedida antes que o intervalo se esgote, este cmdlet retornará um erro.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: ClientTimeoutPerRequestInSeconds

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ConcurrentTaskCount
Especifica o máximo de chamadas de rede simultâneas.
Você pode usar esse parâmetro para limitar a capacidade de limitar o uso de CPU local e largura de banda especificando o número máximo de chamadas de rede simultâneas.
O valor especificado é uma contagem absoluta e não é multiplicado pela contagem principal.
Esse parâmetro pode ajudar a reduzir problemas de conexão de rede em ambientes de baixa largura de banda, como 100 quilobits por segundo.
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

### -Context
Especifica o contexto de armazenamento.
Para criar, você pode usar o cmdlet New-AzStorageContext.
As permissões de contêiner não serão recuperadas quando você usar um contexto de armazenamento criado a partir do Token SAS, pois as permissões do contêiner de consulta exigem a permissão da chave de conta de armazenamento.

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

### -ContinuationToken
Especifica um token de continuação para a lista de blob.

```yaml
Type: Microsoft.Azure.Storage.Blob.BlobContinuationToken
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.

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

### -MaxCount
Especifica o número máximo de objetos que este cmdlet retorna.

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

### -Name
Especifica o nome do contêiner.
Se o nome do contêiner estiver vazio, o cmdlet lista todos os contêineres.
Caso contrário, lista todos os contêineres que corresponderem ao nome especificado ou ao padrão de nome regular.

```yaml
Type: System.String
Parameter Sets: ContainerName
Aliases: N, Container

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -Prefix
Especifica um prefixo usado no nome do contêiner ou contêineres que você deseja obter.
Você pode usar isso para encontrar todos os contêineres que começam com a mesma cadeia de caracteres, como "my" ou "test".

```yaml
Type: System.String
Parameter Sets: ContainerPrefix
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ServerTimeoutPerRequest
Especifica o intervalo de tempo de serviço, em segundos, para uma solicitação.
Se o intervalo especificado se elapse antes que o serviço processe a solicitação, o serviço de armazenamento retornará um erro.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: ServerTimeoutPerRequestInSeconds

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUTS

### System.String

### Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext

## SAÍDAS

### Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageContainer

## NOTES

## LINKS RELACIONADOS

[New-AzStorageContainer](./New-AzStorageContainer.md)

[Remove-AzStorageContainer](./Remove-AzStorageContainer.md)

[Set-AzStorageContainerAcl](./Set-AzStorageContainerAcl.md)


