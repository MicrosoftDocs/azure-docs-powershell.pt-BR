---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/New-AzureRmContainerRegistry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/New-AzureRmContainerRegistry.md
ms.openlocfilehash: 232d767130b789f61d7e4e21fa0bc7c0737c58dc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428254"
---
# New-AzureRmContainerRegistry

## Sinopse
Cria um registro de contêineres.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

```
New-AzureRmContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-Sku] <String>
 [-Location <String>] [-EnableAdminUser] [-Tag <Hashtable>] [-StorageAccountName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **New-AzureRmContainerRegistry** cria um registro do contêiner.

## EXEMPLOS

### Exemplo 1: criar um registro de contêiner com uma nova conta de armazenamento.
```
PS C:\>New-AzureRmContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -Sku "Basic"

Id                 : /subscriptions/3eb31d8d-2879-4706-89b4-4dc4047726c6/resourceGroups/MyResourceGroup/providers/Microsoft.ContainerRegistry/registries/MyRegistry
ResourceGroupName  : MyResourceGroup
Name               : MyRegistry
Type               : Microsoft.ContainerRegistry/registries
Location           : westus
Tags               : {}
SkuName            : Basic
SkuTier            : Basic
LoginServer        : myregistry.azurecr.io
CreationDate       : 4/13/2017 3:48:57 PM
ProvisioningState  : Succeeded
AdminUserEnabled   : False
StorageAccountName : myregistry154817
```

Esse comando cria um registro de contêiner com uma nova conta de armazenamento no grupo de recursos `MyResourceGroup` .

### Exemplo 2: criar um registro de contêiner com o usuário administrador habilitado.
```
PS C:\>New-AzureRmContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -Sku "Basic" -EnableAdminUser

Id                 : /subscriptions/3eb31d8d-2879-4706-89b4-4dc4047726c6/resourceGroups/MyResourceGroup/providers/Microsoft.ContainerRegistry/registries/MyRegistry
ResourceGroupName  : MyResourceGroup
Name               : MyRegistry
Type               : Microsoft.ContainerRegistry/registries
Location           : westus
Tags               : {}
SkuName            : Basic
SkuTier            : Basic
LoginServer        : myregistry.azurecr.io
CreationDate       : 4/13/2017 3:48:57 PM
ProvisioningState  : Succeeded
AdminUserEnabled   : True
StorageAccountName : myregistry154817
```

Esse comando cria um registro de contêiner com o usuário administrador habilitado.

### Exemplo 3: criar um registro de contêiner com uma conta de armazenamento existente.
```
PS C:\>New-AzureRmContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -Sku "Basic" -StorageAccountName "mystorageaccount"

Id                 : /subscriptions/3eb31d8d-2879-4706-89b4-4dc4047726c6/resourceGroups/MyResourceGroup/providers/Microsoft.ContainerRegistry/registries/MyRegistry
ResourceGroupName  : MyResourceGroup
Name               : MyRegistry
Type               : Microsoft.ContainerRegistry/registries
Location           : westus
Tags               : {}
SkuName            : Basic
SkuTier            : Basic
LoginServer        : myregistry.azurecr.io
CreationDate       : 4/13/2017 3:48:57 PM
ProvisioningState  : Succeeded
AdminUserEnabled   : False
StorageAccountName : mystorageaccount
```

Esse comando cria um registro de contêiner com uma conta de armazenamento existente `mystorageaccount` na mesma assinatura.

## OS

### -EnableAdminUser
Habilite o usuário administrador para o registro do contêiner.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: EnableAdmin

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Local
Local do registro do contêiner.
Padrão para o local do grupo de recursos.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Nome
Nome do registro do contêiner.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ContainerRegistryName, RegistryName, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Nome do grupo de recursos.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SKU
SKU do registro do contêiner.
Valores permitidos: Basic.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ContainerRegistrySku, RegistrySku
Accepted values: Basic

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StorageAccountName
O nome de uma conta de armazenamento existente.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Marca
Marcas de registro de contêineres. pares de chave-valor na forma de uma tabela de hash. Por exemplo:

@ {Key0 = "value0"; key1 = $null; Key2 = "value2"}

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

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

## EXIBE

### Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistry

## INFORMA

## LINKS RELACIONADOS

[Get-AzureRmContainerRegistry](./Get-AzureRmContainerRegistry.md)

[Update-AzureRmContainerRegistry](./Update-AzureRmContainerRegistry.md)

[Remove-AzureRmContainerRegistry](./Remove-AzureRmContainerRegistry.md)
