---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/enable-azcontextautosave
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Enable-AzContextAutosave.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Enable-AzContextAutosave.md
ms.openlocfilehash: 6d80ee2ee2072bd31e96f4daa5706cba5f1c8dab
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115578"
---
# Enable-AzContextAutosave

## Sinopse
Os contextos do Azure são objetos do PowerShell que representam sua assinatura ativa para executar comandos e as informações de autenticação necessárias para se conectar a uma nuvem do Azure. Com contextos do Azure, o Azure PowerShell não precisa re autenticar sua conta sempre que você mudar de assinatura. Para obter mais informações, consulte objetos [de contexto do PowerShell do Azure.](https://docs.microsoft.com/powershell/azure/context-persistence)

Esse cmdlet permite que as informações de contexto do Azure sejam salvas e carregadas automaticamente quando você inicia um processo do PowerShell. Por exemplo, ao abrir uma nova janela.

## Sintaxe

```
Enable-AzContextAutosave [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Descrição

Permite que as informações de contexto do Azure sejam salvas e carregadas automaticamente quando um processo do PowerShell é iniciado. O contexto é salvo no final da execução de qualquer cmdlet que afete o contexto. Por exemplo, qualquer cmdlet de perfil. Se você estiver usando a autenticação do usuário, os tokens poderão ser atualizados durante a execução de qualquer cmdlet.

## Exemplos

### Exemplo 1: Habilitar as credenciais de autoslagem para o usuário atual

Ativar o autosave de credenciais para o usuário atual. Sempre que uma janela do PowerShell é aberta, seu contexto atual é lembrado sem fazer logo login.

```powershell
Enable-AzContextAutosave
```

### Exemplo 2

Permita que as informações da credencial, da conta e da assinatura do Azure sejam salvas e carregadas automaticamente quando você abrir uma janela do PowerShell nesta sessão do PowerShell. (gerado automaticamente)

```powershell <!-- Aladdin Generated Example -->
Enable-AzContextAutosave -Scope Process
```

## Parâmetros

### -DefaultProfile

As credenciais, o locatário e a assinatura usadas para comunicação com o Azure

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

### -Escopo

Determina o escopo das alterações de contexto. Por exemplo, se as alterações se aplicam apenas ao processo atual ou a todas as sessões iniciadas por esse usuário. As alterações feitas com o escopo `CurrentUser` afetarão todas as sessões do PowerShell iniciadas pelo usuário. Se uma sessão específica precisar ter configurações diferentes, use o `Process` escopo.

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

### Parâmetros Comuns

Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## Entradas

### Nenhum

## Saídas

### Microsoft.Azure.Commands.Common.Authentication.ContextAutosaveSettings

## Notas

## LINKS RELACIONADOS
