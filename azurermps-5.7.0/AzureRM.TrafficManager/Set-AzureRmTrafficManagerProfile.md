---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM
ms.assetid: 975DD42E-61B6-437B-884D-C15A8DB7A667
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.trafficmanager/set-azurermtrafficmanagerprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Set-AzureRmTrafficManagerProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Set-AzureRmTrafficManagerProfile.md
ms.openlocfilehash: 58811a34a2f3d2b4684813c42723a5cab354a13f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432853"
---
# Set-AzureRmTrafficManagerProfile

## Sinopse
Atualiza um perfil do Gerenciador de tráfego.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

```
Set-AzureRmTrafficManagerProfile -TrafficManagerProfile <TrafficManagerProfile>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **set-AzureRmTrafficManagerProfile** atualiza um perfil do Gerenciador de tráfego do Azure.
Esse cmdlet atualiza as configurações do perfil de um objeto de perfil local.
Você pode especificar o objeto de perfil usando o parâmetro *TrafficManagerProfile* ou usando o pipeline.

Você pode obter um objeto local que representa um perfil usando o cmdlet Get-AzureRmTrafficManagerProfile.
Modifique o objeto localmente e use **set-AzureRmTrafficManagerProfile** para confirmar as alterações.

## EXEMPLOS

### Exemplo 1: atualizar um perfil
```
PS C:\>$TrafficManagerProfile = Get-AzureRmTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11" 
PS C:\> $TrafficManagerProfile.ProfileStatus = Disabled
PS C:\> Set-AzureRmTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

O primeiro comando obtém um perfil do Gerenciador de tráfego do Azure usando o cmdlet Get-AzureRmTrafficManagerProfile.
O comando armazena o perfil localmente na variável $TrafficManagerProfile.

O segundo comando altera esse perfil localmente.
Esse comando desabilita o perfil.

O terceiro comando atualiza o perfil do Gerenciador de tráfego chamado ContosoProfile para corresponder ao valor local em $TrafficManagerProfile.

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

### -TrafficManagerProfile
Especifica um objeto **TrafficManagerProfile** local.
Este cmdlet atualiza o Gerenciador de tráfego para corresponder a esse objeto local.

```yaml
Type: TrafficManagerProfile
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

### Microsoft. Azure. Commands. Network. TrafficManagerProfile
Esse cmdlet aceita um objeto **TrafficManagerProfile** .

## EXIBE

### Microsoft. Azure. Commands. Network. TrafficManagerProfile
Esse cmdlet retorna um objeto **TrafficManagerProfile** .

## INFORMA

## LINKS RELACIONADOS

[Add-AzureRmTrafficManagerEndpointConfig](./Add-AzureRmTrafficManagerEndpointConfig.md)

[Get-AzureRmTrafficManagerProfile](./Get-AzureRmTrafficManagerProfile.md)

[New-AzureRmTrafficManagerProfile](./New-AzureRmTrafficManagerProfile.md)

[Remove-AzureRmTrafficManagerEndpointConfig](./Remove-AzureRmTrafficManagerEndpointConfig.md)

[Remove-AzureRmTrafficManagerProfile](./Remove-AzureRmTrafficManagerProfile.md)


