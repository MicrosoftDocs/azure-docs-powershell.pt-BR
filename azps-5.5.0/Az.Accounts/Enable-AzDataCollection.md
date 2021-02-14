---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/enable-azdatacollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Enable-AzDataCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Enable-AzDataCollection.md
ms.openlocfilehash: a8087f41c33dc3bb066609393a87986d5016d1ae
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115576"
---
# Enable-AzDataCollection

## Sinopse
Permite que o Azure PowerShell colete dados para melhorar a experiência do usuário com os cmdlets do Azure PowerShell. Executar este cmdlet opta pela coleta de dados do usuário atual no computador atual. Os dados são coletados por padrão, a menos que você a opte explicitamente.

## Sintaxe

```
Enable-AzDataCollection [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Descrição

O `Enable-AzDataCollection` cmdlet é usado para optar pela coleta de dados. O Azure PowerShell coleta automaticamente dados de telemetria por padrão. A Microsoft agrega dados coletados para identificar padrões de uso, identificar problemas comuns e melhorar a experiência do PowerShell do Azure.
O Microsoft Azure PowerShell não coleta dados pessoais ou particulares. Para desabilitar a coleta de dados, você deve optar explicitamente por `Disable-AzDataCollection` executar.

## Exemplos

### Exemplo 1: Habilitando a coleta de dados para o usuário atual

O exemplo a seguir mostra como habilitar a coleta de dados para o usuário atual.

```powershell
Enable-AzDataCollection
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

[Disable-AzDataCollection](./Disable-AzDataCollection.md)
