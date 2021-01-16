---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azdatalakegen2itemaclobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzDataLakeGen2ItemACLObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzDataLakeGen2ItemACLObject.md
ms.openlocfilehash: d16a476bea988afb53ddff7b34a83658e0f274e1
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98260772"
---
# Set-AzDataLakeGen2ItemAclObject

## Sinopse
Cria/atualiza um objeto ACL de item datalake Gen2, que pode ser usado no cmdlet Update-AzDataLakeGen2Item.

## SYNTAX

```
Set-AzDataLakeGen2ItemAclObject [-EntityId <String>] [-DefaultScope] -Permission <String>
 [-InputObject <PSPathAccessControlEntry[]>] -AccessControlType <AccessControlType> [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **set-AzDataLakeGen2ItemAclObject** cria/atualiza um objeto ACL de item datalake Gen2, que pode ser usado no cmdlet Update-AzDataLakeGen2Item.
Se a nova entrada ACL com o mesmo AccessControlType/EntityId/DefaultScope não existir na ACL de entrada, criará uma nova entrada ACL, senão a permissão de atualização da entrada ACL existente.

## EXEMPLOS

### Exemplo 1: criar um objeto ACL com 3 entrada de ACL e atualizar a ACL em um diretório
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

Esse comando cria um objeto ACL com 3 entradas ACL (use-InputObject para adicionar a entrada ACL ao objeto ACL existente) e atualiza a ACL em um diretório.

### Exemplo 2: criar um objeto ACL com quatro entradas ACL e atualizar a permissão de uma entrada ACL existente
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

Esse comando primeiro cria um objeto ACL com quatro entradas ACL e, em seguida, executa o cmdlet novamente com uma permissão diferente, mas mesmo AccessControlType/EntityId/DefaultScope de uma entrada ACL existente.
Em seguida, a permissão da entrada ACL será atualizada, mas nenhuma nova entrada ACL será adicionada.

## OS

### -AccessControlType
Há quatro tipos: "usuário" concede direitos ao proprietário ou a um usuário nomeado, "grupo" concede direitos para o grupo proprietário ou um grupo nomeado, "Mask" restringe os direitos concedidos a usuários nomeados e os membros dos grupos e "outros" concede direitos a todos os usuários não encontrados em nenhuma das outras entradas.

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
Defina esse parâmetro para indicar que a ACE pertence à ACL padrão para um diretório; caso contrário, o escopo é implícito e a ACE pertence à ACL do Access.

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
Ele é omitido para entradas de AccessControlType "máscara" e "outros".
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
Se a entrada do \[ \] objeto PSPathAccessControlEntry, adicionará a nova ACL como um novo elemento do objeto PSPathAccessControlEntry de entrada \[ \] .

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

### -Permissão
O campo Permission é uma sequência de 3 caracteres onde o primeiro caractere é ' r ' para conceder acesso de leitura, o segundo caractere é ' w ' para conceder acesso de gravação, e o terceiro caractere é ' x ' para conceder permissão de execução.
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
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

### Nenhuma

## EXIBE

### Microsoft. WindowsAzure. Commands. Storage. Model. ResourceModel. PSPathAccessControlEntry

## INFORMA

## LINKS RELACIONADOS
