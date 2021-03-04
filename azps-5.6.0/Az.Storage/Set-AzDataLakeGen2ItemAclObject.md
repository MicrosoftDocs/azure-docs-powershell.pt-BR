---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/set-azdatalakegen2itemaclobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzDataLakeGen2ItemAclObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzDataLakeGen2ItemAclObject.md
ms.openlocfilehash: 6396da138a0bafd54241f859c107601a1ce14b32
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889597"
---
# Set-AzDataLakeGen2ItemAclObject

## SYNOPSIS
Cria/atualiza um objeto ACL de item dataLake gen2, que pode ser usado Update-AzDataLakeGen2Item cmdlet.

## SINTAXE

```
Set-AzDataLakeGen2ItemAclObject [-EntityId <String>] [-DefaultScope] -Permission <String>
 [-InputObject <PSPathAccessControlEntry[]>] -AccessControlType <AccessControlType> [<CommonParameters>]
```

## DESCRIPTION
O cmdlet **Set-AzDataLakeGen2ItemAclObject** cria/atualiza um objeto dataLake gen2 item ACL, que pode ser usado em um cmdlet Update-AzDataLakeGen2Item.
Se a nova entrada ACL com o mesmo AccessControlType/EntityId/DefaultScope não existir na ACL de entrada, criará uma nova entrada ACL, senão atualizará a permissão da entrada ACL existente.

## EXEMPLOS

### Exemplo 1: Criar um objeto ACL com entrada 3 ACL e atualizar a ACL em um diretório
```
PS C:\>$acl = Set-AzDataLakeGen2ItemAclObject -AccessControlType user -Permission rwx -DefaultScope
PS C:\>$acl = Set-AzDataLakeGen2ItemAclObject -AccessControlType group -Permission rw- -InputObject $acl 
PS C:\>$acl = Set-AzDataLakeGen2ItemAclObject -AccessControlType other -Permission "rw-" -InputObject $acl
PS C:\>Update-AzDataLakeGen2Item -FileSystem "filesystem1" -Path "dir1/dir3" -ACL $acl

   FileSystem Name: filesystem1

Path                 IsDirectory  Length          LastModified         Permissions  Owner                Group               
----                 -----------  ------          ------------         -----------  -----                -----               
dir1/dir3            True                         2020-03-23 09:34:31Z rwxrw-rw-+   $superuser           $superuser
```

Este comando cria um objeto ACL com 3 entradas ACL (use o parâmetro -InputObject para adicionar entrada de acl ao objeto acl existente) e atualiza a ACL em um diretório.

### Exemplo 2: Criar um objeto ACL com 4 entradas ACL e atualizar a permissão de uma entrada ACL existente
```
PS C:\>$acl = Set-AzDataLakeGen2ItemAclObject -AccessControlType user -Permission rwx -DefaultScope
PS C:\>$acl = Set-AzDataLakeGen2ItemAclObject -AccessControlType group -Permission rw- -InputObject $acl 
PS C:\>$acl = Set-AzDataLakeGen2ItemAclObject -AccessControlType other -Permission "rw-" -InputObject $acl
PS C:\>$acl = Set-AzDataLakeGen2ItemAclObject -AccessControlType user -EntityId $id -Permission rwx -InputObject $acl 
PS C:\>$acl

DefaultScope AccessControlType EntityId                             Permissions
------------ ----------------- --------                             -----------
True         User                                                   rwx        
False        Group                                                  rw-        
False        Other                                                  rw-        
False        User              ********-****-****-****-************ rwx        

PS C:\>$acl = Set-AzDataLakeGen2ItemAclObject -AccessControlType user -EntityId $id -Permission r-x -InputObject $acl 
PS C:\>$acl  

DefaultScope AccessControlType EntityId                             Permissions
------------ ----------------- --------                             -----------
True         User                                                   rwx        
False        Group                                                  rw-        
False        Other                                                  rw-        
False        User              ********-****-****-****-************ r-x
```

Este comando cria primeiro um objeto ACL com 4 entradas ACL e, em seguida, execute o cmdlet novamente com uma permissão diferente, mas o mesmo AccessControlType/EntityId/DefaultScope de uma entrada ACL existente.
Em seguida, a permissão da entrada ACL é atualizada, mas nenhuma nova entrada ACL é adicionada.

## PARÂMETROS

### -AccessControlType
Há quatro tipos: "usuário" concede direitos ao proprietário ou a um usuário nomeado, "group" concede direitos ao grupo proprietário ou a um grupo nomeado, "máscara" restringe direitos concedidos a usuários nomeados e aos membros de grupos e "outros" concede direitos a todos os usuários não encontrados em nenhuma das outras entradas.

```yaml
Type: Azure.Storage.Files.DataLake.Models.AccessControlType
Parameter Sets: (All)
Aliases:
Accepted values: User, Group, Mask, Other

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultScope
De definir esse parâmetro para indicar que o ACE pertence à ACL padrão de um diretório; caso contrário, o escopo está implícito e o ACE pertence à ACL de acesso.

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

### -EntityId
O identificador de usuário ou grupo.
Ele é omitido para entradas de AccessControlType "mask" e "other".
O identificador de usuário ou grupo também é omitido para o proprietário e o grupo proprietário.

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

### -InputObject
Se o objeto PSPathAccessControlEntry for de entrada, adicionará o novo ACL como um novo elemento do \[ \] objeto PSPathAccessControlEntry de \[ \] entrada.

```yaml
Type: Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSPathAccessControlEntry[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Permission
O campo de permissão é uma sequência de 3 caracteres onde o primeiro caractere é 'r' para conceder acesso de leitura, o segundo caractere é 'w' para conceder acesso a gravação e o terceiro caractere é 'x' para conceder permissão de execução.
Se o acesso não for concedido, o caractere '-' será usado para indicar que a permissão foi negada.

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

### CommonParameters
Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUTS

### Nenhum

## SAÍDAS

### Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSPathAccessControlEntry

## NOTES

## LINKS RELACIONADOS
