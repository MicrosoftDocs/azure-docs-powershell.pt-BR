---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/powershell/module/az.accounts/enable-azcontextautosave
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Enable-AzContextAutosave.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Enable-AzContextAutosave.md
ms.openlocfilehash: 8bca1314433f8fcbcc0c9f395783bbb3d9835ffb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891530"
---
# Enable-AzContextAutosave

## SYNOPSIS
Os contextos do Azure são objetos do PowerShell que representam sua assinatura ativa para executar comandos e as informações de autenticação necessárias para se conectar a uma nuvem do Azure. Com os contextos do Azure, o Azure PowerShell não precisa reauthenticar sua conta sempre que você trocar de assinatura. Para obter mais informações, consulte [objetos de contexto do Azure PowerShell](https://docs.microsoft.com/powershell/azure/context-persistence).

Esse cmdlet permite que as informações de contexto do Azure sejam salvas e carregadas automaticamente ao iniciar um processo do PowerShell. Por exemplo, ao abrir uma nova janela.

## SINTAXE

```
Enable-AzContextAutosave [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

Permite que as informações de contexto do Azure sejam salvas e carregadas automaticamente quando um processo do PowerShell é iniciado. O contexto é salvo no final da execução de qualquer cmdlet que afete o contexto. Por exemplo, qualquer cmdlet de perfil. Se você estiver usando a autenticação do usuário, os tokens poderão ser atualizados durante a execução de qualquer cmdlet.

## EXEMPLOS

### Exemplo 1: Habilitar credenciais de autosaving para o usuário atual

Ativar o autosave de credenciais para o usuário atual. Sempre que uma janela do PowerShell é aberta, seu contexto atual é lembrado sem entrar.

```powershell
Enable-AzContextAutosave
```

### Exemplo 2

Permitir que as informações de credencial, conta e assinatura do Azure sejam salvas e carregadas automaticamente quando você abrir uma janela do PowerShell nesta sessão do PowerShell. (gerado automaticamente)

```powershell <!-- Aladdin Generated Example -->
Enable-AzContextAutosave -Scope Process
```

## PARÂMETROS

### -DefaultProfile

As credenciais, locatários e assinaturas usadas para comunicação com o Azure

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

### -Scope

Determina o escopo das alterações de contexto. Por exemplo, se as alterações se aplicam apenas ao processo atual ou a todas as sessões iniciadas por esse usuário. As alterações feitas com o escopo `CurrentUser` afetarão todas as sessões do PowerShell iniciadas pelo usuário. Se uma sessão específica precisar ter configurações diferentes, use o escopo `Process` .

```yaml
Type: Microsoft.Azure.Commands.Profile.Common.ContextModificationScope
Parameter Sets: (All)
Aliases:
Accepted values: Process, CurrentUser

Required: False
Position: Named
Default value: CurrentUser
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
Default value: None
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
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### Nenhum

## SAÍDAS

### Microsoft.Azure.Commands.Common.Authentication.ContextAutosaveSettings

## NOTES

## LINKS RELACIONADOS
