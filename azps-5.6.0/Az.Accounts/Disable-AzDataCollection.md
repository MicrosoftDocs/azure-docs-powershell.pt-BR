---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/powershell/module/az.accounts/disable-azdatacollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Disable-AzDataCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Disable-AzDataCollection.md
ms.openlocfilehash: 54af80b230c3cb031e8927a82ec3536cc1a81ec0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891534"
---
# Disable-AzDataCollection

## SYNOPSIS
Opta por não coletar dados para melhorar os cmdlets do Azure PowerShell. Os dados são coletados por padrão, a menos que você opte explicitamente.

## SINTAXE

```
Disable-AzDataCollection [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

O `Disable-AzDataCollection` cmdlet é usado para excluir a coleta de dados. O Azure PowerShell coleta automaticamente dados de telemetria por padrão. Para desabilitar a coleta de dados, você deve desativar explicitamente. A Microsoft agrega dados coletados para identificar padrões de uso, identificar problemas comuns e melhorar a experiência do Azure PowerShell. O Microsoft Azure PowerShell não coleta dados pessoais ou particulares. Se você tiver optado anteriormente, execute o cmdlet para habilitar a coleta de dados para o usuário `Enable-AzDataCollection` atual no computador atual.

## EXEMPLOS

### Exemplo 1: Desabilitando a coleta de dados para o usuário atual

O exemplo a seguir mostra como desabilitar a coleta de dados para o usuário atual.

```powershell
Disable-AzDataCollection
```

## PARÂMETROS

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

### -Confirm

Solicita a confirmação antes de executar o cmdlet.

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

Mostra o que aconteceria se o cmdlet fosse executado. O cmdlet não é executado.

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
Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### Nenhum

## SAÍDAS

### System.Void

## NOTES

## LINKS RELACIONADOS

[Enable-AzDataCollection](./Enable-AzDataCollection.md)
