---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/disable-azdatacollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Disable-AzDataCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Disable-AzDataCollection.md
ms.openlocfilehash: 27b3565191d7de110a5ba3a1e37d204fe3301cbf
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115581"
---
# Disable-AzDataCollection

## Sinopse
Opta por não coletar dados para melhorar os cmdlets do Azure PowerShell. Os dados são coletados por padrão, a menos que você a opte explicitamente.

## Sintaxe

```
Disable-AzDataCollection [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Descrição

O `Disable-AzDataCollection` cmdlet é usado para não usar a coleta de dados. O Azure PowerShell coleta automaticamente dados de telemetria por padrão. Para desabilitar a coleta de dados, você deve sair explicitamente. A Microsoft agrega dados coletados para identificar padrões de uso, identificar problemas comuns e melhorar a experiência do PowerShell do Azure. O Microsoft Azure PowerShell não coleta dados pessoais ou particulares. Se você tiver optado anteriormente, execute o cmdlet para habilitar a coleta de dados para o usuário `Enable-AzDataCollection` atual no computador atual.

## Exemplos

### Exemplo 1: desabilitando a coleta de dados para o usuário atual

O exemplo a seguir mostra como desabilitar a coleta de dados para o usuário atual.

```powershell
Disable-AzDataCollection
```

## Parâmetros

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

### -Confirmar

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

Mostra o que acontece se o cmdlet for executado. O cmdlet não é executado.

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

Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Para obter mais informações, [consulte about_CommonParameters.](/powershell/module/microsoft.powershell.core/about/about_commonparameters)

## Entradas

### Nenhum

## Saídas

### System.Void

## Notas

## LINKS RELACIONADOS

[Enable-AzDataCollection](./Enable-AzDataCollection.md)
