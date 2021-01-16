---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azstorageobjectreplicationpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageObjectReplicationPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageObjectReplicationPolicy.md
ms.openlocfilehash: bf8d7aade5eeeafc2c3a78e4cdfed5df2d733006
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98271310"
---
# Set-AzStorageObjectReplicationPolicy

## Sinopse
Cria ou atualiza a política de replicação de objetos especificada em uma conta de armazenamento.

## SYNTAX

### AccountName (padrão)
```
Set-AzStorageObjectReplicationPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-PolicyId <String>] -SourceAccount <String> [-DestinationAccount <String>]
 -Rule <PSObjectReplicationPolicyRule[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### Políticaobject
```
Set-AzStorageObjectReplicationPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -InputObject <PSObjectReplicationPolicy> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### Accountobject
```
Set-AzStorageObjectReplicationPolicy -StorageAccount <PSStorageAccount> [-PolicyId <String>]
 -SourceAccount <String> [-DestinationAccount <String>] -Rule <PSObjectReplicationPolicyRule[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **set-AzStorageObjectReplicationPolicy** cria ou atualiza a política de replicação de objetos especificada em uma conta de armazenamento.

## EXEMPLOS

### Exemplo 1: definir a política de replicação de objetos para a conta de destino e de origem.
```
PS C:\> $rule1 = New-AzStorageObjectReplicationPolicyRule -SourceContainer src1 -DestinationContainer dest1 

PS C:\> $rule2 = New-AzStorageObjectReplicationPolicyRule -SourceContainer src -DestinationContainer dest -MinCreationTime 2019-01-01T16:00:00Z -PrefixMatch a,abc,dd

PS C:\> $destPolicy = Set-AzStorageObjectReplicationPolicy -ResourceGroupName "myresourcegroup" -AccountName "mydestaccount" -PolicyId default -SourceAccount $srcAccountName  -Rule $rule1,$rule2

PS C:\> $destPolicy

ResourceGroupName StorageAccountName PolicyId                             EnabledTime SourceAccount   DestinationAccount Rules                                     
----------------- ------------------ --------                             ----------- -------------   ------------------ -----   
myresourcegroup   mydestaccount      56bfa11c-81ef-4f8d-b307-5e5386e16fba             mysourceaccount mydestaccount      [5fa8b1d6-4985-4abd-a0b3-ec4d07295a43,...]

PS C:\> Set-AzStorageObjectReplicationPolicy -ResourceGroupName "myresourcegroup" -AccountName "mysourceaccount" -InputObject $destPolicy

ResourceGroupName StorageAccountName PolicyId                             EnabledTime SourceAccount   DestinationAccount Rules                                     
----------------- ------------------ --------                             ----------- -------------   ------------------ -----                                     
myresourcegroup   mysourceaccount    56bfa11c-81ef-4f8d-b307-5e5386e16fba             mysourceaccount mydestaccount      [5fa8b1d6-4985-4abd-a0b3-ec4d07295a43,...]
```

Este comando define a política de replicação de objetos para a conta de destino e de origem.
Primeiro, crie duas regras de política de replicação de objetos e defina a política com as 2 regras para a conta de destino. Em seguida, defina a política de replicação de objeto da conta de destino para a conta de origem.

## OS

### -DefaultProfile
As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DestinationAccount
Política de replicação de objeto DestinationAccount.

```yaml
Type: System.String
Parameter Sets: AccountName, AccountObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
Objeto de política de replicação de objeto a ser definido para a conta especificada.

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSObjectReplicationPolicy
Parameter Sets: PolicyObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -PolicyId
ID da política de replicação de objetos. Ele deve ser um GUID ou ' default '.
Se não inserir PolicyId, usará ' default ', o que significa criar uma nova política e a ID da nova política será retornada na política criada.

```yaml
Type: System.String
Parameter Sets: AccountName, AccountObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Nome do grupo de recursos.

```yaml
Type: System.String
Parameter Sets: AccountName, PolicyObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Regra
Regras de política de replicação de objetos.

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSObjectReplicationPolicyRule[]
Parameter Sets: AccountName, AccountObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SourceAccount
Política de replicação de objeto SourceAccount.

```yaml
Type: System.String
Parameter Sets: AccountName, AccountObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StorageAccount
Objeto da conta de armazenamento

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount
Parameter Sets: AccountObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -StorageAccountName
Nome da conta de armazenamento.

```yaml
Type: System.String
Parameter Sets: AccountName, PolicyObject
Aliases: AccountName

Required: True
Position: 1
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
Default value: None
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
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

### Microsoft. Azure. Commands. Management. Storage. Models. PSStorageAccount

### Microsoft. Azure. Commands. Management. Storage. Models. PSObjectReplicationPolicy

## EXIBE

### Microsoft. Azure. Commands. Management. Storage. Models. PSObjectReplicationPolicy

## INFORMA

## LINKS RELACIONADOS
