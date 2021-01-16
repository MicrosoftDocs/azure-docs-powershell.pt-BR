---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/enable-azdatacollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Enable-AzDataCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Enable-AzDataCollection.md
ms.openlocfilehash: a8087f41c33dc3bb066609393a87986d5016d1ae
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98258246"
---
# Enable-AzDataCollection

## Sinopse
Permite que o Azure PowerShell colete dados para melhorar a experiência do usuário com os cmdlets do PowerShell do Azure. Executar esse cmdlet é ativado para a coleta de dados do usuário atual no computador atual. Os dados são coletados por padrão, a menos que você explicitamente opte por sair.

## SYNTAX

```
Enable-AzDataCollection [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRITIVO

O `Enable-AzDataCollection` cmdlet é usado para aceitar a coleta de dados. O PowerShell do Azure coleta automaticamente dados de telemetria por padrão. A Microsoft agrega dados coletados para identificar padrões de uso, identificar problemas comuns e melhorar a experiência do PowerShell do Azure.
O Microsoft Azure PowerShell não coleta nenhum dado particular ou pessoal. Para desabilitar a coleta de dados, você deve explicitamente optar por executar `Disable-AzDataCollection` .

## EXEMPLOS

### Exemplo 1: Habilitando a coleta de dados para o usuário atual

O exemplo a seguir mostra como habilitar a coleta de dados para o usuário atual.

```powershell
Enable-AzDataCollection
```

## OS

### -DefaultProfile

As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.

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

### -Confirme

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

Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte [about_CommonParameters](/powershell/module/microsoft.powershell.core/about/about_commonparameters).

## SENSORES

### Nenhuma

## EXIBE

### System. void

## INFORMA

## LINKS RELACIONADOS

[Disable-AzDataCollection](./Disable-AzDataCollection.md)
