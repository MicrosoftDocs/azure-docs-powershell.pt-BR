---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/powershell/module/az.accounts/enable-azdatacollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Enable-AzDataCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Enable-AzDataCollection.md
ms.openlocfilehash: ce2c4060d6471cc65c6b343e86c1e15b74ca5414
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891528"
---
# Enable-AzDataCollection

## SYNOPSIS
Permite que o Azure PowerShell colete dados para melhorar a experiência do usuário com os cmdlets do Azure PowerShell. A execução desse cmdlet opta pela coleta de dados para o usuário atual no computador atual. Os dados são coletados por padrão, a menos que você opte explicitamente.

## SINTAXE

```
Enable-AzDataCollection [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

O `Enable-AzDataCollection` cmdlet é usado para optar pela coleta de dados. O Azure PowerShell coleta automaticamente dados de telemetria por padrão. A Microsoft agrega dados coletados para identificar padrões de uso, identificar problemas comuns e melhorar a experiência do Azure PowerShell.
O Microsoft Azure PowerShell não coleta dados pessoais ou particulares. Para desabilitar a coleta de dados, você deve optar explicitamente pela execução `Disable-AzDataCollection` de .

## EXEMPLOS

### Exemplo 1: Habilitando a coleta de dados para o usuário atual

O exemplo a seguir mostra como habilitar a coleta de dados para o usuário atual.

```powershell
Enable-AzDataCollection
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

[Disable-AzDataCollection](./Disable-AzDataCollection.md)
