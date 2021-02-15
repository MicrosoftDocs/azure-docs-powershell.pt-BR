---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/reset-azsynapsesqladvancedthreatprotectionsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Reset-AzSynapseSqlAdvancedThreatProtectionSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Reset-AzSynapseSqlAdvancedThreatProtectionSetting.md
ms.openlocfilehash: 420b95d8d20d21758e4f42db6c31e2d1ead557ac
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118885"
---
# Reset-AzSynapseSqlAdvancedThreatProtectionSetting

## Sinopse
Remove as configurações avançadas de proteção contra ameaças de um espaço de trabalho.

## Sintaxe

### ClearByNameParameterSet (Padrão)
```
Reset-AzSynapseSqlAdvancedThreatProtectionSetting [-ResourceGroupName <String>] -WorkspaceName <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ClearByInputObjectParameterSet
```
Reset-AzSynapseSqlAdvancedThreatProtectionSetting -InputObject <PSSynapseWorkspace> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ClearByResourceIdParameterSet
```
Reset-AzSynapseSqlAdvancedThreatProtectionSetting -ResourceId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Descrição
O cmdlet **Reset-AzSynapseSqlAdvancedThreatProtectionSetting** remove as configurações avançadas de proteção contra ameaças de um Espaço de Trabalho de Análise do Azure Synapse.

## Exemplos

### Exemplo 1
```powershell
PS C:\> Reset-AzSynapseSqlAdvancedThreatProtectionSetting -WorkspaceName ContosoWorkspace
```

Esse comando remove as configurações avançadas de proteção contra ameaças de um espaço de trabalho chamado ContosoWorkspace.

## Parâmetros

### -AsJob
Executar cmdlet em segundo plano

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

### -DefaultProfile
As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.

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

### -InputObject
objeto de entrada de espaço de trabalho, geralmente passado pelo pipeline.

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: ClearByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -PassThru
Este Cmdlet não retorna um objeto por padrão.
Se essa opção for especificada, ela retornará verdadeira se for bem-sucedida.

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
Nome do grupo de recursos.

```yaml
Type: System.String
Parameter Sets: ClearByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceId
Identificador de recurso do espaço de trabalho Synapse.

```yaml
Type: System.String
Parameter Sets: ClearByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NomedoEspacial de Trabalho
Nome do espaço de trabalho Synapse.

```yaml
Type: System.String
Parameter Sets: ClearByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Confirmar
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
Mostra o que acontece se o cmdlet for executado.
O cmdlet não é executado.

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
Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## Entradas

### Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace

## Saídas

### System.Boolean

## Notas

## LINKS RELACIONADOS
