---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 18D5B95E-4CF1-4C79-AE8B-9F4DA49B46A9
online version: https://docs.microsoft.com/powershell/module/az.monitor/add-azlogprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Add-AzLogProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Add-AzLogProfile.md
ms.openlocfilehash: a5d60cbda668e963793dbb350950ea0e85812892
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888926"
---
# Add-AzLogProfile

## SYNOPSIS
Cria um novo perfil de log de atividades. Esse perfil é usado para arquivar o log de atividades em uma conta de armazenamento do Azure ou para transmitir para um hub de eventos do Azure na mesma assinatura. 

## SINTAXE

```
Add-AzLogProfile -Name <String> [-StorageAccountId <String>] [-ServiceBusRuleId <String>]
 [-RetentionInDays <Int32>] -Location <System.Collections.Generic.List`1[System.String]>
 [-Category <System.Collections.Generic.List`1[System.String]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
O cmdlet **Add-AzLogProfile** cria um perfil de log.
- **Conta de** Armazenamento - Somente conta de armazenamento padrão (conta de armazenamento premium não é suportada) é suportada. Pode ser do tipo ARM ou Clássico. Se ele estiver conectado a uma conta de armazenamento, o custo de armazenar o log de atividades será cobrado com taxas de armazenamento padrão normais. Pode haver apenas um perfil de log por assinatura, consequentemente, apenas uma conta de armazenamento por assinatura pode ser usada para exportar o log de atividades. 
- **Hub de Eventos** - Pode haver apenas um perfil de log por assinatura, consequentemente, apenas um hub de eventos por assinatura pode ser usado para exportar o log de atividades. Se o log de atividades for transmitido para um hub de eventos, o preço padrão do hub de eventos será aplicado. No log de atividades, os eventos podem pertencer a uma região ou podem ser "Globais". Global essencialmente significa que esses eventos são agnósticos de região e são independentes da região, na verdade, a maioria dos eventos se enquadra nessa categoria. Se o perfil do log de atividades for definido a partir do portal, ele adiciona implicitamente "Global" juntamente com qualquer outra região selecionada na interface do usuário. Ao usar o cmdlet, o local como "Global" deve ser explicitamente mencionado além de qualquer outra região. 
**Observação** :- **Falha ao definir "Global"** nos locais resultará em uma maioria do log de atividades não sendo exportado. Este cmdlet implementa o padrão ShouldProcess, ou seja, ele pode solicitar confirmação do usuário antes de realmente criar, modificar ou remover o recurso.

## EXEMPLOS

### Exemplo 1: Adicionar um novo perfil de log para exportar o log de atividades que corresponde à condição de local para uma conta de armazenamento
```powershell
Add-AzLogProfile -Location "Global","West US" -Name ExportLogProfile -StorageAccountId /subscriptions/40gpe80s-9sb7-4f07-9042-b1b6a92ja9fk/resourceGroups/activitylogRG/providers/Microsoft.Storage/storageAccounts/activitylogstorageaccount
```

### Exemplo 2

Cria um novo perfil de log de atividades. (gerado automaticamente)

```powershell <!-- Aladdin Generated Example --> 
Add-AzLogProfile -Location 'Global' -Name ExportLogProfile -RetentionInDays <Int32> -ServiceBusRuleId <String> -StorageAccountId /subscriptions/40gpe80s-9sb7-4f07-9042-b1b6a92ja9fk/resourceGroups/activitylogRG/providers/Microsoft.Storage/storageAccounts/activitylogstorageaccount
```

## PARÂMETROS

### -Category
Especifica a lista de categorias.

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
As credenciais, conta, locatário e assinatura usadas para comunicação com o azure

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

### -Location
Especifica o local do perfil de log.
Valores válidos: Execute abaixo do cmdlet para obter a lista mais recente de locais. Get-AzLocation | Selecionar DisplayName

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name
Especifica o nome do perfil.

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

### -RetentionInDays
Especifica a política de retenção, em dias. Esse é o número de dias em que os logs são preservados na conta de armazenamento especificada. Para manter os dados definidos para sempre como **0**. Se não for especificado, o padrão é **0**. As taxas de cobrança padrão de armazenamento ou hub de eventos serão aplicadas para retenção de dados.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ServiceBusRuleId
Especifica a ID da regra de Barramento de Serviço.

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

### -StorageAccountId
Especifica a ID da conta de armazenamento. ID é a ID de Recurso totalmente qualificada da conta de armazenamento, por exemplo  
/subscriptions/40gpe80s-9sb7-4f07-9042-b1b6a92ja9fk/resourceGroups/activitylogRG/providers/Microsoft.Storage/storageAccounts/activitylogstorageaccount

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

### -Confirm
Solicita a confirmação antes de executar o cmdlet.

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
Mostra o que aconteceria se o cmdlet fosse executado. O cmdlet não é executado.

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

### System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]

### System.Collections.Generic.List'1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]

## SAÍDAS

### Microsoft.Azure.Commands.Insights.OutputClasses.PSLogProfile

## NOTES

## LINKS RELACIONADOS

[Get-AzLogProfile](./Get-AzLogProfile.md)

[Remove-AzLogProfile](./Remove-AzLogProfile.md)


