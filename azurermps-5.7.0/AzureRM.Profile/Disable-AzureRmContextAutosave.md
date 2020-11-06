---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/disable-azurermcontextautosave
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Disable-AzureRmContextAutosave.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Disable-AzureRmContextAutosave.md
ms.openlocfilehash: 622cbd399f554173bbe9734429f4ae787fe94d0f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93426659"
---
# Disable-AzureRmContextAutosave

## Sinopse
Desativar o salvamento de credenciais do Azure.  Suas informações de login serão esquecidas na próxima vez que você abrir uma janela do PowerShell

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

```
Disable-AzureRmContextAutosave [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRITIVO
Desativar o salvamento de credenciais do Azure.  Suas informações de login serão esquecidas na próxima vez que você abrir uma janela do PowerShell

## EXEMPLOS

### Desabilitar o salvamento AutoTexto
```
PS C:\> Disable-AzureRmContextAutosave
```

Desabilitar o salvamento automático do usuário atual.

## OS

### -DefaultProfile
As credenciais, o locatário e a assinatura usados para comunicação com o Azure

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Escopo
Determina o escopo das alterações de contexto, por exemplo, se as alterações se aplicam somente ao processo atual ou a todas as sessões iniciadas por este usuário

```yaml
Type: ContextModificationScope
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
Type: SwitchParameter
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
Type: SwitchParameter
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

