---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/powershell/module/az.datashare/remove-azdatashare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShare.md
ms.openlocfilehash: 8a46ecacae8df648ab6400cad25c3ca24b3ee3a8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886977"
---
# Remove-AzDataShare

## SYNOPSIS
Remove um compartilhamento de dados.

## SINTAXE

### ByFieldsParameterSet (Padrão)
```
Remove-AzDataShare -ResourceGroupName <String> -AccountName <String> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByResourceIdParameterSet
```
Remove-AzDataShare -ResourceId <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByObjectParameterSet
```
Remove-AzDataShare -InputObject <PSDataShare> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
O cmdlet **Remove-AzDataShare** remove um compartilhamento de dados.

## EXEMPLOS

### Exemplo 1
```
PS C:\> Remove-AzDataShare -ResourceGroupName "ADS" -AccountName "WikiAds" -Name "AdsShare"
Are you sure you want to remove data share "AdsShare"? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

Esses comandos removem o compartilhamento de dados chamado AdsShare da conta de compartilhamento de dados do azure WikiAds. 

## PARÂMETROS

### -AccountName
Nome da conta de compartilhamento de dados do Azure

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AsJob
{{Fill AsJob Description}}

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
As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.

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
Objeto de compartilhamento de dados do Azure' ''yaml Tipo: PSDataShare Parameter Sets: ByObjectParameterSet Aliases: 

Obrigatório: True Position: Valor padrão nomeado: Entrada de pipeline Nenhum Aceitar: True (ByValue) Aceitar caracteres curinga: False

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
Nome do compartilhamento de dados do Azure

tipo yaml: Conjuntos de parâmetros de cadeia de caracteres: ByFieldsParameterSet Aliases: 

Obrigatório: True Position: Valor padrão nomeado: Entrada de pipeline Nenhum Aceitar: Caracteres curinga false accept: False

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PassThru
Objeto Return (se especificado).

tipo yaml: Conjuntos de parâmetros SwitchParameter: (Todos) Aliases: 

Obrigatório: False Position: Valor padrão nomeado: Nenhuma entrada de pipeline de aceitação: caracteres curinga false accept: False

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
O nome do grupo de recursos da conta de compartilhamento de dados do azure

tipo yaml: Conjuntos de parâmetros de cadeia de caracteres: ByFieldsParameterSet Aliases: 

Obrigatório: True Position: Valor padrão nomeado: Entrada de pipeline Nenhum Aceitar: Caracteres curinga false accept: False

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceId
A id de recurso do compartilhamento de dados do Azure

tipo yaml: Conjuntos de parâmetros de cadeia de caracteres: ByResourceIdParameterSet Aliases: 

Obrigatório: True Position: Nomeado Valor padrão: Entrada de pipeline Nenhum Aceitar: True (ByPropertyName) Aceitar caracteres curinga: False

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Confirm
Solicita a confirmação antes de executar o cmdlet.

tipo yaml: SwitchParameter Parameter Sets: (All) Aliases: cf

Obrigatório: False Position: Valor padrão nomeado: Nenhuma entrada de pipeline de aceitação: caracteres curinga false accept: False

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
Mostra o que aconteceria se o cmdlet fosse executado.
O cmdlet não é executado.

tipo yaml: SwitchParameter Parameter Sets: (All) Aliases: wi

Obrigatório: False Position: Valor padrão nomeado: Nenhuma entrada de pipeline de aceitação: caracteres curinga false accept: False




tipo yaml: Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDconjuntos de parâmetros ataShare: Aliases ByObjectParameterSet:

Obrigatório: True Position: Valor padrão nomeado: Entrada de pipeline Nenhum Aceitar: True (ByValue) Aceitar caracteres curinga: False

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
Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### System.String

### Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare

## SAÍDAS

### System.Boolean

## NOTES

## LINKS RELACIONADOS
