---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: CC9D74BB-DFB2-41F3-B5CF-B265C549EC33
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/import-azurermautomationdscnodeconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Import-AzureRmAutomationDscNodeConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Import-AzureRmAutomationDscNodeConfiguration.md
ms.openlocfilehash: 49cd2fdb2d482621ea52f1df88c9bcd95521badd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432806"
---
# Import-AzureRmAutomationDscNodeConfiguration

## Sinopse
Importa um documento MOF como uma configuração de nó DSC na automação.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

```
Import-AzureRmAutomationDscNodeConfiguration -Path <String> -ConfigurationName <String> [-Force]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-IncrementNodeConfigurationBuild] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Import-AzureRmAutomationDscConfiguration** importa um documento de configuração do MOF (Managed Object Format) para a automação do Azure como uma configuração de nó de configuração de estado desejado (DSC).
Especifique o caminho de um arquivo. mof.

## EXEMPLOS

### Exemplo 1: importar uma configuração de nó DSC para automação
```
PS C:\>Import-AzureRmAutomationDscConfiguration -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01" -ConfigurationName "ContosoConfiguration" -Path "C:\DSC\webserver.mof" -Force
```

Esse comando importa uma configuração de nó DSC do arquivo chamado WebServer. MOF para a conta de automação chamada Contoso17, sob a configuração DSC ContosoConfiguration.
O comando especifica o parâmetro *Force* .
Se houver uma configuração de nó DSC chamada ContosoConfiguration. WebServer, esse comando a substituirá.

### Exemplo 2: importar uma configuração de nó DSC para automação e criar uma nova versão de compilação e não substituir NodeConfiguration existentes.
```
PS C:\>Import-AzureRmAutomationDscConfiguration -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01" -ConfigurationName "ContosoConfiguration" -Path "C:\DSC\webserver.mof" -IncrementNodeConfigurationBuild
```

Esse comando importa uma configuração de nó DSC do arquivo chamado WebServer. MOF para a conta de automação chamada Contoso17, sob a configuração DSC ContosoConfiguration.
O comando especifica o parâmetro *Force* .
Se houver uma configuração de nó DSC chamada ContosoConfiguration. WebServer, esse comando adicionará uma nova versão de compilação com o nome ContosoConfiguration [2]. WebServer.

## OS

### -AutomationAccountName
Especifica o nome da conta de automação na qual esse cmdlet importa uma configuração de nó DSC.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ConfigurationName
Especifica o nome de uma configuração DSC em automação para usar como o namespace e o contêiner para a configuração do nó a ser importada.

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

### -DefaultProfile
As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure

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

### -Force
Indica que esse cmdlet substitui uma configuração de nó DSC existente na automação.

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

### -IncrementNodeConfigurationBuild
Cria uma nova versão de compilação de configuração de nó.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -Caminho
Especifica o caminho do documento de configuração do MOF que este cmdlet importa.

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
Especifica o nome de um grupo de recursos para o qual esse cmdlet importa uma configuração de nó DSC.

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

### -Confirme
Solicita confirmação antes de executar o cmdlet.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
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
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

### System. String

## EXIBE

### Microsoft. Azure. Commands. Automation. Model. NodeConfiguration

## INFORMA

## LINKS RELACIONADOS

[Export-AzureRmAutomationDscConfiguration](./Export-AzureRmAutomationDscConfiguration.md)

[Get-AzureRmAutomationDscConfiguration](./Get-AzureRmAutomationDscConfiguration.md)


