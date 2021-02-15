---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azdatalakegen2itemaclobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzDataLakeGen2ItemAclObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzDataLakeGen2ItemAclObject.md
ms.openlocfilehash: 209cb5ded738faabfdafc113d3d9524f7c01e927
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118911"
---
# <span data-ttu-id="5adbb-101">Set-AzDataLakeGen2ItemAclObject</span><span class="sxs-lookup"><span data-stu-id="5adbb-101">Set-AzDataLakeGen2ItemAclObject</span></span>

## <span data-ttu-id="5adbb-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5adbb-102">SYNOPSIS</span></span>
<span data-ttu-id="5adbb-103">Cria/atualiza um objeto ACL de item dataLake gen2, que pode ser usado no cmdlet Update-AzDataLakeGen2Item dataLake.</span><span class="sxs-lookup"><span data-stu-id="5adbb-103">Creates/Updates a DataLake gen2 item ACL object, which can be used in Update-AzDataLakeGen2Item cmdlet.</span></span>

## <span data-ttu-id="5adbb-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5adbb-104">SYNTAX</span></span>

```
Set-AzDataLakeGen2ItemAclObject [-EntityId <String>] [-DefaultScope] -Permission <String>
 [-InputObject <PSPathAccessControlEntry[]>] -AccessControlType <AccessControlType> [<CommonParameters>]
```

## <span data-ttu-id="5adbb-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="5adbb-105">DESCRIPTION</span></span>
<span data-ttu-id="5adbb-106">O cmdlet **Set-AzDataLakeGen2ItemAclObject** cria/atualiza um objeto ACL de item dataLake gen2, que pode ser usado no cmdlet Update-AzDataLakeGen2Item.</span><span class="sxs-lookup"><span data-stu-id="5adbb-106">The **Set-AzDataLakeGen2ItemAclObject** cmdlet creates/updates a DataLake gen2 item ACL object, which can be used in Update-AzDataLakeGen2Item cmdlet.</span></span>
<span data-ttu-id="5adbb-107">Se a nova entrada ACL com o mesmo AccessControlType/EntityId/DefaultScope não existir na ACL de entrada, criará uma nova entrada ACL, ou atualizará a permissão da entrada ACL existente.</span><span class="sxs-lookup"><span data-stu-id="5adbb-107">If the new ACL entry with same AccessControlType/EntityId/DefaultScope not exist in the input ACL, will create a new ACL entry, else update permission of existing ACL entry.</span></span>

## <span data-ttu-id="5adbb-108">Exemplos</span><span class="sxs-lookup"><span data-stu-id="5adbb-108">EXAMPLES</span></span>

### <span data-ttu-id="5adbb-109">Exemplo 1: Criar um objeto ACL com entrada 3 ACL e atualizar ACL em um diretório</span><span class="sxs-lookup"><span data-stu-id="5adbb-109">Example 1: Create an ACL object with 3 ACL entry, and update ACL on a directory</span></span>
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

<span data-ttu-id="5adbb-110">Esse comando cria um objeto ACL com 3 entradas ACL (use o parâmetro -InputObject para adicionar entrada de acl ao objeto acl existente) e atualiza o ACL em um diretório.</span><span class="sxs-lookup"><span data-stu-id="5adbb-110">This command creates an ACL object with 3 ACL entries (use -InputObject parameter to add acl entry to existing acl object), and updates ACL on a directory.</span></span>

### <span data-ttu-id="5adbb-111">Exemplo 2: Criar um objeto ACL com 4 entradas ACL e atualizar a permissão de uma entrada ACL existente</span><span class="sxs-lookup"><span data-stu-id="5adbb-111">Example 2: Create an ACL object with 4 ACL entries, and update permission of an existing ACL entry</span></span>
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

<span data-ttu-id="5adbb-112">Esse comando primeiro cria um objeto ACL com 4 entradas ACL e, em seguida, execute o cmdlet novamente com permissão diferente, mas mesmo AccessControlType/EntityId/DefaultScope de uma entrada ACL existente.</span><span class="sxs-lookup"><span data-stu-id="5adbb-112">This command first creates an ACL object with 4 ACL entries, then run the cmdlet again with different permission but same AccessControlType/EntityId/DefaultScope of an existing ACL entry.</span></span>
<span data-ttu-id="5adbb-113">Em seguida, a permissão da entrada ACL é atualizada, mas nenhuma nova entrada ACL é adicionada.</span><span class="sxs-lookup"><span data-stu-id="5adbb-113">Then the permission of the ACL entry is updated, but no new ACL entry is added.</span></span>

## <span data-ttu-id="5adbb-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5adbb-114">PARAMETERS</span></span>

### <span data-ttu-id="5adbb-115">-AccessControlType</span><span class="sxs-lookup"><span data-stu-id="5adbb-115">-AccessControlType</span></span>
<span data-ttu-id="5adbb-116">Há quatro tipos: "usuário" concede direitos ao proprietário ou a um usuário nomeado, "grupo" concede direitos ao grupo proprietário ou a um grupo nomeado, "máscara" restringe os direitos concedidos a usuários nomeados e aos membros de grupos e "outros" concede direitos a todos os usuários não encontrados em nenhuma das outras entradas.</span><span class="sxs-lookup"><span data-stu-id="5adbb-116">There are four types: "user" grants rights to the owner or a named user, "group" grants rights to the owning group or a named group, "mask" restricts rights granted to named users and the members of groups, and "other" grants rights to all users not found in any of the other entries.</span></span>

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

### <span data-ttu-id="5adbb-117">-DefaultScope</span><span class="sxs-lookup"><span data-stu-id="5adbb-117">-DefaultScope</span></span>
<span data-ttu-id="5adbb-118">Delimi este parâmetro para indicar que o ACE pertence ao ACL padrão de um diretório; caso contrário, o escopo está implícito e o ACE pertence ao ACL de acesso.</span><span class="sxs-lookup"><span data-stu-id="5adbb-118">Set this parameter to indicate the ACE belongs to the default ACL for a directory; otherwise scope is implicit and the ACE belongs to the access ACL.</span></span>

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

### <span data-ttu-id="5adbb-119">-EntityId</span><span class="sxs-lookup"><span data-stu-id="5adbb-119">-EntityId</span></span>
<span data-ttu-id="5adbb-120">O identificador de usuário ou grupo.</span><span class="sxs-lookup"><span data-stu-id="5adbb-120">The user or group identifier.</span></span>
<span data-ttu-id="5adbb-121">Ele é omitido para entradas de "máscara" e "outros" do AccessControlType.</span><span class="sxs-lookup"><span data-stu-id="5adbb-121">It is omitted for entries of AccessControlType "mask" and "other".</span></span>
<span data-ttu-id="5adbb-122">O identificador de usuário ou grupo também é omitido para o proprietário e o grupo proprietário.</span><span class="sxs-lookup"><span data-stu-id="5adbb-122">The user or group identifier is also omitted for the owner and owning group.</span></span>

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

### <span data-ttu-id="5adbb-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5adbb-123">-InputObject</span></span>
<span data-ttu-id="5adbb-124">Se você inserir o objeto PSPathAccessControlEntry, adicionará o novo ACL como um novo elemento do objeto \[ \] PSPathAccessControlEntry de \[ \] entrada.</span><span class="sxs-lookup"><span data-stu-id="5adbb-124">If input the PSPathAccessControlEntry\[\] object, will add the new ACL as a new element of the input PSPathAccessControlEntry\[\] object.</span></span>

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

### <span data-ttu-id="5adbb-125">-Permissão</span><span class="sxs-lookup"><span data-stu-id="5adbb-125">-Permission</span></span>
<span data-ttu-id="5adbb-126">O campo de permissão é uma sequência de 3 caracteres onde o primeiro caractere é 'r' para conceder acesso de leitura, o segundo caractere é 'w' para conceder acesso à gravação e o terceiro caractere é 'x' para conceder permissão de execução.</span><span class="sxs-lookup"><span data-stu-id="5adbb-126">The permission field is a 3-character sequence where the first character is 'r' to grant read access, the second character is 'w' to grant write access, and the third character is 'x' to grant execute permission.</span></span>
<span data-ttu-id="5adbb-127">Se o acesso não for concedido, o caractere '-' será usado para indicar que a permissão foi negada.</span><span class="sxs-lookup"><span data-stu-id="5adbb-127">If access is not granted, the '-' character is used to denote that the permission is denied.</span></span>

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

### <span data-ttu-id="5adbb-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5adbb-128">CommonParameters</span></span>
<span data-ttu-id="5adbb-129">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5adbb-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5adbb-130">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5adbb-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5adbb-131">Entradas</span><span class="sxs-lookup"><span data-stu-id="5adbb-131">INPUTS</span></span>

### <span data-ttu-id="5adbb-132">Nenhum</span><span class="sxs-lookup"><span data-stu-id="5adbb-132">None</span></span>

## <span data-ttu-id="5adbb-133">Saídas</span><span class="sxs-lookup"><span data-stu-id="5adbb-133">OUTPUTS</span></span>

### <span data-ttu-id="5adbb-134">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSPathAccessControlEntry</span><span class="sxs-lookup"><span data-stu-id="5adbb-134">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSPathAccessControlEntry</span></span>

## <span data-ttu-id="5adbb-135">Notas</span><span class="sxs-lookup"><span data-stu-id="5adbb-135">NOTES</span></span>

## <span data-ttu-id="5adbb-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5adbb-136">RELATED LINKS</span></span>
