---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: B6487D26-2B6A-4938-B1CD-48EADD8D0C3C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Import-AzureRMAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Import-AzureRMAutomationRunbook.md
ms.openlocfilehash: d28166ec0a9a339017aa11bc30c0c5f0394afe94
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431187"
---
# Import-AzureRmAutomationRunbook

## Sinopse
Importa um runbook de automação.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

```
Import-AzureRmAutomationRunbook [-Path] <String> [-Description <String>] [-Name <String>] [-Tags <IDictionary>]
 -Type <String> [-LogProgress <Boolean>] [-LogVerbose <Boolean>] [-Published] [-Force]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Import-AzureRmAutomationRunbook** importa um runbook de automação do Azure. Especifique o caminho para um arquivo de script wps_2 (. ps1) a ser importado para wps_2 e wps_2 runbooks de fluxo de trabalho ou para um arquivo de runbook gráfico (. graphrunbook) para runbooks gráficos. O nome do arquivo se torna o nome do runbook. Para wps_2 runbooks de fluxo de trabalho, o script deve conter uma única definição de fluxo de trabalho wps_2 que corresponda ao nome do arquivo.

## EXEMPLOS

### Exemplo 1: importar um runbook de um arquivo
```
PS C:\> $Tags = @{"tag01"="value01"; "tag02"="value02"}
PS C:\> Import-AzureRmAutomationRunbook -Path .\GraphicalRunbook06.graphrunbook -Tags $Tags -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -Type GraphicalPowershell
```

O primeiro comando atribui dois pares de chave/valor à variável $Tags.

O segundo comando importa um runbook gráfico chamado GraphicalRunbook06 para a conta de automação chamada AutomationAccount01.
O comando também atribui as marcas armazenadas em $Tags.

## OS

### -AutomationAccountName
Especifica o nome da conta de automação na qual esse cmdlet importa um runbook.

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

### -Descrição
Especifica uma descrição do runbook importado.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Force
ps_force

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

### -LogProgress
Especifica se o runbook registra informações de progresso.

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -LogVerbose
Especifica se o runbook registra informações detalhadas.

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Nome
Especifica o nome do runbook importado por esse cmdlet.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: RunbookName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Caminho
Especifica o caminho de um arquivo. ps1 ou. graphrunbook que este cmdlet importa.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SourcePath

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Publicado
Indica que esse cmdlet publica o runbook que ele importa.

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

### -ResourceGroupName
Especifica o nome do grupo de recursos para o qual esse cmdlet importa um runbook.

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

### -Marcas
Pares de valores chave na forma de uma tabela de hash. Por exemplo:

@ {Key0 = "value0"; key1 = $null; Key2 = "value2"}

```yaml
Type: System.Collections.IDictionary
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Digite
Especifica o tipo de runbook que este cmdlet cria.
Os valores válidos são:

- ™
- GraphicalPowerShell
- PowerShellWorkflow
- GraphicalPowerShellWorkflow
- Representar

O gráfico de valor é obsoleto.
É equivalente a GraphicalPowerShellWorkflow.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: PowerShell, GraphicalPowerShell, PowerShellWorkflow, GraphicalPowerShellWorkflow, Graph

Required: True
Position: Named
Default value: None
Accept pipeline input: False
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

### Microsoft. Azure. Commands. Automation. Model. runbook

## INFORMA

## LINKS RELACIONADOS

[Export-AzureRmAutomationRunbook](./Export-AzureRMAutomationRunbook.md)

[Get-AzureRmAutomationRunbook](./Get-AzureRMAutomationRunbook.md)

[New-AzureRmAutomationRunbook](./New-AzureRMAutomationRunbook.md)

[New-AzureRmAutomationRunbook](./New-AzureRMAutomationRunbook.md)

[Publicar-AzureRmAutomationRunbook](./Publish-AzureRMAutomationRunbook.md)

[Remove-AzureRmAutomationRunbook](./Remove-AzureRMAutomationRunbook.md)

[Set-AzureRmAutomationRunbook](./Set-AzureRMAutomationRunbook.md)

[Start-AzureRmAutomationRunbook](./Start-AzureRMAutomationRunbook.md)
