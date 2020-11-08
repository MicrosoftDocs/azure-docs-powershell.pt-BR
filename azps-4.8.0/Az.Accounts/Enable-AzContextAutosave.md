---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/enable-azcontextautosave
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Enable-AzContextAutosave.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Enable-AzContextAutosave.md
ms.openlocfilehash: 6d80ee2ee2072bd31e96f4daa5706cba5f1c8dab
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94111926"
---
# Enable-AzContextAutosave

## Sinopse
Os contextos do Azure são objetos do PowerShell que representam a sua assinatura ativa para executar comandos e as informações de autenticação necessárias para se conectar a uma nuvem do Azure. Com os contextos do Azure, o PowerShell do Azure não precisa autenticar sua conta sempre que você alternar entre assinaturas. Para obter mais informações, consulte [objetos de contexto do PowerShell do PowerShell](https://docs.microsoft.com/powershell/azure/context-persistence).

Esse cmdlet permite que as informações de contexto do Azure sejam salvas e carregadas automaticamente quando você inicia um processo do PowerShell. Por exemplo, ao abrir uma nova janela.

## SYNTAX

```
Enable-AzContextAutosave [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRITIVO

Permite que as informações de contexto do Azure sejam salvas e carregadas automaticamente quando um processo do PowerShell é iniciado. O contexto é salvo no final da execução de qualquer cmdlet que afete o contexto. Por exemplo, qualquer cmdlet de perfil. Se você estiver usando a autenticação de usuário, os tokens podem ser atualizados durante o curso da execução de qualquer cmdlet.

## EXEMPLOS

### Exemplo 1: habilitar a gravação de credenciais para o usuário atual

Ative o salvamento automático de credenciais para o usuário atual. Sempre que uma janela do PowerShell é aberta, seu contexto atual é lembrado sem fazer logon.

```powershell
Enable-AzContextAutosave
```

### Exemplo 2

Permitir que a credencial do Azure, a conta e as informações de assinatura sejam salvas e carregadas automaticamente quando você abrir uma janela do PowerShell nesta sessão do PowerShell. (gerado automaticamente)

```powershell <!-- Aladdin Generated Example -->
Enable-AzContextAutosave -Scope Process
```

## OS

### -DefaultProfile

As credenciais, o locatário e a assinatura usados para comunicação com o Azure

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

Determina o escopo das alterações de contexto. Por exemplo, se as alterações se aplicam somente ao processo atual ou a todas as sessões iniciadas por esse usuário. As alterações feitas com o escopo `CurrentUser` afetarão todas as sessões do PowerShell iniciadas pelo usuário. Se uma sessão específica precisa ter configurações diferentes, use o escopo `Process` .

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

### -Confirme

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

Mostra o que aconteceria se o cmdlet fosse executado.
O cmdlet não está em execução.

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

### Parâmetros comuns

Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## SENSORES

### Nenhuma

## EXIBE

### Microsoft. Azure. Commands. Common. Authentication. ContextAutosaveSettings

## INFORMA

## LINKS RELACIONADOS
