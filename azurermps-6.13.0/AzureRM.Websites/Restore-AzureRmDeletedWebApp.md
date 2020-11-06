---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/restore-azurermdeletedwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Restore-AzureRmDeletedWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Restore-AzureRmDeletedWebApp.md
ms.openlocfilehash: caebbe3c9b84b469e5fc357686b256aca59c2b61
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430772"
---
# Restore-AzureRmDeletedWebApp

## Sinopse
Restaura um aplicativo Web excluído para um aplicativo Web novo ou existente.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

### FromDeletedResourceName
```
Restore-AzureRmDeletedWebApp [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-TargetResourceGroupName <String>] [-TargetName <String>] [-TargetSlot <String>]
 [-TargetAppServicePlanName <String>] [-RestoreContentOnly] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### FromDeletedApp
```
Restore-AzureRmDeletedWebApp [-TargetResourceGroupName <String>] [-TargetName <String>] [-TargetSlot <String>]
 [-TargetAppServicePlanName <String>] [-RestoreContentOnly] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-InputObject] <PSAzureDeletedWebApp> [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Restore-AzureRmDeletedWebApp** restaura um aplicativo Web excluído. O aplicativo Web especificado por TargetResourceGroupName, TargetName e TargetSlot será substituído pelo conteúdo e pelas configurações do aplicativo Web excluído. Se os parâmetros de destino não forem especificados, eles serão automaticamente preenchidos com o grupo de recursos, o nome e o slot do aplicativo Web excluído. Se o aplicativo Web de destino não existir, ele será automaticamente criado no plano do serviço de aplicativo especificado por TargetAppServicePlanName. O parâmetro de opção RestoreContentOnly pode ser usado para restaurar somente os arquivos do aplicativo excluído sem as configurações do aplicativo.

## EXEMPLOS

### Exemplo 1
```powershell
PS C:\> Restore-AzureRmDeletedWebApp -ResourceGroupName Default-Web-WestUS -Name ContosoApp -TargetAppServicePlanName ContosoPlan
```

Restaura um aplicativo excluído denominado ContosoApp pertencente ao grupo de recursos-Web-oeste-padrão. Um novo aplicativo com o mesmo nome e grupo de recursos será criado no plano do serviço de aplicativo chamado ContosoPlan, e os arquivos e as configurações do aplicativo excluídos serão restaurados.

### Exemplo 2
```powershell
PS C:\> Restore-AzureRmDeletedWebApp -ResourceGroupName Default-Web-WestUS -Name ContosoApp -Slot Staging -TargetResourceGroupName Default-Web-EastUS -TargetName ContosoRestore -RestoreContentOnly
```

Restaura o slot de preparo de um aplicativo excluído denominado ContosoApp pertencente ao grupo de recursos-Web-Westus padrão. O aplicativo Web denominado ContosoRestore pertencente ao grupo de recursos padrão-Web-Eastus será substituído. As configurações do aplicativo Web excluído não serão restauradas.

## OS

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

### -Force
Faça a restauração sem solicitar confirmação.

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

### -InputObject
O aplicativo Web Azure excluído.

```yaml
Type: PSAzureDeletedWebApp
Parameter Sets: FromDeletedApp
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Nome
O nome do aplicativo Web Azure excluído.

```yaml
Type: String
Parameter Sets: FromDeletedResourceName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
O grupo de recursos do aplicativo Web Azure excluído.

```yaml
Type: String
Parameter Sets: FromDeletedResourceName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RestoreContentOnly
Restaure os arquivos do aplicativo Web, mas não restaure as configurações.

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

### -Slot
O slot do Azure Web App excluído.

```yaml
Type: String
Parameter Sets: FromDeletedResourceName
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TargetAppServicePlanName
O plano de serviço de aplicativo para o novo Azure Web App.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TargetName
O nome do novo Azure Web App.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TargetResourceGroupName
O grupo de recursos que contém o novo Azure Web App.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TargetSlot
O nome do novo slot do Azure Web App.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.
Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

### Microsoft. Azure. Commands. webapps. cmdlets. webapps. PSAzureDeletedWebApp

## EXIBE

### Microsoft. Azure. Commands. webapps. Models. PSSite

## INFORMA

## LINKS RELACIONADOS

[Get-AzureRmDeletedWebApp](./Get-AzureRmDeletedWebApp.md)
