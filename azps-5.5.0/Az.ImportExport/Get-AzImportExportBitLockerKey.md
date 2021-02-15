---
external help file: ''
Module Name: Az.ImportExport
online version: https://docs.microsoft.com/en-us/powershell/module/az.importexport/get-azimportexportbitlockerkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Get-AzImportExportBitLockerKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Get-AzImportExportBitLockerKey.md
ms.openlocfilehash: 5f7a1fe5e8b80f6847bc3b3ca063d7166bf3ea95
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118972"
---
# Get-AzImportExportBitLockerKey

## Sinopse
Retorna as Teclas BitLocker para todas as unidades no trabalho especificado.

## Sintaxe

```
Get-AzImportExportBitLockerKey -JobName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-AcceptLanguage <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## Descrição
Retorna as Teclas BitLocker para todas as unidades no trabalho especificado.

## Exemplos

### Exemplo 1: Listar todas as Chaves do BitLocker no trabalho ImportExport especificado
```powershell
PS C:\> Get-AzImportExportBitLockerKey -JobName test-job -ResourceGroupName ImportTestRG 
BitLockerKey                                            DriveId
------------                                            -------
238810-662376-448998-450120-652806-203390-606320-483076 9CA995BA
```

Este cmdlet lista todas as Teclas BitLocker no trabalho ImportExport especificado.

## Parâmetros

### -AcceptLanguage
Especifica o idioma preferencial para a resposta.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -JobName
O nome do trabalho de importação/exportação.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
O nome do grupo de recursos identifica exclusivamente o grupo de recursos dentro da assinatura do usuário.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubscriptionId
A ID da assinatura do usuário do Azure.

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## Entradas

## Saídas

### Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.Api20161101.IDriveBitLockerKey

## Notas

Aliases

## LINKS RELACIONADOS

