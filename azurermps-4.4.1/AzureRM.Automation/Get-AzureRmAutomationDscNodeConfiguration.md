---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 89C931AE-DA81-47A7-80E4-159C36497DA0
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationDscNodeConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationDscNodeConfiguration.md
ms.openlocfilehash: f5de98b4f64b4f9adb03493638cdf4e1e613e10f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431203"
---
# Get-AzureRmAutomationDscNodeConfiguration

## Sinopse
Obtém metadados para configurações de nó DSC na automação.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

### ByAll (padrão)
```
Get-AzureRmAutomationDscNodeConfiguration [-RollupStatus <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByNodeConfigurationName
```
Get-AzureRmAutomationDscNodeConfiguration -Name <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByConfigurationName
```
Get-AzureRmAutomationDscNodeConfiguration -ConfigurationName <String> [-RollupStatus <String>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Get-AzureRmAutomationDscNodeConfiguration** obtém metadados das configurações do nó DSC (configuração de estado desejado) do APS na automação do Azure.
A automação armazena a configuração do nó DSC como um documento de configuração do MOF (formato de objeto gerenciado).

## EXEMPLOS

### Exemplo 1: obter todas as configurações do nó DSC
```
PS C:\>Get-AzureRmAutomationDscNodeConfiguration -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17"
```

Esse comando obtém metadados para todas as configurações de nó DSC na conta de automação chamada Contoso17.

### Exemplo 2: obter todas as configurações do nó DSC para uma configuração DSC
```
PS C:\>Get-AzureRmAutomationDscNodeConfiguration -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -ConfigurationName "ContosoConfiguration"
```

Esse comando obtém metadados para todas as configurações de nó DSC na conta de automação chamada Contoso17 que a configuração DSC nomeada ContosoConfiguration gerou.

### Exemplo 3: obter uma configuração de nó DSC por nome
```
PS C:\>Get-AzureRmAutomationDscNodeConfiguration -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Name "ContosoConfiguration.webserver"
```

Esse comando obtém metadados para uma configuração de nó DSC com o nome ContosoConfiguration. WebServer na conta de automação chamada Contoso17.

## OS

### -AutomationAccountName
Especifica o nome de uma conta de automação que contém as configurações de nó DSC para as quais esse cmdlet obtém metadados.

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
Especifica o nome da configuração DSC para a qual esse cmdlet obtém metadados de configuração de nó.

```yaml
Type: System.String
Parameter Sets: ByConfigurationName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Nome
Especifica o nome da configuração do nó DSC para a qual esse cmdlet obtém metadados.

```yaml
Type: System.String
Parameter Sets: ByNodeConfigurationName
Aliases: NodeConfigurationName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Especifica o nome de um grupo de recursos.
Esse cmdlet obtém metadados para configurações de nó DSC no grupo de recursos que esse parâmetro especifica.

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

### -RollupStatus
Especifica o status de acúmulo das configurações de nó DSC que esse cmdlet obtém.
Os valores válidos são: 

- Mal 
- Corretamente

```yaml
Type: System.String
Parameter Sets: ByAll, ByConfigurationName
Aliases: 
Accepted values: Good, Bad

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

### Microsoft. Azure. Commands. Automation. Model. CompilationJob

## INFORMA

## LINKS RELACIONADOS

[Import-AzureRmAutomationDscNodeConfiguration](./Import-AzureRmAutomationDscNodeConfiguration.md)


