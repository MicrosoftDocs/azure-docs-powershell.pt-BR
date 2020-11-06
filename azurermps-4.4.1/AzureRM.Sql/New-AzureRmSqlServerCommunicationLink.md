---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 52664E45-7EAB-41C9-BF78-304F10BFC51A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlServerCommunicationLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlServerCommunicationLink.md
ms.openlocfilehash: ac2ec676143ef1179adbfeb793bd787d81e8f435
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427749"
---
# New-AzureRmSqlServerCommunicationLink

## Sinopse
Cria um link de comunicação para transações de banco de dados elástico entre dois servidores de banco de dados SQL.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

```
New-AzureRmSqlServerCommunicationLink -LinkName <String> -PartnerServer <String> [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **New-AzureRmSqlServerCommunicationLink** cria um link de comunicação para transações de banco de dados elástico entre dois servidores lógicos no banco de dados SQL do Azure.
Transações de banco de dados elástico podem abranger bancos de dados em qualquer um dos servidores emparelhados.
Você pode criar mais de um link em um servidor.
Portanto, as transações de banco de dados elástico podem se estender por um número maior de servidores.

## EXEMPLOS

### Exemplo 1: criar um link de comunicação
```
PS C:\>New-AzureRmSqlServerCommunicationLink -ResourceGroupName "ResourceGroup01" -ServerName "ContosoServer17" -LinkName "Link01" -PartnerServer "ContosoServer02"
```

Esse comando cria um link chamado Link01 entre ContosoServer17 e ContosoServer02.

## OS

### -LinkId
Especifica o nome do link de comunicação do servidor que este cmdlet cria.

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

### -PartnerServer
Especifica o nome do outro servidor que faz parte deste link de comunicação.

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
Especifica o nome do grupo de recursos ao qual o servidor especificado pelo parâmetro *ServerName* pertence.

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
Especifica o nome do servidor no qual esse cmdlet configura o link de comunicação.

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

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

## EXIBE

### Microsoft. Azure. Commands. Sql. Server. Model. AzureSqlServerCommunicationLinkModel

## INFORMA
* Palavras-chave: Azure, azurerm, ARM, Resource, Management, Manager, SQL, Database, MSSQL

## LINKS RELACIONADOS

[Get-AzureRmSqlServerCommunicationLink](./Get-AzureRmSqlServerCommunicationLink.md)

[Remove-AzureRmSqlServerCommunicationLink](./Remove-AzureRmSqlServerCommunicationLink.md)

[Documentação do banco de dados SQL](https://docs.microsoft.com/azure/sql-database/)
