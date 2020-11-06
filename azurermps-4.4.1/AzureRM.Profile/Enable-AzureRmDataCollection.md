---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.profile
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Enable-AzureRmDataCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Enable-AzureRmDataCollection.md
ms.openlocfilehash: 4a29a1d57d903edb0e19689750de2bad45b2c2f4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430685"
---
# Enable-AzureRmDataCollection

## Sinopse
Permite que o Azure PowerShell colete dados para melhorar a experiência do usuário com cmdlets do AzurePowerShell.
Executar esse cmdlet é ativado para a coleta de dados do usuário atual no computador atual.
Nenhum dado será coletado, a menos que você explicitamente opte por fazê-lo.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

```
Enable-AzureRmDataCollection [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRITIVO
Você pode melhorar a experiência de usar o Microsoft Cloud e o PowerShell do Azure, optando pela coleta de dados.
O PowerShell do Azure não coleta dados sem o seu consentimento-você deve optar explicitamente por meio da execução de Enable-AzureRmDataCollection ou respondendo Sim quando o PowerShell do Azure solicitar a coleta de dados na primeira vez que você executar um cmdlet.
A Microsoft agrega dados coletados para identificar padrões de uso, identificar problemas comuns e melhorar a experiência de usar o PowerShell do Azure.
O Microsoft Azure PowerShell não coleta dados particulares nem qualquer informação que possa identificá-lo pessoalmente.

Execute o cmdlet Enable-AzureRMDataCollection para habilitar a coleta de dados para o usuário atual no computador atual.
Isso impedirá que o usuário atual seja avisado sobre a coleta de dados na primeira vez que cmdlets são executados.

Para desabilitar a coleta de dados para o usuário atual, execute o cmdlet Disable-AzureRmDataCollection.

## EXEMPLOS

### Exemplo 1: Habilitando a coleta de dados para o usuário atual
```
PS C:\> Enable-AzureRmDataCollection
```

Este exemplo mostra como habilitar a coleta de dados para o usuário atual.

## OS

### -DefaultProfile
As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.

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
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

## EXIBE

### Nenhuma

## INFORMA

## LINKS RELACIONADOS

[Disable-AzureRmDataCollection](./Disable-AzureRmDataCollection.md)

