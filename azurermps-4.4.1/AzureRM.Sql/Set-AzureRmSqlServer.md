---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: FAAF458C-1662-4130-9A16-0514B714D11D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServer.md
ms.openlocfilehash: 9eb0e0503d1a7a7b71cac8f9f71a7c2f18847bca
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429023"
---
# Set-AzureRmSqlServer

## Sinopse
Modifica as propriedades de um servidor de banco de dados SQL.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

```
Set-AzureRmSqlServer [-ServerName] <String> [-SqlAdministratorPassword <SecureString>] [-Tags <Hashtable>]
 [-ServerVersion <String>] [-AssignIdentity] [-Force] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **set-AzureRmSqlServer** modifica as propriedades de um servidor de banco de dados SQL do Azure.

## EXEMPLOS

### Exemplo 1: redefinir a senha de administrador
```
PS C:\>$ServerPassword = "newpassword"
PS C:\> $SecureString = ConvertTo-SecureString $ServerPassword -AsPlainText -Force
PS C:\> Set-AzureRmSqlServer -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -SqlAdministratorPassword $secureString
ResourceGroupName        : ResourceGroup01
ServerName               : Server01
Location                 : Australia East
SqlAdministratorLogin    : adminLogin
SqlAdministratorPassword :
ServerVersion            : 12.0
Tags                     :
```

Esse comando redefine a senha de administrador no servidor AzureSQL chamado Server01.

## OS

### -AssignIdentity
Gerar e atribuir uma identidade do Azure Active Directory para este servidor para uso com serviços de gerenciamento de chaves como o cofre de chaves do Azure.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force
Força o comando a ser executado sem pedir confirmação do usuário.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
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
Especifica o nome do servidor que esse cmdlet modifica.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ServerVersion
Especifica a versão para a qual esse cmdlet altera o servidor. Os valores aceitáveis para esse parâmetro são: 2,0 e 12,0.

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

### -SqlAdministratorPassword
Especifica uma nova senha, como uma **SecureString** , para o administrador do servidor de banco de dados. Para obter uma **SecureString** , use o cmdlet Get-Credential. Para obter mais informações, digite `Get-Help
ConvertTo-SecureString` .

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Marcas
Especifica um dicionário de marcas que este cmdlet associa ao servidor. Pares de valores chave na forma de uma tabela de hash definidas como marcas no servidor. Por exemplo:

@ {Key0 = "value0"; key1 = $null; Key2 = "value2"}

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tag

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

### Microsoft. Azure. Commands. Sql. Server. Model. AzureSqlServerModel

## INFORMA

## LINKS RELACIONADOS

[Documentação do banco de dados SQL](https://docs.microsoft.com/azure/sql-database/)
