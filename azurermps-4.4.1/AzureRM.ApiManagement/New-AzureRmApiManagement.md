---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 164C5205-01BA-47BB-B780-D0B9AE614A4B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagement.md
ms.openlocfilehash: 82e09e146999ce0bd320ba398ab2f196f1115688
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431243"
---
# New-AzureRmApiManagement

## Sinopse
Cria uma implantação de gerenciamento de API.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

```
New-AzureRmApiManagement -ResourceGroupName <String> -Name <String> -Location <String> -Organization <String>
 -AdminEmail <String> [-Sku <PsApiManagementSku>] [-Capacity <Int32>] [-VpnType <PsApiManagementVpnType>]
 [-VirtualNetwork <PsApiManagementVirtualNetwork>]
 [-Tags <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-AdditionalRegions <PsApiManagementRegion[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **New-AzureRmApiManagement** cria uma implantação de gerenciamento de API no gerenciamento de APIs do Azure.

## EXEMPLOS

### Exemplo 1: criar um serviço de gerenciamento de API de camada de desenvolvedor
```
PS C:\>New-AzureRmApiManagement -ResourceGroupName "ContosoGroup02" -Name "ContosoApi" -Location "Central US" -Organization "Contoso" -AdminEmail "admin@contoso.com"
```

Esse comando cria um serviço de gerenciamento de API de camada de desenvolvedor.
O comando especifica a organização e o endereço de administrador.
O comando não especifica o parâmetro *SKU* .
Portanto, o cmdlet usa o valor padrão do desenvolvedor.

### Exemplo 2: criar um serviço de camada padrão com três unidades
```
PS C:\>New-AzureRmApiManagement -ResourceGroupName "ContosoGroup02 -Name "ContosoApi" -Location "Central US" -Organization "Contoso" -AdminEmail "admin@contoso.com" -Sku Standard -Capacity 3
```

Esse comando cria um serviço de gerenciamento de API de camada padrão que tem três unidades.

### Exemplo 3: criar um serviço de gerenciamento de API para uma rede virtual externa
```
PS C:\> $virtualNetwork = New-AzureRmApiManagementVirtualNetwork -Location "West US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-b1e8-3726ab15d0e2/resourceGroups/ContosoGroup/providers/Microsoft.Network/virtualNetworks/westUsVirtualNetwork/subnets/backendSubnet"
PS C:\> New-AzureRmApiManagement -ResourceGroupName "ContosoGroup" -Location "West US" -Name "ContosoApi" -Organization Contoso -AdminEmail admin@contoso.com -VirtualNetwork $virtualNetwork -VpnType "External" -Sku "Premium"
```

Esse comando cria um serviço de gerenciamento de API de camada Premium em uma sub-rede de rede virtual do Azure com um ponto de extremidade de gateway externo com uma região mestre nos EUA do oeste.

### Exemplo 4: criar um serviço de gerenciamento de API para uma rede virtual interna
```
PS C:\> $virtualNetwork = New-AzureRmApiManagementVirtualNetwork -Location "West US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-b1e8-3726ab15d0e2/resourceGroups/ContosoGroup/providers/Microsoft.Network/virtualNetworks/westUsVirtualNetwork/subnets/backendSubnet"
PS C:\> New-AzureRmApiManagement -ResourceGroupName "ContosoGroup" -Location "West US" -Name "ContosoApi" -Organization "Contoso" -AdminEmail "admin@contoso.com" -VirtualNetwork $virtualNetwork -VpnType "Internal" -Sku "Premium"
```

Esse comando cria um serviço de gerenciamento de API de camada Premium em uma sub-rede de rede virtual do Azure com um ponto de extremidade de gateway de face interna com uma região mestre nos EUA do oeste.

## OS

### -AdditionalRegions
Regiões de implantação adicionais do gerenciamento de APIs do Azure.

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -AdminEmail
Especifica o endereço de email de origem para todas as notificações que o sistema de gerenciamento de API envia.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Capacidade
Especifica a capacidade de SKU do serviço de gerenciamento de APIs do Azure.
O padrão é um (1).

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Local
Especifica o local em que esse cmdlet cria uma implantação de gerenciamento de API.
Para obter locais válidos, use os cmdlets Get-AzureLocation.

Os valores válidos são: 

- Centro Norte dos EUA
- Centro-Sul dos EUA
- Centro dos EUA
- Oeste da Europa
- Norte da Europa
- Oeste dos EUA
- Leste dos EUA
- Leste dos EUA 2
- Japão oriental
- Oeste do Japão
- Sul do Brasil
- Sudeste Asiático
- Leste da Ásia
- Leste da Austrália
- Sudeste da Austrália

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Nome
Especifica um nome para a implantação de gerenciamento de API.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Organização
Especifica o nome de uma organização.
O gerenciamento de APIs usa esse endereço no portal do desenvolvedor em notificações por email.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Especifica o nome do grupo de recursos sob o qual esse cmdlet cria uma implantação de gerenciamento de API.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SKU
Especifica a camada do serviço de gerenciamento de API.
Os valores válidos são: 

- Event 
- Oficial 
- Gratifica 

O padrão é desenvolvedor.

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSku]
Parameter Sets: (All)
Aliases: 
Accepted values: Developer, Standard, Premium

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Marcas
Especifica um dicionário de marcas.

```yaml
Type: System.Collections.Generic.Dictionary`2[System.String,System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VirtualNetwork
Configuração de rede virtual da região de implantação do gerenciamento de API do Azure mestre.

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VpnType
Tipo de rede virtual da implantação do ApiManagement. Valores válidos são 
- "Nenhum" (valor padrão. O ApiManagement não faz parte de uma rede virtual ")
- "Externo" (a implantação do ApiManagement é configurada dentro de uma rede virtual com um ponto de extremidade voltado para a Internet)
- "Internal" (a implantação do ApiManagement é configurada dentro de uma rede virtual com um ponto de extremidade voltado à intranet)

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVpnType
Parameter Sets: (All)
Aliases: 
Accepted values: None, External, Internal

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

### Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagement

## INFORMA

## LINKS RELACIONADOS

[Backup-AzureRmApiManagement](./Backup-AzureRmApiManagement.md)

[Get-AzureRmApiManagement](./Get-AzureRmApiManagement.md)

[Remove-AzureRmApiManagement](./Remove-AzureRmApiManagement.md)

[Restore-AzureRmApiManagement](./Restore-AzureRmApiManagement.md)


