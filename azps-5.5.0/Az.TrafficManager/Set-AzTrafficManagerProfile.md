---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 975DD42E-61B6-437B-884D-C15A8DB7A667
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/set-aztrafficmanagerprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Set-AzTrafficManagerProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Set-AzTrafficManagerProfile.md
ms.openlocfilehash: 8f774ab221160a94ee4e8b5f13780b7e3131f252
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112357"
---
# Set-AzTrafficManagerProfile

## Sinopse
Atualiza um perfil do Gerenciador de Tráfego.

## Sintaxe

```
Set-AzTrafficManagerProfile -TrafficManagerProfile <TrafficManagerProfile>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Descrição
O cmdlet **Set-AzTrafficManagerProfile** atualiza um perfil do Gerenciador de Tráfego do Azure.
Este cmdlet atualiza as configurações do perfil de um objeto de perfil local.
Você pode especificar o objeto de perfil usando o parâmetro *TrafficManagerProfile* ou usando o pipeline.

Você pode obter um objeto local que representa um perfil usando Get-AzTrafficManagerProfile cmdlet.
Modifique o objeto localmente e use **Set-AzTrafficManagerProfile** para comprometer suas alterações.

## Exemplos

### Exemplo 1: Atualizar um perfil
```
PS C:\>$TrafficManagerProfile = Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11" 
PS C:\> $TrafficManagerProfile.ProfileStatus = Disabled
PS C:\> Set-AzTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

O primeiro comando obtém um perfil do Gerenciador de Tráfego do Azure usando Get-AzTrafficManagerProfile cmdlet.
O comando armazena o perfil localmente na variável $TrafficManagerProfile dados.

O segundo comando altera esse perfil localmente.
Esse comando desabilita o perfil.

O terceiro comando atualiza o perfil do Gerenciador de Tráfego chamado ContosoProfile para corresponder ao valor local no $TrafficManagerProfile.

## Parâmetros

### -DefaultProfile
As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.

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

### -TrafficManagerProfile
Especifica um objeto **TrafficManagerProfile** local.
Este cmdlet atualiza o Gerenciador de Tráfego para corresponder a este objeto local.

```yaml
Type: Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## Entradas

### Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile

## Saídas

### Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile

## Notas

## LINKS RELACIONADOS

[Add-AzTrafficManagerEndpointConfig](./Add-AzTrafficManagerEndpointConfig.md)

[Get-AzTrafficManagerProfile](./Get-AzTrafficManagerProfile.md)

[New-AzTrafficManagerProfile](./New-AzTrafficManagerProfile.md)

[Remove-AzTrafficManagerEndpointConfig](./Remove-AzTrafficManagerEndpointConfig.md)

[Remove-AzTrafficManagerProfile](./Remove-AzTrafficManagerProfile.md)


