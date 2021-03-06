---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 07811B64-6A77-452C-B148-DE8C13E73DEF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/get-azurebatchremoteloginsettings
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchRemoteLoginSettings.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchRemoteLoginSettings.md
ms.openlocfilehash: 01ded3d4e9d77edac39e7c632f46d6e7ecf9eeb5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427691"
---
# Get-AzureBatchRemoteLoginSettings

## Sinopse
Obtém as configurações de logon remoto para um nó de computação.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

### ID (padrão)
```
Get-AzureBatchRemoteLoginSettings [-PoolId] <String> [-ComputeNodeId] <String>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### InputObject
```
Get-AzureBatchRemoteLoginSettings [[-ComputeNode] <PSComputeNode>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Get-AzureBatchRemoteLoginSettings** Obtém as configurações de logon remoto para um nó de computação em um pool baseado em infraestrutura de máquinas virtuais.

## EXEMPLOS

### Exemplo 1: obter configurações de logon remoto para todos os nós em um pool
```
PS C:\>$Context = Get-AzureRmBatchAccountKeys -AccountName "ContosoBatchAccount"
PS C:\> Get-AzureBatchComputeNode -PoolId "ContosoPool" -BatchContext $Context | Get-AzureBatchRemoteLoginSettings -BatchContext $Context
IPAddress       Port
---------       ----
10.214.75.221   50002
10.214.75.221   50001
10.214.75.221   50000
```

O primeiro comando obtém um contexto de conta em lotes que contém as chaves de acesso para a sua assinatura usando **Get-AzureRmBatchAccountKeys**.
O comando armazena o contexto na variável $Context para usar no próximo comando.

O segundo comando obtém cada nó de computação no pool que tem o ID ContosoPool usando **Get-AzureBatchComputeNode**.
O comando passa cada nó de computador para o cmdlet atual usando o operador pipeline.
O comando obtém as configurações de logon remoto para cada nó de computação.

### Exemplo 2: obter configurações de logon remoto para um nó
```
PS C:\>$Context = Get-AzureRmBatchAccountKeys -AccountName "ContosoBatchAccount"
PS C:\> Get-AzureBatchRemoteLoginSettings -PoolId "ContosoPool" -ComputeNodeId "tvm-1900272697_1-20150330t205553z" -BatchContext $Context
IPAddress       Port
---------       ----
10.214.75.221   50000
```

O primeiro comando obtém um contexto de conta em lotes que contém as teclas de acesso para a sua assinatura e, em seguida, armazena-a na variável $Context.

O segundo comando obtém as configurações de logon remoto para o nó de computação com a ID especificada no pool que tem a ID ContosoPool.

## OS

### -BatchContext
Especifica a instância **BatchAccountContext** que este cmdlet usa para interagir com o serviço em lotes.
Para obter um **BatchAccountContext** que contenha as teclas de acesso para a sua assinatura, use o cmdlet Get-AzureRmBatchAccountKeys.

```yaml
Type: BatchAccountContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ComputeNode
Especifica um nó de computação, como um objeto **PSComputeNode** , para o qual esse cmdlet obtém as configurações de logon remoto.
Para obter um objeto do nó de computação, use o cmdlet Get-AzureBatchComputeNode.

```yaml
Type: PSComputeNode
Parameter Sets: InputObject
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ComputeNodeId
Especifica a ID do nó de computação para a qual obter as configurações de logon remoto.
para o qual este cmdlet obtém as configurações de logon remoto.

```yaml
Type: String
Parameter Sets: Id
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Poolid
Especifica a ID do pool que contém a máquina virtual.

```yaml
Type: String
Parameter Sets: Id
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

### BatchAccountContext
O parâmetro ' BatchContext ' aceita o valor do tipo ' BatchAccountContext ' do pipeline

### PSComputeNode
O parâmetro ' ComputeNode ' aceita o valor do tipo ' PSComputeNode ' do pipeline

## EXIBE

### PSRemoteLoginSettings

## INFORMA

## LINKS RELACIONADOS

[Get-AzureRmBatchAccountKeys](./Get-AzureRmBatchAccountKeys.md)

[Get-AzureBatchComputeNode](./Get-AzureBatchComputeNode.md)

[Get-AzureBatchRemoteDesktopProtocolFile](./Get-AzureBatchRemoteDesktopProtocolFile.md)

[Cmdlets do Azure batch](./AzureRM.Batch.md)


