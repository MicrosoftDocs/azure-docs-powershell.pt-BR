---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.WebSites
ms.assetid: D23BBF34-80C0-48B1-8E1C-6F345DEC61AD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/new-azurermwebappslot
schema: 2.0.0
ms.openlocfilehash: f41149c6abb946340acc06b847c72dcabcee18fe
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93785588"
---
# New-AzureRmWebAppSlot

## Sinopse
Cria um slot do Azure Web App.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

```
New-AzureRmWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [[-AppServicePlan] <String>] [[-SourceWebApp] <Site>] [-IgnoreSourceControl] [-IgnoreCustomHostNames]
 [[-AppSettingsOverrides] <Hashtable>] [[-AseName] <String>] [[-AseResourceGroupName] <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **New-AzureRmWebAppSlot** cria um slot do aplicativo Web do Azure em um determinado grupo de recursos que usa o plano do serviço de aplicativo especificado e o Data Center.

## EXEMPLOS

### Exemplo 1
```
PS C:\> New-AzureRmWebAppSlot -ResourceGroupName Default-Web-WestUS -Name "ContosoSite" -AppServicePlan "ContosoServicePlan" -Slot "Slot001"
```

Esse comando cria um slot chamado Slot001 em um aplicativo Web existente nomes ContosoSite no grupo de recursos existente chamado padrão-Web-Oesteus no centro de dados oeste dos EUA.
O comando usa um plano do serviço de aplicativo existente chamado ContosoServicePlan.

## OS

### -AppServicePlan
Nome do plano do serviço de aplicativo

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AppSettingsOverrides
Configurações do aplicativo substitui Hashtable

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AseName
Nome do ambiente do serviço de aplicativo

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AseResourceGroupName
Nome do grupo de recursos do ambiente do serviço de aplicativo

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 9
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

### -IgnoreCustomHostNames
Opção ignorar nomes de host personalizados

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IgnoreSourceControl
Opção ignorar controle de origem

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Nome
Nome do webapp

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Nome do grupo de recursos

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Slot
Nome do slot do webapp

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SourceWebApp
Objeto WebApp de origem

```yaml
Type: Site
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -AsJob
Executar o cmdlet em segundo plano

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

### Instalação
O parâmetro ' SourceWebApp ' aceita o valor do tipo ' site ' da pipeline

## EXIBE

## INFORMA

## LINKS RELACIONADOS

[Get-AzureRMWebAppSlot](./Get-AzureRMWebAppSlot.md)

[Remove-AzureRMWebAppSlot](./Remove-AzureRMWebAppSlot.md)

[Restart-AzureRMWebAppSlot](./Restart-AzureRMWebAppSlot.md)

[Set-AzureRMWebAppSlot](./Set-AzureRMWebAppSlot.md)

[Start-AzureRMWebAppSlot](./Start-AzureRMWebAppSlot.md)

[Parar-AzureRMWebAppSlot](./Stop-AzureRMWebAppSlot.md)

[Get-AzureRmAppServicePlan](./Get-AzureRmAppServicePlan.md)

[Get-AzureRmWebApp](./Get-AzureRmWebApp.md)
