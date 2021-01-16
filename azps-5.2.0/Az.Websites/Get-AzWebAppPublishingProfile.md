---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 38433470-CAFD-4B8F-980C-63D4B264B39F
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azwebapppublishingprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppPublishingProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppPublishingProfile.md
ms.openlocfilehash: 4e4e8e1575070f04a02496014ab93276a2dc9328
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98256717"
---
# Get-AzWebAppPublishingProfile

## Sinopse
Obtém um perfil de publicação do Azure Web App.

## SYNTAX

### Eles
```
Get-AzWebAppPublishingProfile [[-OutputFile] <String>] [[-Format] <String>] [-IncludeDisasterRecoveryEndpoints]
 [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### S2
```
Get-AzWebAppPublishingProfile [[-OutputFile] <String>] [[-Format] <String>] [-IncludeDisasterRecoveryEndpoints]
 [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Get-AzWebAppPublishingProfile** Obtém um perfil de publicação do Azure Web App.

## EXEMPLOS

### Exemplo 1
```powershell
PS C:\> Get-AzWebAppPublishingProfile -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Format "Ftp" -OutputFile "C:\Users\contoso\outputfile.publishsettings"
```

Este comando obtém o perfil de publicação no formato FTP para o aplicativo Web ContosoWebApp associado ao grupo de recursos Default-Web-Oesteus e o armazena no arquivo de saída especificado.

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

### -Format
Format

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: WebDeploy, FileZilla3, Ftp

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IncludeDisasterRecoveryEndpoints
Inclua os pontos de extremidade de recuperação de desastre se verdadeiro

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Nome
Nome do WebApp

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -OutputFile
Arquivo de saída

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Nome do grupo de recursos

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WebApp
Objeto WebApp

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: S2
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

### System. String

### Microsoft. Azure. Commands. webapps. Models. PSSite

## EXIBE

### System. String

## INFORMA

## LINKS RELACIONADOS

[Get-AzAppServicePlan](./Get-AzAppServicePlan.md)

[Get-AzWebApp](./Get-AzWebApp.md)


