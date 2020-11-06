---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D344
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.trafficmanager/remove-azurermtrafficmanagerexpectedstatuscoderange
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Remove-AzureRmTrafficManagerExpectedStatusCodeRange.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Remove-AzureRmTrafficManagerExpectedStatusCodeRange.md
ms.openlocfilehash: 0971a4b8d485c1590794de6f1b6c2d4d9d21da4a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427102"
---
# Remove-AzureRmTrafficManagerExpectedStatusCodeRange

## Sinopse
Remove um intervalo de código de status esperado de um objeto de perfil do Gerenciador de tráfego local.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

```
Remove-AzureRmTrafficManagerExpectedStatusCodeRange -Min <Int32> -TrafficManagerProfile <TrafficManagerProfile>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Remove-AzureRmTrafficManagerExpectedStatusCodeRange** remove um intervalo de códigos de status esperados de um objeto de perfil do Azure Traffic Manager local.
Você pode obter um perfil usando os cmdlets New-AzureRmTrafficManagerProfile ou Get-AzureRmTrafficManagerProfile.

Este cmdlet opera no objeto de perfil local.
Confirme as alterações no perfil do Gerenciador de tráfego usando o cmdlet Set-AzureRmTrafficManagerProfile.

## EXEMPLOS

### Exemplo 1: remover um intervalo de código de status esperado de um perfil
```
PS C:\> $TrafficManagerProfile = Get-AzureRmTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> Remove-AzureRmTrafficManagerExpectedStatusCodeRange -TrafficManagerProfile $TrafficManagerProfile -Min 200
PS C:\> Set-AzureRmTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

O primeiro comando obtém um perfil do Gerenciador de tráfego do Azure usando o cmdlet **Get-AzureRmTrafficManagerProfile** .
O segundo comando Remove um intervalo de código de status esperado do perfil armazenado em $TrafficManagerProfile.
O comando final atualiza o perfil no Gerenciador de tráfego para corresponder ao valor local em $TrafficManagerProfile.

## OS

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

### -Min
Especifica o valor mais baixo no intervalo de código de status a ser removido.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TrafficManagerProfile
Especifica um objeto **TrafficManagerProfile** local.
Esse cmdlet modifica esse objeto local.
Para obter um objeto **TrafficManagerProfile** , use o cmdlet Get-AzureRmTrafficManagerProfile.

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
Mostra o que aconteceria se o cmdlet fosse executado. O cmdlet não é executado.

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
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

### Microsoft. Azure. Commands. Network. TrafficManagerProfile
Este cmdlet aceita um objeto **TrafficManagerProfile** para este cmdlet.

## EXIBE

### Microsoft. Azure. Commands. Network. TrafficManagerProfile
Esse cmdlet retorna um objeto **TrafficManagerProfile** modificado.

## INFORMA

## LINKS RELACIONADOS

[Add-AzureRmTrafficManagerExpectedStatusCodeRange](./Add-AzureRmTrafficManagerExpectedStatusCodeRange.md)

[Get-AzureRmTrafficManagerProfile](./Get-AzureRmTrafficManagerProfile.md)

[Set-AzureRmTrafficManagerProfile](./Set-AzureRmTrafficManagerProfile.md)
