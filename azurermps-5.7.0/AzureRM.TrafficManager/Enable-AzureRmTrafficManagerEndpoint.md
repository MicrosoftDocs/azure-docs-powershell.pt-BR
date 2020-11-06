---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM
ms.assetid: 32263236-C207-4FE0-AB8A-018118FC7729
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.trafficmanager/enable-azurermtrafficmanagerendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Enable-AzureRmTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Enable-AzureRmTrafficManagerEndpoint.md
ms.openlocfilehash: 9412a75ff595424637b36fb64db82ba556c9a057
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432372"
---
# Enable-AzureRmTrafficManagerEndpoint

## Sinopse
Habilita um ponto de extremidade em um perfil do Gerenciador de tráfego.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

### Campos
```
Enable-AzureRmTrafficManagerEndpoint -Name <String> -Type <String> -ProfileName <String>
 -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Objeto
```
Enable-AzureRmTrafficManagerEndpoint -TrafficManagerEndpoint <TrafficManagerEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Enable-AzureRmTrafficManagerEndpoint** habilita um ponto de extremidade em um perfil do Gerenciador de tráfego do Azure.

Você pode usar o operador pipeline para passar um objeto **TrafficManagerEndpoint** para esse cmdlet ou pode especificar um objeto **TrafficManagerEndpoint** usando o parâmetro *TrafficManagerEndpoint* .

Você também pode especificar o nome e o tipo de ponto de extremidade usando os parâmetros *Name* e *Type* , juntamente com os parâmetros *ProfileName* e *ResourceGroupName* .

## EXEMPLOS

### Exemplo 1: habilitar um ponto de extremidade de um perfil
```
PS C:\>Enable-AzureRmTrafficManagerEndpoint -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName ResourceGroup11 -Type ExternalEndpoints
```

Esse comando habilita o ponto de extremidade externo chamado contoso no perfil chamado ContosoProfile na ResouceGroup11 do grupo de recursos.

### Exemplo 2: habilitar um ponto de extremidade usando o pipeline
```
PS C:\>Get-AzureRmTrafficManagerEndpoint -Name "contoso" -Type ExternalEndpoints -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" | Enable-AzureRmTrafficManagerEndpoint
```

Esse comando obtém o ponto de extremidade externo chamado contoso do perfil chamado ContosoProfile em ResourceGroup11.
Em seguida, o comando passa esse ponto de extremidade para o cmdlet **Enable-AzureRmTrafficManagerEndpoint** usando o operador pipeline.
Esse cmdlet habilita esse ponto de extremidade.

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
Especifica o nome do ponto de extremidade do Gerenciador de tráfego que o cmdlet habilita.

```yaml
Type: String
Parameter Sets: Fields
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ProfileName
Especifica o nome de um perfil do Gerenciador de tráfego no qual esse cmdlet habilita um ponto de extremidade.
Para obter um perfil, use o cmdlet Get-AzureRmTrafficManagerProfile.

```yaml
Type: String
Parameter Sets: Fields
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Especifica o nome de um grupo de recursos.
Esse cmdlet habilita um ponto de extremidade do Gerenciador de tráfego no grupo que esse parâmetro especifica.

```yaml
Type: String
Parameter Sets: Fields
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TrafficManagerEndpoint
Especifica o ponto de extremidade do Gerenciador de tráfego que este cmdlet habilita.
Para obter um objeto **TrafficManagerEndpoint** , use o cmdlet Get-AzureRmTrafficManagerEndpoint.

```yaml
Type: TrafficManagerEndpoint
Parameter Sets: Object
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Digite
Especifica o tipo de ponto de extremidade que esse cmdlet desabilita no perfil do Gerenciador de tráfego.
Os valores válidos são: 

- AzureEndpoints
- ExternalEndpoints
- NestedEndpoints

```yaml
Type: String
Parameter Sets: Fields
Aliases: 
Accepted values: AzureEndpoints, ExternalEndpoints, NestedEndpoints

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

### TrafficManagerEndpoint
O parâmetro ' TrafficManagerEndpoint ' aceita o valor do tipo ' TrafficManagerEndpoint ' do pipeline

## EXIBE

### System. Boolean

## INFORMA

## LINKS RELACIONADOS

[Disable-AzureRmTrafficManagerEndpoint](./Disable-AzureRmTrafficManagerEndpoint.md)

[Get-AzureRmTrafficManagerEndpoint](./Get-AzureRmTrafficManagerEndpoint.md)

[Get-AzureRmTrafficManagerProfile](./Get-AzureRmTrafficManagerProfile.md)

[New-AzureRmTrafficManagerEndpoint](./New-AzureRmTrafficManagerEndpoint.md)

[New-AzureRmTrafficManagerProfile](./New-AzureRmTrafficManagerProfile.md)

[Remove-AzureRmTrafficManagerEndpoint](./Remove-AzureRmTrafficManagerEndpoint.md)

[Set-AzureRmTrafficManagerProfile](./Set-AzureRmTrafficManagerProfile.md)


