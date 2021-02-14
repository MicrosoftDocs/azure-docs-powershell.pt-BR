---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/remove-azdatashare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShare.md
ms.openlocfilehash: 2679a3f63be3b7332020354e325e33573911334b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100110982"
---
# Remove-AzDataShare

## Sinopse
Remove um compartilhamento de dados.

## Sintaxe

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

## Descrição
O **cmdlet Remove-AzDataShare** remove um compartilhamento de dados.

## Exemplos

### Exemplo 1
```
PS C:\> Remove-AzDataShare -ResourceGroupName "ADS" -AccountName "WikiAds" -Name "AdsShare"
Are you sure you want to remove data share "AdsShare"? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

Esses comandos removem o compartilhamento de dados chamado AdsShare da conta wikiAds do compartilhamento de dados do azure. 

## Parâmetros

### -NomedaEm conta
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
Objeto de compartilhamento de dados do Azure' ''tipo yaml: Conjuntos de parâmetros PSDataShare: Aliases byObjectParameterSet: 

Obrigatório: Posição Verdadeira: Valor padrão nomeado: nenhuma entrada de pipeline aceita: Verdadeiro (ByValue) Aceitar caracteres curinga: False

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

### -Nome
Nome do compartilhamento de dados do Azure

Tipo yaml: Conjuntos de Parâmetros de Cadeia de Caracteres: Aliases byFieldsParameterSet: 

Obrigatório: Posição Verdadeira: Valor padrão nomeado: entrada de pipeline Nenhum aceitar: caracteres curinga False Accept: False

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
Objeto return (se especificado).

Tipo yaml: Conjuntos de Parâmetros SwitchParameter: (Todos) Aliases: 

Obrigatório: Posição falsa: valor padrão nomeado: nenhuma entrada de pipeline aceita: caracteres curinga False Accept: False

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

Tipo yaml: Conjuntos de Parâmetros de Cadeia de Caracteres: Aliases byFieldsParameterSet: 

Obrigatório: Posição Verdadeira: Valor padrão nomeado: entrada de pipeline Nenhum aceitar: caracteres curinga False Accept: False

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
A ID do recurso do compartilhamento de dados do Azure

tipo yaml: Conjuntos de Parâmetros de Cadeia de Caracteres: Aliases byResourceIdParameterSet: 

Obrigatório: Posição Verdadeira: Valor padrão nomeado: Nenhuma entrada de pipeline aceita: Verdadeiro (ByPropertyName) Aceitar caracteres curinga: False

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

### -Confirmar
Solicita confirmação antes de executar o cmdlet.

Tipo yaml: Conjuntos de Parâmetros SwitchParameter: (Todos) Aliases: cf

Obrigatório: Posição falsa: valor padrão nomeado: nenhuma entrada de pipeline aceita: caracteres curinga False Accept: False

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

tipo yaml: Conjuntos de Parâmetros SwitchParameter: (Todos) Aliases: wi

Obrigatório: Posição falsa: valor padrão nomeado: nenhuma entrada de pipeline aceita: caracteres curinga False Accept: False




tipo yaml: Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDconjuntos de parâmetros ataShare: Aliases byObjectParameterSet:

Obrigatório: Posição Verdadeira: Valor padrão nomeado: nenhuma entrada de pipeline aceita: Verdadeiro (ByValue) Aceitar caracteres curinga: False

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

### System.String

### Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare

## Saídas

### System.Boolean

## Notas

## LINKS RELACIONADOS
