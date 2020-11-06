---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: FE7689DE-4EC6-4C6B-94A4-D22C61CA569D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchComputeNodeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchComputeNodeUser.md
ms.openlocfilehash: 6289aa916b4d03559fccb11ea0a8897f4b506b53
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431153"
---
# New-AzureBatchComputeNodeUser

## Sinopse
Cria uma conta de usuário em um nó de computação em lotes.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

### %
```
New-AzureBatchComputeNodeUser [-PoolId] <String> [-ComputeNodeId] <String> -Name <String> -Password <String>
 [-ExpiryTime <DateTime>] [-IsAdmin] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ParentObject
```
New-AzureBatchComputeNodeUser [[-ComputeNode] <PSComputeNode>] -Name <String> -Password <String>
 [-ExpiryTime <DateTime>] [-IsAdmin] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **New-AzureBatchComputeNodeUser** cria uma conta de usuário em um nó de computação em lotes do Azure.

## EXEMPLOS

### Exemplo 1: criar uma conta de usuário que tenha credenciais administrativas
```
PS C:\>New-AzureBatchComputeNodeUser -PoolId "MyPool01" -ComputeNodeId "ComputeNode01" -Name "TestUser" -Password "Password" -ExpiryTime ([DateTime]::Now.AddDays(7)) -IsAdmin -BatchContext $Context
```

Esse comando cria uma conta de usuário no nó de computação que tem a ID ComputeNode01.
O nó está no pool que tem a ID MyPool01.
O nome de usuário é testuser, a senha é password, a conta expira em sete dias e a conta tem credenciais administrativas.

### Exemplo 2: criar uma conta de usuário em um nó de computação usando o pipeline
```
PS C:\>Get-AzureBatchComputeNode "MyPool01" -ComputeNodeId "ComputeNode01" -BatchContext $Context | New-AzureBatchComputeNodeUser -Name "TestUser" -Password "Password" -BatchContext $Context
```

Esse comando obtém o nó de computação chamado ComputeNode01 usando o cmdlet **Get-AzureBatchComputeNode** .
Esse nó está no pool que tem a ID MyPool01.
O comando passa aquele nó COMPUTE para o cmdlet atual usando o operador pipeline.
O comando cria uma conta de usuário com o nome de usuário TestUserand a senha.

## OS

### -BatchContext
Especifica a instância **BatchAccountContext** que este cmdlet usa para interagir com o serviço em lotes.
Para obter um objeto **BatchAccountContext** que contém as teclas de acesso para a sua assinatura, use o cmdlet Get-AzureRmBatchAccountKeys.

```yaml
Type: Microsoft.Azure.Commands.Batch.BatchAccountContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ComputeNode
Especifica o nó de computação, como um objeto **PSComputeNode** , em que esse cmdlet cria uma conta de usuário.

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSComputeNode
Parameter Sets: ParentObject
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ComputeNodeId
Especifica a ID do nó de computação em que esse cmdlet cria uma conta de usuário.

```yaml
Type: System.String
Parameter Sets: Id
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ExpiryTime
Especifica o tempo de expiração da nova conta de usuário.

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ISAdmin
Indica que o cmdlet cria uma conta de usuário que tem credenciais administrativas.

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

### -Nome
Especifica o nome da nova conta local do Windows.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Senha
Especifica a senha da conta de usuário.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Poolid
Especifica a ID do pool que contém o nó de computação no qual criar a conta de usuário.

```yaml
Type: System.String
Parameter Sets: Id
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
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

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

### BatchAccountContext
O parâmetro ' BatchContext ' aceita o valor do tipo ' BatchAccountContext ' do pipeline

### PSComputeNode
O parâmetro ' ComputeNode ' aceita o valor do tipo ' PSComputeNode ' do pipeline

## EXIBE

## INFORMA

## LINKS RELACIONADOS

[Get-AzureRmBatchAccountKeys](./Get-AzureRmBatchAccountKeys.md)

[Get-AzureBatchComputeNode](./Get-AzureBatchComputeNode.md)

[Remove-AzureBatchComputeNodeUser](./Remove-AzureBatchComputeNodeUser.md)

[Cmdlets do Azure batch](./AzureRM.Batch.md)


