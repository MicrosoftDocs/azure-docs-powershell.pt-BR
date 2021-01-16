---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 7D27F7B1-BAF8-4A01-8BA7-A75A4CFAE370
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/get-azdatalakestorefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreFirewallRule.md
ms.openlocfilehash: c681ba089487868b556bd6e0ae198384a0dadd8c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98259572"
---
# Get-AzDataLakeStoreFirewallRule

## Sinopse
Obtém as regras de firewall especificadas no repositório data Lake especificado.
Se nenhuma regra de firewall for especificada, lista todas as regras de firewall da conta.

## SYNTAX

```
Get-AzDataLakeStoreFirewallRule [-Account] <String> [[-Name] <String>] [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet Get-AzDataLakeStoreFirewallRule Obtém as regras de firewall especificadas no repositório data Lake especificado.
Se nenhuma regra de firewall for especificada, lista todas as regras de firewall da conta.

## EXEMPLOS

### Exemplo 1: recuperar uma regra de firewall específica
```
PS C:\> Get-AzDataLakeStoreFirewallRule -AccountName "ContosoADL" -Name MyFirewallRule
```

Retorna a regra de firewall chamada "MyFirewallRule" da conta "ContosoADL"

### Exemplo 2: listar todas as regras de firewall em uma conta
```
PS C:\> Get-AzDataLakeStoreFirewallRule -AccountName "ContosoADL"
```

Retorna todas as regras de firewall na conta "ContosoADL"

## OS

### -Conta
A conta do data Lake Store da qual recuperar a regra de firewall.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure

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

### -Nome
O nome da regra de firewall a ser recuperada

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Nome do grupo de recursos sob o qual deseja recuperar a regra de firewall especificada da conta especificada.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

### System. String

## EXIBE

### Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStoreFirewallRule

## INFORMA

## LINKS RELACIONADOS
