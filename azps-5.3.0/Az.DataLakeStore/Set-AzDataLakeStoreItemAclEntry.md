---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 0671D833-8B3A-4480-A576-92F1A9E8CE92
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/set-azdatalakestoreitemaclentry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreItemAclEntry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreItemAclEntry.md
ms.openlocfilehash: 4f432596e6165989df07187a9383da04f0929a2d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98426591"
---
# <span data-ttu-id="08bb5-101">Set-AzDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="08bb5-101">Set-AzDataLakeStoreItemAclEntry</span></span>

## <span data-ttu-id="08bb5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="08bb5-102">SYNOPSIS</span></span>
<span data-ttu-id="08bb5-103">Modifica uma entrada na ACL de um arquivo ou pasta no data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="08bb5-103">Modifies an entry in the ACL of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="08bb5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="08bb5-104">SYNTAX</span></span>

### <span data-ttu-id="08bb5-105">SetByACLObject (padrão)</span><span class="sxs-lookup"><span data-stu-id="08bb5-105">SetByACLObject (Default)</span></span>
```
Set-AzDataLakeStoreItemAclEntry [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-Acl] <DataLakeStoreItemAce[]> [-PassThru] [-Recurse] [-Concurrency <Int32>] [-ShowProgress]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="08bb5-106">SetSpecificACE</span><span class="sxs-lookup"><span data-stu-id="08bb5-106">SetSpecificACE</span></span>
```
Set-AzDataLakeStoreItemAclEntry [-Account] <String> [-Path] <DataLakeStorePathInstance> [-AceType] <AceType>
 [[-Id] <Guid>] [-Permissions] <Permission> [-Default] [-PassThru] [-Recurse] [-Concurrency <Int32>]
 [-ShowProgress] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="08bb5-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="08bb5-107">DESCRIPTION</span></span>
<span data-ttu-id="08bb5-108">O cmdlet **set-AzDataLakeStoreItemAclEntry** modifica uma Entry (ACE) na lista de controle de acesso (ACL) de um arquivo ou pasta no data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="08bb5-108">The **Set-AzDataLakeStoreItemAclEntry** cmdlet modifies an entry (ACE) in the access control list (ACL) of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="08bb5-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="08bb5-109">EXAMPLES</span></span>

### <span data-ttu-id="08bb5-110">Exemplo 1: modificar permissões para uma ACE</span><span class="sxs-lookup"><span data-stu-id="08bb5-110">Example 1: Modify permissions for an ACE</span></span>
```
PS C:\>Set-AzDataLakeStoreItemAclEntry -AccountName "ContosoADL" -Path / -AceType User -Id (Get-AzADUser -Mail "PattiFuller@contoso.com").ObjectId -Permissions All
```

<span data-ttu-id="08bb5-111">Esse comando modifica a ACE para Patti Pereira para ter todas as permissões.</span><span class="sxs-lookup"><span data-stu-id="08bb5-111">This command modifies the ACE for Patti Fuller to have all permissions.</span></span>

### <span data-ttu-id="08bb5-112">Exemplo 2: modificar permissões para uma ACE recursivamente</span><span class="sxs-lookup"><span data-stu-id="08bb5-112">Example 2: Modify permissions for an ACE recursively</span></span>
```
PS C:\>Set-AzDataLakeStoreItemAclEntry -AccountName "ContosoADL" -Path / -AceType User -Id (Get-AzADUser -Mail "PattiFuller@contoso.com").ObjectId -Permissions All -Recurse -Concurrency 128
```

### <span data-ttu-id="08bb5-113">Exemplo 3: modificar permissões para uma ACE recursivamente usando o objeto ACL</span><span class="sxs-lookup"><span data-stu-id="08bb5-113">Example 3: Modify permissions for an ACE recursively using Acl object</span></span>
```
PS C:\>$fullAcl="user:userid1:--x,default:user:userid1:--x"
PS C:\>$newFullAcl = $fullAcl.Split("{,}")
PS C:\>Set-AzDataLakeStoreItemAclEntry -AccountName "ContosoADL" -Path / -Acl $newFullAcl -Recurse -Concurrency 128
```

<span data-ttu-id="08bb5-114">Esse comando modifica recursivamente a ACE para Patti Pereira para ter todas as permissões para a raiz e todas as suas subpastas e arquivos.</span><span class="sxs-lookup"><span data-stu-id="08bb5-114">This command recursively modifies the ACE for Patti Fuller to have all permissions to root and all its subdirectories and files.</span></span>

## <span data-ttu-id="08bb5-115">OS</span><span class="sxs-lookup"><span data-stu-id="08bb5-115">PARAMETERS</span></span>

### <span data-ttu-id="08bb5-116">-Conta</span><span class="sxs-lookup"><span data-stu-id="08bb5-116">-Account</span></span>
<span data-ttu-id="08bb5-117">Especifica o nome da conta do data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="08bb5-117">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="08bb5-118">-AceType</span><span class="sxs-lookup"><span data-stu-id="08bb5-118">-AceType</span></span>
<span data-ttu-id="08bb5-119">Especifica o tipo de ACE a ser modificado.</span><span class="sxs-lookup"><span data-stu-id="08bb5-119">Specifies the type of ACE to modify.</span></span>
<span data-ttu-id="08bb5-120">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="08bb5-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="08bb5-121">Utilizador</span><span class="sxs-lookup"><span data-stu-id="08bb5-121">User</span></span> 
- <span data-ttu-id="08bb5-122">Grupos</span><span class="sxs-lookup"><span data-stu-id="08bb5-122">Group</span></span> 
- <span data-ttu-id="08bb5-123">Remoção</span><span class="sxs-lookup"><span data-stu-id="08bb5-123">Mask</span></span> 
- <span data-ttu-id="08bb5-124">Demais</span><span class="sxs-lookup"><span data-stu-id="08bb5-124">Other</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+AceType
Parameter Sets: SetSpecificACE
Aliases:
Accepted values: User, Group, Mask, Other

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="08bb5-125">-ACL</span><span class="sxs-lookup"><span data-stu-id="08bb5-125">-Acl</span></span>
<span data-ttu-id="08bb5-126">Especifica o objeto ACL que contém as entradas a serem modificadas.</span><span class="sxs-lookup"><span data-stu-id="08bb5-126">Specifies the ACL object that contains the entries to modify.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItemAce[]
Parameter Sets: SetByACLObject
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="08bb5-127">-Simultaneidade</span><span class="sxs-lookup"><span data-stu-id="08bb5-127">-Concurrency</span></span>
<span data-ttu-id="08bb5-128">Número de arquivos/diretórios processados em paralelo.</span><span class="sxs-lookup"><span data-stu-id="08bb5-128">Number of files/directories processed in parallel.</span></span> <span data-ttu-id="08bb5-129">Opcional: um padrão razoável será selecionado</span><span class="sxs-lookup"><span data-stu-id="08bb5-129">Optional: a reasonable default will be selected</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="08bb5-130">-Padrão</span><span class="sxs-lookup"><span data-stu-id="08bb5-130">-Default</span></span>
<span data-ttu-id="08bb5-131">Indica que essa operação modifica a ACE padrão da ACL especificada.</span><span class="sxs-lookup"><span data-stu-id="08bb5-131">Indicates that this operation modifies the default ACE from the specified ACL.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SetSpecificACE
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="08bb5-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08bb5-132">-DefaultProfile</span></span>
<span data-ttu-id="08bb5-133">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="08bb5-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="08bb5-134">-ID</span><span class="sxs-lookup"><span data-stu-id="08bb5-134">-Id</span></span>
<span data-ttu-id="08bb5-135">Especifica a ID de objeto do usuário, grupo ou entidade de serviço do diretório do AzureActive para o qual modificar uma ACE.</span><span class="sxs-lookup"><span data-stu-id="08bb5-135">Specifies the object ID of the AzureActive Directory user, group, or service principal for which to modify an ACE.</span></span>

```yaml
Type: System.Guid
Parameter Sets: SetSpecificACE
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="08bb5-136">-PassThru</span><span class="sxs-lookup"><span data-stu-id="08bb5-136">-PassThru</span></span>
<span data-ttu-id="08bb5-137">Indica que a ACL resultante deve ser retornada.</span><span class="sxs-lookup"><span data-stu-id="08bb5-137">Indicates the resulting ACL should be returned.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="08bb5-138">-Caminho</span><span class="sxs-lookup"><span data-stu-id="08bb5-138">-Path</span></span>
<span data-ttu-id="08bb5-139">Especifica o caminho do repositório data Lake do item para o qual modificar uma ACE, começando com o diretório raiz (/).</span><span class="sxs-lookup"><span data-stu-id="08bb5-139">Specifies the Data Lake Store path of the item for which to modify an ACE, starting with the root directory (/).</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="08bb5-140">-Permissões</span><span class="sxs-lookup"><span data-stu-id="08bb5-140">-Permissions</span></span>
<span data-ttu-id="08bb5-141">Especifica as permissões para o ACE.</span><span class="sxs-lookup"><span data-stu-id="08bb5-141">Specifies the permissions for the ACE.</span></span>
<span data-ttu-id="08bb5-142">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="08bb5-142">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="08bb5-143">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="08bb5-143">None</span></span>
- <span data-ttu-id="08bb5-144">Novamente</span><span class="sxs-lookup"><span data-stu-id="08bb5-144">Execute</span></span>
- <span data-ttu-id="08bb5-145">Gravação</span><span class="sxs-lookup"><span data-stu-id="08bb5-145">Write</span></span>
- <span data-ttu-id="08bb5-146">WriteExecute</span><span class="sxs-lookup"><span data-stu-id="08bb5-146">WriteExecute</span></span>
- <span data-ttu-id="08bb5-147">Ler</span><span class="sxs-lookup"><span data-stu-id="08bb5-147">Read</span></span>
- <span data-ttu-id="08bb5-148">ReadExecute</span><span class="sxs-lookup"><span data-stu-id="08bb5-148">ReadExecute</span></span>
- <span data-ttu-id="08bb5-149">Leitura</span><span class="sxs-lookup"><span data-stu-id="08bb5-149">ReadWrite</span></span>
- <span data-ttu-id="08bb5-150">Todo</span><span class="sxs-lookup"><span data-stu-id="08bb5-150">All</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+Permission
Parameter Sets: SetSpecificACE
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="08bb5-151">-Recurse</span><span class="sxs-lookup"><span data-stu-id="08bb5-151">-Recurse</span></span>
<span data-ttu-id="08bb5-152">Indica a ACL a ser modificada recursivamente para os arquivos e subpastas filho</span><span class="sxs-lookup"><span data-stu-id="08bb5-152">Indicates the ACL to be modified recursively to the child subdirectories and files</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="08bb5-153">-Progresso</span><span class="sxs-lookup"><span data-stu-id="08bb5-153">-ShowProgress</span></span>
<span data-ttu-id="08bb5-154">Se for passado, o status do progresso será mostrado.</span><span class="sxs-lookup"><span data-stu-id="08bb5-154">If passed then progress status is showed.</span></span> <span data-ttu-id="08bb5-155">Só se aplica quando a modificação de ACL recursiva é feita.</span><span class="sxs-lookup"><span data-stu-id="08bb5-155">Only applicable when recursive Acl modify is done.</span></span>

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

### <span data-ttu-id="08bb5-156">-Confirme</span><span class="sxs-lookup"><span data-stu-id="08bb5-156">-Confirm</span></span>
<span data-ttu-id="08bb5-157">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="08bb5-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="08bb5-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="08bb5-158">-WhatIf</span></span>
<span data-ttu-id="08bb5-159">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="08bb5-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="08bb5-160">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="08bb5-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="08bb5-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08bb5-161">CommonParameters</span></span>
<span data-ttu-id="08bb5-162">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="08bb5-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08bb5-163">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="08bb5-163">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08bb5-164">SENSORES</span><span class="sxs-lookup"><span data-stu-id="08bb5-164">INPUTS</span></span>

### <span data-ttu-id="08bb5-165">System. String</span><span class="sxs-lookup"><span data-stu-id="08bb5-165">System.String</span></span>

### <span data-ttu-id="08bb5-166">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="08bb5-166">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="08bb5-167">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStoreItemAce []</span><span class="sxs-lookup"><span data-stu-id="08bb5-167">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItemAce[]</span></span>

### <span data-ttu-id="08bb5-168">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStoreEnums + AceType</span><span class="sxs-lookup"><span data-stu-id="08bb5-168">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+AceType</span></span>

### <span data-ttu-id="08bb5-169">System. GUID</span><span class="sxs-lookup"><span data-stu-id="08bb5-169">System.Guid</span></span>

### <span data-ttu-id="08bb5-170">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStoreEnums + Permission</span><span class="sxs-lookup"><span data-stu-id="08bb5-170">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+Permission</span></span>

### <span data-ttu-id="08bb5-171">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="08bb5-171">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="08bb5-172">System. Int32</span><span class="sxs-lookup"><span data-stu-id="08bb5-172">System.Int32</span></span>

## <span data-ttu-id="08bb5-173">EXIBE</span><span class="sxs-lookup"><span data-stu-id="08bb5-173">OUTPUTS</span></span>

### <span data-ttu-id="08bb5-174">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStoreItemAce</span><span class="sxs-lookup"><span data-stu-id="08bb5-174">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItemAce</span></span>

## <span data-ttu-id="08bb5-175">INFORMA</span><span class="sxs-lookup"><span data-stu-id="08bb5-175">NOTES</span></span>

## <span data-ttu-id="08bb5-176">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="08bb5-176">RELATED LINKS</span></span>

[<span data-ttu-id="08bb5-177">Remove-AzDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="08bb5-177">Remove-AzDataLakeStoreItemAclEntry</span></span>](./Remove-AzDataLakeStoreItemAclEntry.md)


