---
external help file: Microsoft.Azure.Commands.ContainerInstance.dll-Help.xml
Module Name: AzureRM.ContainerInstance
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerinstance/get-azurermcontainergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerInstance/Commands.ContainerInstance/help/Get-AzureRmContainerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerInstance/Commands.ContainerInstance/help/Get-AzureRmContainerGroup.md
ms.openlocfilehash: 665fcc30b0b9c2769af66ae4a590f3526438cae6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93426755"
---
# Get-AzureRmContainerGroup

## Sinopse
Obtém grupos de contêineres.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

### ListContainerGroupParamSet (padrão)
```
Get-AzureRmContainerGroup [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### GetContainerGroupInResourceGroupParamSet
```
Get-AzureRmContainerGroup [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### GetContainerGroupByResourceIdParamSet
```
Get-AzureRmContainerGroup -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Get-AzureRmContainerGroup** Obtém um grupo de contêiner específico ou todos os grupos de contêineres em um grupo de recursos ou a assinatura.

## EXEMPLOS

### Exemplo 1: Obtém um grupo de contêineres especificado
```
PS C:\> Get-AzureRmContainerGroup -ResourceGroupName demo -Name mycontainer

ResourceGroupName        : demo
Id                       : /subscriptions/ae43b1e3-c35d-4c8c-bc0d-f148b4c52b78/resourceGroups/demo/providers/Microsoft.ContainerInstance/containerGroups/mycontainer
Name                     : mycontainer
Type                     : Microsoft.ContainerInstance/containerGroups
Location                 : westus
Tags                     :
ProvisioningState        : Succeeded
Containers               : {mycontainer}
ImageRegistryCredentials :
RestartPolicy            :
IpAddress                : 13.88.10.240
Ports                    : {8000}
OsType                   : Linux
Volumes                  :
State                    : Running
Events                   : {}
```

O comando obtém o grupo de contêineres especificado.

### Exemplo 2: Obtém grupos de contêineres em um grupo de recursos
```
PS C:\> Get-AzureRmContainerGroup -ResourceGroupName demo

ResourceGroupName Name                     Location   OsType  Image                         IP                   Resources        ProvisioningState
----------------- ----                     --------   ------  -----                         --                   ---------        -----------------
demo              container1               west us    Linux   alpine:latest                 40.83.144.50:8002    1 cores/1 gb             Succeeded
demo              container2               west us    Linux   alpine:latest                 104.42.228.253:8001  1 cores/1 gb             Succeeded
```

O comando obtém os grupos de contêineres no grupo de recursos `demo` .

### Exemplo 3: Obtém grupos de contêineres na assinatura atual
```
PS C:\> Get-AzureRmContainerGroup

ResourceGroupName Name                     Location   OsType  Image                         IP                   Resources        ProvisioningState
----------------- ----                     --------   ------  -----                         --                   ---------        -----------------
demo1             container1               west us    Linux   alpine:latest                 40.83.144.50:8002    1 cores/1 gb             Succeeded
demo2             container2               west us    Linux   alpine:latest                 104.42.228.253:8001  1 cores/1 gb             Succeeded
```

O comando obtém os grupos de contêineres na assinatura atual.

### Exemplo 4: Obtém grupos de contêineres usando a ID do recurso.
```
PS C:\> Find-AzureRmResource -ResourceGroupEquals demo -ResourceNameEquals mycontainer | Get-AzureRmContainerGroup

ResourceGroupName        : demo
Id                       : /subscriptions/ae43b1e3-c35d-4c8c-bc0d-f148b4c52b78/resourceGroups/demo/providers/Microsoft.ContainerInstance/containerGroups/mycontainer
Name                     : mycontainer
Type                     : Microsoft.ContainerInstance/containerGroups
Location                 : westus
Tags                     :
ProvisioningState        : Succeeded
Containers               : {mycontainer}
ImageRegistryCredentials :
RestartPolicy            :
IpAddress                : 13.88.10.240
Ports                    : {8000}
OsType                   : Linux
Volumes                  :
State                    : Running
Events                   : {}
```

O comando obtém o grupo de contêineres com a ID do recurso.

## OS

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

### -Nome
O nome do grupo de contêineres.

```yaml
Type: String
Parameter Sets: GetContainerGroupInResourceGroupParamSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
O nome do grupo de recursos.

```yaml
Type: String
Parameter Sets: ListContainerGroupParamSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: GetContainerGroupInResourceGroupParamSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceId
A ID do recurso.

```yaml
Type: String
Parameter Sets: GetContainerGroupByResourceIdParamSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

### System. String

## EXIBE

### Microsoft. Azure. Commands. ContainerInstance. Models. PSContainerGroup

## INFORMA

## LINKS RELACIONADOS
