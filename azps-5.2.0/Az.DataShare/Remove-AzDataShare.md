---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/remove-azdatashare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Remove-AzDataShare.md
ms.openlocfilehash: 2679a3f63be3b7332020354e325e33573911334b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98256892"
---
# Remove-AzDataShare

## Sinopse
Remove um compartilhamento de dados.

## SYNTAX

### ByFieldsParameterSet (padrão)
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

## DESCRITIVO
O cmdlet **Remove-AzDataShare** remove um compartilhamento de dados.

## EXEMPLOS

### Exemplo 1
```
PS C:\> Remove-AzDataShare -ResourceGroupName "ADS" -AccountName "WikiAds" -Name "AdsShare"
Are you sure you want to remove data share "AdsShare"? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

Esses comandos removem o compartilhamento de dados chamado AdsShare da conta do Azure data share WikiAds. 

## OS

### -AccountName
Nome da conta do compartilhamento de dados do Azure

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
{{Preencher Descrição AsJob}}

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

### -InputObject
O objeto de compartilhamento de dados do Azure ' ' ' YAML o tipo de parâmetro PSDataShare: ByObjectParameterSet aliases: 

Obrigatório: posição verdadeira: valor nomeado padrão: nenhum aceitar entrada de pipeline: true (ByValue) aceitar caracteres curinga: false

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

YAML tipo: conjuntos de parâmetros de cadeias de caracteres: ByFieldsParameterSet aliases: 

Obrigatório: posição verdadeira: valor nomeado padrão: nenhum aceitar entrada de pipeline: falso aceitar caracteres curinga: falso

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
Objeto de retorno (se especificado).

YAML tipo: SwitchParameter parâmetro define: (All) aliases: 

Obrigatório: posição falso: nome padrão nomeado: nenhum aceitar entrada de pipeline: falso aceitar caracteres curinga: falso

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
O nome do grupo de recursos da conta do Azure data share

YAML tipo: conjuntos de parâmetros de cadeias de caracteres: ByFieldsParameterSet aliases: 

Obrigatório: posição verdadeira: valor nomeado padrão: nenhum aceitar entrada de pipeline: falso aceitar caracteres curinga: falso

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

YAML tipo: conjuntos de parâmetros de cadeias de caracteres: ByResourceIdParameterSet aliases: 

Obrigatório: posição verdadeira: valor nomeado padrão: nenhum aceitar entrada de pipeline: true (ByPropertyName) aceitar caracteres curinga: false

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

### -Confirme
Solicita confirmação antes de executar o cmdlet.

YAML tipo: SwitchParameter parâmetro define: (All) aliases: FC

Obrigatório: posição falso: nome padrão nomeado: nenhum aceitar entrada de pipeline: falso aceitar caracteres curinga: falso

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

YAML tipo: SwitchParameter parâmetro define: (All) aliases: Wi

Obrigatório: posição falso: nome padrão nomeado: nenhum aceitar entrada de pipeline: falso aceitar caracteres curinga: falso




Tipo de YAML: Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDconjuntos de parâmetro ataShare: alias ByObjectParameterSet:

Obrigatório: posição verdadeira: valor nomeado padrão: nenhum aceitar entrada de pipeline: true (ByValue) aceitar caracteres curinga: false

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
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## SENSORES

### System. String

### Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare

## EXIBE

### System. Boolean

## INFORMA

## LINKS RELACIONADOS
