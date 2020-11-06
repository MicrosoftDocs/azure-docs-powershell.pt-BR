---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 60E0D10F-9B93-45A9-A1FF-5C943B8CA09C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerActiveDirectoryAdministrator.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerActiveDirectoryAdministrator.md
ms.openlocfilehash: 76d5c2fc90b4e0e518aa022a97c6b9ce369715db
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431763"
---
# Set-AzureRmSqlServerActiveDirectoryAdministrator

## Sinopse
Provisiona um administrador do Azure AD para SQL Server.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

```
Set-AzureRmSqlServerActiveDirectoryAdministrator [-DisplayName] <String> [[-ObjectId] <Guid>]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **set-AzureRmSqlServerActiveDirectoryAdministrator** provisiona um administrador do Azure Active Directory (Azure AD) para AzureSQL Server na assinatura atual.

Você pode provisionar apenas um administrador de cada vez.

Os seguintes membros do Azure AD podem ser provisionados como um administrador do SQL Server:

- Membros nativos do Azure AD 
- Membros federados do Azure AD 
- Membros importados de outros anúncios do Azure que são membros nativos ou federados 
- Grupos do Azure AD criados como grupos de segurança

Contas da Microsoft, como os dos domínios Outlook.com, Hotmail.com ou Live.com, não são compatíveis com administradores.
Não há suporte para outras contas de convidado, como aquelas dos domínios Gmail.com ou Yahoo.com como administradores.

Recomendamos que você provisione um grupo dedicado do Azure AD como administrador.

## EXEMPLOS

### Exemplo 1: configurar um grupo de administradores para um servidor
```
PS C:\>Set-AzureRmSqlServerActiveDirectoryAdministrator -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DisplayName "DBAs" 
ResourceGroupName ServerName DisplayName ObjectId 
----------------- ---------- ----------- -------- 
ResourceGroup01   Server01   DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b
```

Esse comando provisiona um grupo de administradores do Azure AD chamado DBAs para o servidor chamado Server01.
Este servidor está associado à ResourceGroup01 do grupo de recursos.

### Exemplo 2: prover um usuário administrador para um servidor
```
PS C:\>Set-AzureRmSqlServerActiveDirectoryAdministrator -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DisplayName "David Chew"
ResourceGroupName ServerName DisplayName ObjectId 
----------------- ---------- ----------- -------- 
resourcegroup01   server01   David Chew  11E95548-B179-4FE1-9AF4-ACA49D13ABB9
```

Esse comando provisiona um usuário do Azure AD como administrador para o servidor chamado Server01.

### Exemplo 3: provisionar um grupo de administradores especificando sua ID
```
PS C:\>Set-AzureRmSqlServerActiveDirectoryAdministrator -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DisplayName "DBAs" -ObjectId "40b79501-b343-44ed-9ce7-da4c8cc7353b"
ResourceGroupName ServerName DisplayName ObjectId 
----------------- ---------- ----------- -------- 
ResourceGroup01   Server01   DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b
```

Esse comando provisiona um grupo de administradores do Azure AD chamado DBAs para o servidor chamado Server01.
O comando especifica uma ID para o parâmetro *ObjectID* .
Isso garante que o comando tenha êxito mesmo se o nome de exibição do grupo não for exclusivo.

## OS

### -DisplayName
Especifica o nome de exibição do administrador do Azure AD que este cmdlet provisiona.

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

### -ObjectId
Especifica a ID exclusiva do administrador do Azure AD que este cmdlet provisiona.
Se o nome para exibição não for exclusivo, você deve especificar um valor para esse parâmetro.

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Especifica o nome do grupo de recursos ao qual o servidor está atribuído.

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
Especifica o nome do SQL Server para o qual esse cmdlet provisiona um administrador.

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

### Microsoft. Azure. Commands. Sql. ServerActiveDirectoryAdministrator. Model. AzureSqlServerActiveDirectoryAdministratorModel

## INFORMA

## LINKS RELACIONADOS

[Get-AzureRmSqlServerActiveDirectoryAdministrator](./Get-AzureRmSqlServerActiveDirectoryAdministrator.md)

[Remove-AzureRmSqlServerActiveDirectoryAdministrator](./Remove-AzureRmSqlServerActiveDirectoryAdministrator.md)

[Documentação do banco de dados SQL](https://docs.microsoft.com/azure/sql-database/)


