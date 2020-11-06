---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: F22E14D6-B18B-4136-B1DF-710DA34372C3
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabasesecureconnectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseSecureConnectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseSecureConnectionPolicy.md
ms.openlocfilehash: b29af2f5f8931876d1bf23d05072e92dc4eb588e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93599016"
---
# Get-AzSqlDatabaseSecureConnectionPolicy

## Sinopse
Obtém a política de conexão segura para um banco de dados.

## SYNTAX

```
Get-AzSqlDatabaseSecureConnectionPolicy [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Get-AzSqlDatabaseSecureConnectionPolicy** Obtém a política de canal criptografado de um banco de dados SQL do Azure.
Para usar o cmdlet, use os parâmetros *ResourceGroupName* , *ServerName* e *DatabaseName* para identificar o banco de dados.
Depois que o cmdlet é executado com êxito, ele retorna um objeto que descreve a política de canal criptografado atual e também os identificadores de banco de dados.
Os identificadores de banco de dados incluem, entre outros, **ResourceGroupName** , **nomedoservidor** e **DatabaseName**.
Esse cmdlet também é compatível com o serviço Stretch Database do SQL Server no Azure.

## EXEMPLOS

### Exemplo 1: obter a política de canal criptografado de um banco de dados SQL do Azure
```
PS C:\>Get-AzSqlDatabaseSecureConnectionPolicy -ResourceGroupName "resourcegroup01" -ServerName "server01" -DatabaseName "database01"
DatabaseName          : database01
ConnectionStrings     : Microsoft.Azure.Commands.Sql.SecureConnection.Model.ConnectionStrings
ResourceGroupName     : resourcegroup01
ServerName            : server01
ProxyDnsName          : server01.database.secure.windows.net
ProxyPort             : 1433
SecureConnectionState : Optional
```

Esse comando obtém a política de canal criptografado de um banco de dados SQL do Azure chamado database01 localizado no servidor Server01.

## OS

### -DatabaseName
Especifica o nome do banco de dados.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
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

### -ResourceGroupName
Especifica o nome do grupo de recursos ao qual o banco de dados está atribuído.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Nomedoservidor
Especifica o nome do servidor que hospeda o banco de dados.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
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
Mostra o que aconteceria se o cmdlet fosse executado.
O cmdlet não é executado.

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
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).

## SENSORES

### System. String

## EXIBE

### Microsoft. Azure. Commands. Sql. SecureConnection. Model. DatabaseSecureConnectionPolicyModel

## INFORMA

## LINKS RELACIONADOS
