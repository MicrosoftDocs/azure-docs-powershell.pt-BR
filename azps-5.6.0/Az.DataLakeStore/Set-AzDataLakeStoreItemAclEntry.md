---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 0671D833-8B3A-4480-A576-92F1A9E8CE92
online version: https://docs.microsoft.com/powershell/module/az.datalakestore/set-azdatalakestoreitemaclentry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreItemAclEntry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreItemAclEntry.md
ms.openlocfilehash: 2577f61476fd5026d75b677e35b994d64f4954e7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101885908"
---
# <span data-ttu-id="e495f-101">Set-AzDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="e495f-101">Set-AzDataLakeStoreItemAclEntry</span></span>

## <span data-ttu-id="e495f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e495f-102">SYNOPSIS</span></span>
<span data-ttu-id="e495f-103">Modifica uma entrada na ACL de um arquivo ou pasta no Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="e495f-103">Modifies an entry in the ACL of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="e495f-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="e495f-104">SYNTAX</span></span>

### <span data-ttu-id="e495f-105">SetByACLObject (Padrão)</span><span class="sxs-lookup"><span data-stu-id="e495f-105">SetByACLObject (Default)</span></span>
```
Set-AzDataLakeStoreItemAclEntry [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-Acl] <DataLakeStoreItemAce[]> [-PassThru] [-Recurse] [-Concurrency <Int32>] [-ShowProgress]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e495f-106">SetSpecificACE</span><span class="sxs-lookup"><span data-stu-id="e495f-106">SetSpecificACE</span></span>
```
Set-AzDataLakeStoreItemAclEntry [-Account] <String> [-Path] <DataLakeStorePathInstance> [-AceType] <AceType>
 [[-Id] <Guid>] [-Permissions] <Permission> [-Default] [-PassThru] [-Recurse] [-Concurrency <Int32>]
 [-ShowProgress] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e495f-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="e495f-107">DESCRIPTION</span></span>
<span data-ttu-id="e495f-108">O cmdlet **Set-AzDataLakeStoreItemAclEntry** modifica uma entrada (ACE) na lista de controles de acesso (ACL) de um arquivo ou pasta no Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="e495f-108">The **Set-AzDataLakeStoreItemAclEntry** cmdlet modifies an entry (ACE) in the access control list (ACL) of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="e495f-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e495f-109">EXAMPLES</span></span>

### <span data-ttu-id="e495f-110">Exemplo 1: Modificar permissões para um ACE</span><span class="sxs-lookup"><span data-stu-id="e495f-110">Example 1: Modify permissions for an ACE</span></span>
```
PS C:\>Set-AzDataLakeStoreItemAclEntry -AccountName "ContosoADL" -Path / -AceType User -Id (Get-AzADUser -Mail "PattiFuller@contoso.com").ObjectId -Permissions All
```

<span data-ttu-id="e495f-111">Este comando modifica o ACE para Patti Fuller ter todas as permissões.</span><span class="sxs-lookup"><span data-stu-id="e495f-111">This command modifies the ACE for Patti Fuller to have all permissions.</span></span>

### <span data-ttu-id="e495f-112">Exemplo 2: Modificar permissões para um ACE recursivamente</span><span class="sxs-lookup"><span data-stu-id="e495f-112">Example 2: Modify permissions for an ACE recursively</span></span>
```
PS C:\>Set-AzDataLakeStoreItemAclEntry -AccountName "ContosoADL" -Path / -AceType User -Id (Get-AzADUser -Mail "PattiFuller@contoso.com").ObjectId -Permissions All -Recurse -Concurrency 128
```

### <span data-ttu-id="e495f-113">Exemplo 3: Modificar permissões para um objeto ACE recursivamente usando o objeto Acl</span><span class="sxs-lookup"><span data-stu-id="e495f-113">Example 3: Modify permissions for an ACE recursively using Acl object</span></span>
```
PS C:\>$fullAcl="user:userid1:--x,default:user:userid1:--x"
PS C:\>$newFullAcl = $fullAcl.Split("{,}")
PS C:\>Set-AzDataLakeStoreItemAclEntry -AccountName "ContosoADL" -Path / -Acl $newFullAcl -Recurse -Concurrency 128
```

<span data-ttu-id="e495f-114">Esse comando modifica recursivamente o ACE para Patti Fuller ter todas as permissões para raiz e todos os subdiretivos e arquivos.</span><span class="sxs-lookup"><span data-stu-id="e495f-114">This command recursively modifies the ACE for Patti Fuller to have all permissions to root and all its subdirectories and files.</span></span>

## <span data-ttu-id="e495f-115">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="e495f-115">PARAMETERS</span></span>

### <span data-ttu-id="e495f-116">-Account</span><span class="sxs-lookup"><span data-stu-id="e495f-116">-Account</span></span>
<span data-ttu-id="e495f-117">Especifica o nome da conta do Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="e495f-117">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="e495f-118">-AceType</span><span class="sxs-lookup"><span data-stu-id="e495f-118">-AceType</span></span>
<span data-ttu-id="e495f-119">Especifica o tipo de ACE a ser modificado.</span><span class="sxs-lookup"><span data-stu-id="e495f-119">Specifies the type of ACE to modify.</span></span>
<span data-ttu-id="e495f-120">Os valores aceitáveis para este parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="e495f-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="e495f-121">Usuário</span><span class="sxs-lookup"><span data-stu-id="e495f-121">User</span></span> 
- <span data-ttu-id="e495f-122">Grupo</span><span class="sxs-lookup"><span data-stu-id="e495f-122">Group</span></span> 
- <span data-ttu-id="e495f-123">Máscara</span><span class="sxs-lookup"><span data-stu-id="e495f-123">Mask</span></span> 
- <span data-ttu-id="e495f-124">Outros</span><span class="sxs-lookup"><span data-stu-id="e495f-124">Other</span></span>

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

### <span data-ttu-id="e495f-125">-Acl</span><span class="sxs-lookup"><span data-stu-id="e495f-125">-Acl</span></span>
<span data-ttu-id="e495f-126">Especifica o objeto ACL que contém as entradas a modificar.</span><span class="sxs-lookup"><span data-stu-id="e495f-126">Specifies the ACL object that contains the entries to modify.</span></span>

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

### <span data-ttu-id="e495f-127">-Concurrency</span><span class="sxs-lookup"><span data-stu-id="e495f-127">-Concurrency</span></span>
<span data-ttu-id="e495f-128">Número de arquivos/diretórios processados em paralelo.</span><span class="sxs-lookup"><span data-stu-id="e495f-128">Number of files/directories processed in parallel.</span></span> <span data-ttu-id="e495f-129">Opcional: um padrão razoável será selecionado</span><span class="sxs-lookup"><span data-stu-id="e495f-129">Optional: a reasonable default will be selected</span></span>

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

### <span data-ttu-id="e495f-130">-Default</span><span class="sxs-lookup"><span data-stu-id="e495f-130">-Default</span></span>
<span data-ttu-id="e495f-131">Indica que essa operação modifica o ACE padrão da ACL especificada.</span><span class="sxs-lookup"><span data-stu-id="e495f-131">Indicates that this operation modifies the default ACE from the specified ACL.</span></span>

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

### <span data-ttu-id="e495f-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e495f-132">-DefaultProfile</span></span>
<span data-ttu-id="e495f-133">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="e495f-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e495f-134">-Id</span><span class="sxs-lookup"><span data-stu-id="e495f-134">-Id</span></span>
<span data-ttu-id="e495f-135">Especifica a ID do objeto do usuário, grupo ou entidade de serviço do AzureActive Directory para o qual modificar um ACE.</span><span class="sxs-lookup"><span data-stu-id="e495f-135">Specifies the object ID of the AzureActive Directory user, group, or service principal for which to modify an ACE.</span></span>

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

### <span data-ttu-id="e495f-136">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e495f-136">-PassThru</span></span>
<span data-ttu-id="e495f-137">Indica que a ACL resultante deve ser retornada.</span><span class="sxs-lookup"><span data-stu-id="e495f-137">Indicates the resulting ACL should be returned.</span></span>

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

### <span data-ttu-id="e495f-138">-Path</span><span class="sxs-lookup"><span data-stu-id="e495f-138">-Path</span></span>
<span data-ttu-id="e495f-139">Especifica o caminho do Data Lake Store do item para o qual modificar um ACE, começando com o diretório raiz (/).</span><span class="sxs-lookup"><span data-stu-id="e495f-139">Specifies the Data Lake Store path of the item for which to modify an ACE, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="e495f-140">-Permissões</span><span class="sxs-lookup"><span data-stu-id="e495f-140">-Permissions</span></span>
<span data-ttu-id="e495f-141">Especifica as permissões para o ACE.</span><span class="sxs-lookup"><span data-stu-id="e495f-141">Specifies the permissions for the ACE.</span></span>
<span data-ttu-id="e495f-142">Os valores aceitáveis para este parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="e495f-142">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="e495f-143">Nenhum</span><span class="sxs-lookup"><span data-stu-id="e495f-143">None</span></span>
- <span data-ttu-id="e495f-144">Executar</span><span class="sxs-lookup"><span data-stu-id="e495f-144">Execute</span></span>
- <span data-ttu-id="e495f-145">Gravar</span><span class="sxs-lookup"><span data-stu-id="e495f-145">Write</span></span>
- <span data-ttu-id="e495f-146">WriteExecute</span><span class="sxs-lookup"><span data-stu-id="e495f-146">WriteExecute</span></span>
- <span data-ttu-id="e495f-147">Leitura</span><span class="sxs-lookup"><span data-stu-id="e495f-147">Read</span></span>
- <span data-ttu-id="e495f-148">ReadExecute</span><span class="sxs-lookup"><span data-stu-id="e495f-148">ReadExecute</span></span>
- <span data-ttu-id="e495f-149">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="e495f-149">ReadWrite</span></span>
- <span data-ttu-id="e495f-150">All</span><span class="sxs-lookup"><span data-stu-id="e495f-150">All</span></span>

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

### <span data-ttu-id="e495f-151">-Recurse</span><span class="sxs-lookup"><span data-stu-id="e495f-151">-Recurse</span></span>
<span data-ttu-id="e495f-152">Indica a ACL a ser modificada recursivamente para os subdiretivos e arquivos filho</span><span class="sxs-lookup"><span data-stu-id="e495f-152">Indicates the ACL to be modified recursively to the child subdirectories and files</span></span>

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

### <span data-ttu-id="e495f-153">-ShowProgress</span><span class="sxs-lookup"><span data-stu-id="e495f-153">-ShowProgress</span></span>
<span data-ttu-id="e495f-154">Se aprovado, o status de progresso será mostrado.</span><span class="sxs-lookup"><span data-stu-id="e495f-154">If passed then progress status is showed.</span></span> <span data-ttu-id="e495f-155">Aplicável somente quando a modificação recursiva do Acl é feita.</span><span class="sxs-lookup"><span data-stu-id="e495f-155">Only applicable when recursive Acl modify is done.</span></span>

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

### <span data-ttu-id="e495f-156">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e495f-156">-Confirm</span></span>
<span data-ttu-id="e495f-157">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e495f-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e495f-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e495f-158">-WhatIf</span></span>
<span data-ttu-id="e495f-159">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e495f-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e495f-160">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e495f-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e495f-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e495f-161">CommonParameters</span></span>
<span data-ttu-id="e495f-162">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e495f-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e495f-163">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e495f-163">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e495f-164">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e495f-164">INPUTS</span></span>

### <span data-ttu-id="e495f-165">System.String</span><span class="sxs-lookup"><span data-stu-id="e495f-165">System.String</span></span>

### <span data-ttu-id="e495f-166">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="e495f-166">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="e495f-167">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItemAce[]</span><span class="sxs-lookup"><span data-stu-id="e495f-167">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItemAce[]</span></span>

### <span data-ttu-id="e495f-168">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+AceType</span><span class="sxs-lookup"><span data-stu-id="e495f-168">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+AceType</span></span>

### <span data-ttu-id="e495f-169">System.Guid</span><span class="sxs-lookup"><span data-stu-id="e495f-169">System.Guid</span></span>

### <span data-ttu-id="e495f-170">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+Permission</span><span class="sxs-lookup"><span data-stu-id="e495f-170">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+Permission</span></span>

### <span data-ttu-id="e495f-171">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="e495f-171">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="e495f-172">System.Int32</span><span class="sxs-lookup"><span data-stu-id="e495f-172">System.Int32</span></span>

## <span data-ttu-id="e495f-173">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="e495f-173">OUTPUTS</span></span>

### <span data-ttu-id="e495f-174">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItemAce</span><span class="sxs-lookup"><span data-stu-id="e495f-174">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItemAce</span></span>

## <span data-ttu-id="e495f-175">NOTES</span><span class="sxs-lookup"><span data-stu-id="e495f-175">NOTES</span></span>

## <span data-ttu-id="e495f-176">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e495f-176">RELATED LINKS</span></span>

[<span data-ttu-id="e495f-177">Remove-AzDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="e495f-177">Remove-AzDataLakeStoreItemAclEntry</span></span>](./Remove-AzDataLakeStoreItemAclEntry.md)


