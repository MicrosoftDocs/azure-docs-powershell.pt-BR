---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.profile
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Enable-AzureRmContextAutosave.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Enable-AzureRmContextAutosave.md
ms.openlocfilehash: d785cd364cd67a9d79f8710ef664048b8f54b8ff
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430687"
---
# Enable-AzureRmContextAutosave

## Sinopse
Permitir que a credencial do Azure, a conta e as informações de assinatura sejam salvas e carregadas automaticamente quando você abrir uma janela do PowerShell. 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

```
Enable-AzureRmContextAutosave [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRITIVO
Permitir que a credencial do Azure, a conta e as informações de assinatura sejam salvas e carregadas automaticamente quando você abrir uma janela do PowerShell. 

## EXEMPLOS

### Habilitar a gravação simultânea de credenciais para o usuário atual
```
PS C:\> Enable-AzureRmContextAutosave
```

Ative o salvamento automático de credenciais para o usuário atual.  Sempre que uma janela do PowerShell é aberta, seu contexto atual será lembrado sem fazer logon.

## OS

### -DefaultProfile
As credenciais, o locatário e a assinatura usados para comunicação com o Azure

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Escopo
Determina o escopo das alterações de contexto, por exemplo, wheher alterações se aplicam somente ao processo cusrrent ou a todas as sessões iniciadas por este usuário

```yaml
Type: Microsoft.Azure.Commands.Profile.Common.ContextModificationScope
Parameter Sets: (All)
Aliases: 
Accepted values: Process, CurrentUser

Required: False
Position: Named
Default value: None
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
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

### Nenhuma

## EXIBE

### Microsoft. Azure. Commands. Common. Authentication. ContextAutosaveSettings
Informações sobre as configurações atuais de salvamento automático, incluindo se o salvamento automático está habilitado para o usuário atual e onde os arquivos de contexto e credenciais são salvos.

## INFORMA

## LINKS RELACIONADOS

