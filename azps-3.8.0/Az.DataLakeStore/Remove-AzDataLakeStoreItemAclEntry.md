---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 33E7607E-C2BC-4F46-9038-91AC92041F00
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/remove-azdatalakestoreitemaclentry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreItemAclEntry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreItemAclEntry.md
ms.openlocfilehash: b6d07dbf390a0835bd28a045e4eea8bcf29e15f9
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93944101"
---
# <span data-ttu-id="34de6-101">Remove-AzDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="34de6-101">Remove-AzDataLakeStoreItemAclEntry</span></span>

## <span data-ttu-id="34de6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="34de6-102">SYNOPSIS</span></span>
<span data-ttu-id="34de6-103">Remove uma entrada da ACL de um arquivo ou pasta no data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="34de6-103">Removes an entry from the ACL of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="34de6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="34de6-104">SYNTAX</span></span>

### <span data-ttu-id="34de6-105">RemoveByACLObject (padrão)</span><span class="sxs-lookup"><span data-stu-id="34de6-105">RemoveByACLObject (Default)</span></span>
```
Remove-AzDataLakeStoreItemAclEntry [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-Acl] <DataLakeStoreItemAce[]> [-PassThru] [-Recurse] [-Concurrency <Int32>] [-ShowProgress]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="34de6-106">RemoveSpecificACE</span><span class="sxs-lookup"><span data-stu-id="34de6-106">RemoveSpecificACE</span></span>
```
Remove-AzDataLakeStoreItemAclEntry [-Account] <String> [-Path] <DataLakeStorePathInstance> [-AceType] <AceType>
 [[-Id] <Guid>] [-Default] [-PassThru] [-Recurse] [-Concurrency <Int32>] [-ShowProgress]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="34de6-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="34de6-107">DESCRIPTION</span></span>
<span data-ttu-id="34de6-108">O cmdlet **Remove-AzDataLakeStoreItemAclEntry** remove uma Entry (ACE) da lista de controle de acesso (ACL) de um arquivo ou pasta no data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="34de6-108">The **Remove-AzDataLakeStoreItemAclEntry** cmdlet removes an entry (ACE) from the access control list (ACL) of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="34de6-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="34de6-109">EXAMPLES</span></span>

### <span data-ttu-id="34de6-110">Exemplo 1: remover uma entrada de usuário</span><span class="sxs-lookup"><span data-stu-id="34de6-110">Example 1: Remove a user entry</span></span>
```
PS C:\>Remove-AzDataLakeStoreItemAclEntry -AccountName "ContosoADL" -Path / -AceType User -Id (Get-AzADUser -Mail "PattiFuller@contoso.com").ObjectId
```

<span data-ttu-id="34de6-111">Esse comando Remove a ACE do usuário para Patti Pereira da conta ContosoADL.</span><span class="sxs-lookup"><span data-stu-id="34de6-111">This command removes the user ACE for Patti Fuller from the ContosoADL account.</span></span>

### <span data-ttu-id="34de6-112">Exemplo 2: remover uma entrada de usuário recursivamente</span><span class="sxs-lookup"><span data-stu-id="34de6-112">Example 2: Remove a user entry recursively</span></span>
```
PS C:\>Remove-AzDataLakeStoreItemAclEntry -AccountName "ContosoADL" -Path / -AceType User -Id (Get-AzADUser -Mail "PattiFuller@contoso.com").ObjectId -Recurse -Concurrency 128
```

### <span data-ttu-id="34de6-113">Exemplo 3: remover as permissões de uma ACE recursivamente usando o objeto ACL</span><span class="sxs-lookup"><span data-stu-id="34de6-113">Example 3: Remove permissions for an ACE recursively using Acl object</span></span>
```
PS C:\>$fullAcl="user:userid1,default:user:userid1
PS C:\>$newFullAcl = $fullAcl.Split("{,}")
PS C:\>Remove-AzDataLakeStoreItemAclEntry -AccountName "ContosoADL" -Path / -Acl $newFullAcl -Recurse -Concurrency 128
```

<span data-ttu-id="34de6-114">Esse comando Remove a ACE do usuário para Patti Pereira da raiz e recursivamente de todas as suas subpastas e arquivos para a conta ContosoADL.</span><span class="sxs-lookup"><span data-stu-id="34de6-114">This command removes the user ACE for Patti Fuller from the root and recursively from all it's subdirectories and files for account ContosoADL.</span></span>

## <span data-ttu-id="34de6-115">OS</span><span class="sxs-lookup"><span data-stu-id="34de6-115">PARAMETERS</span></span>

### <span data-ttu-id="34de6-116">-Conta</span><span class="sxs-lookup"><span data-stu-id="34de6-116">-Account</span></span>
<span data-ttu-id="34de6-117">Especifica o nome da conta do data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="34de6-117">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="34de6-118">-AceType</span><span class="sxs-lookup"><span data-stu-id="34de6-118">-AceType</span></span>
<span data-ttu-id="34de6-119">Especifica o tipo de ACE a ser removida.</span><span class="sxs-lookup"><span data-stu-id="34de6-119">Specifies the type of ACE to remove.</span></span>
<span data-ttu-id="34de6-120">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="34de6-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="34de6-121">Utilizador</span><span class="sxs-lookup"><span data-stu-id="34de6-121">User</span></span>
- <span data-ttu-id="34de6-122">Grupos</span><span class="sxs-lookup"><span data-stu-id="34de6-122">Group</span></span>
- <span data-ttu-id="34de6-123">Remoção</span><span class="sxs-lookup"><span data-stu-id="34de6-123">Mask</span></span>
- <span data-ttu-id="34de6-124">Demais</span><span class="sxs-lookup"><span data-stu-id="34de6-124">Other</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+AceType
Parameter Sets: RemoveSpecificACE
Aliases:
Accepted values: User, Group, Mask, Other

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="34de6-125">-ACL</span><span class="sxs-lookup"><span data-stu-id="34de6-125">-Acl</span></span>
<span data-ttu-id="34de6-126">Especifica o objeto ACL que contém as entradas a serem removidas.</span><span class="sxs-lookup"><span data-stu-id="34de6-126">Specifies the ACL object that contains the entries to be removed.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItemAce[]
Parameter Sets: RemoveByACLObject
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="34de6-127">-Simultaneidade</span><span class="sxs-lookup"><span data-stu-id="34de6-127">-Concurrency</span></span>
<span data-ttu-id="34de6-128">Número de arquivos/diretórios processados em paralelo.</span><span class="sxs-lookup"><span data-stu-id="34de6-128">Number of files/directories processed in parallel.</span></span> <span data-ttu-id="34de6-129">Opcional: um padrão razoável será selecionado</span><span class="sxs-lookup"><span data-stu-id="34de6-129">Optional: a reasonable default will be selected</span></span>

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

### <span data-ttu-id="34de6-130">-Padrão</span><span class="sxs-lookup"><span data-stu-id="34de6-130">-Default</span></span>
<span data-ttu-id="34de6-131">Indica que essa operação Remove a ACE padrão da ACL especificada.</span><span class="sxs-lookup"><span data-stu-id="34de6-131">Indicates that this operation removes the default ACE from the specified ACL.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: RemoveSpecificACE
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="34de6-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34de6-132">-DefaultProfile</span></span>
<span data-ttu-id="34de6-133">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="34de6-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="34de6-134">-ID</span><span class="sxs-lookup"><span data-stu-id="34de6-134">-Id</span></span>
<span data-ttu-id="34de6-135">Especifica a ID de objeto do usuário, grupo ou entidade de serviço do diretório do AzureActive para o qual remover uma ACE.</span><span class="sxs-lookup"><span data-stu-id="34de6-135">Specifies the object ID of the AzureActive Directory user, group, or service principal for which to remove an ACE.</span></span>

```yaml
Type: System.Guid
Parameter Sets: RemoveSpecificACE
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="34de6-136">-PassThru</span><span class="sxs-lookup"><span data-stu-id="34de6-136">-PassThru</span></span>
<span data-ttu-id="34de6-137">Indica que uma resposta booliana deve ser retornada indicando o resultado da operação de exclusão.</span><span class="sxs-lookup"><span data-stu-id="34de6-137">Indicates a boolean response should be returned indicating the result of the delete operation.</span></span>

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

### <span data-ttu-id="34de6-138">-Caminho</span><span class="sxs-lookup"><span data-stu-id="34de6-138">-Path</span></span>
<span data-ttu-id="34de6-139">Especifica o caminho do repositório data Lake do item do qual você deseja remover uma ACE, começando com o diretório raiz (/).</span><span class="sxs-lookup"><span data-stu-id="34de6-139">Specifies the Data Lake Store path of the item from which to remove an ACE, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="34de6-140">-Recurse</span><span class="sxs-lookup"><span data-stu-id="34de6-140">-Recurse</span></span>
<span data-ttu-id="34de6-141">Indica a ACL a ser removida recursivamente para os arquivos e subpastas filho</span><span class="sxs-lookup"><span data-stu-id="34de6-141">Indicates the ACL to be removed recursively to the child subdirectories and files</span></span>

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

### <span data-ttu-id="34de6-142">-Progresso</span><span class="sxs-lookup"><span data-stu-id="34de6-142">-ShowProgress</span></span>
<span data-ttu-id="34de6-143">Se for passado, o status do progresso será mostrado.</span><span class="sxs-lookup"><span data-stu-id="34de6-143">If passed then progress status is showed.</span></span> <span data-ttu-id="34de6-144">Aplicável somente quando a remoção de ACL recursiva é concluída.</span><span class="sxs-lookup"><span data-stu-id="34de6-144">Only applicable when recursive Acl remove is done.</span></span>

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

### <span data-ttu-id="34de6-145">-Confirme</span><span class="sxs-lookup"><span data-stu-id="34de6-145">-Confirm</span></span>
<span data-ttu-id="34de6-146">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="34de6-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="34de6-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="34de6-147">-WhatIf</span></span>
<span data-ttu-id="34de6-148">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="34de6-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="34de6-149">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="34de6-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="34de6-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34de6-150">CommonParameters</span></span>
<span data-ttu-id="34de6-151">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="34de6-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34de6-152">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="34de6-152">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34de6-153">SENSORES</span><span class="sxs-lookup"><span data-stu-id="34de6-153">INPUTS</span></span>

### <span data-ttu-id="34de6-154">System. String</span><span class="sxs-lookup"><span data-stu-id="34de6-154">System.String</span></span>

### <span data-ttu-id="34de6-155">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="34de6-155">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="34de6-156">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStoreItemAce []</span><span class="sxs-lookup"><span data-stu-id="34de6-156">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItemAce[]</span></span>

### <span data-ttu-id="34de6-157">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStoreEnums + AceType</span><span class="sxs-lookup"><span data-stu-id="34de6-157">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+AceType</span></span>

### <span data-ttu-id="34de6-158">System. GUID</span><span class="sxs-lookup"><span data-stu-id="34de6-158">System.Guid</span></span>

### <span data-ttu-id="34de6-159">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="34de6-159">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="34de6-160">System. Int32</span><span class="sxs-lookup"><span data-stu-id="34de6-160">System.Int32</span></span>

## <span data-ttu-id="34de6-161">EXIBE</span><span class="sxs-lookup"><span data-stu-id="34de6-161">OUTPUTS</span></span>

### <span data-ttu-id="34de6-162">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="34de6-162">System.Boolean</span></span>

## <span data-ttu-id="34de6-163">INFORMA</span><span class="sxs-lookup"><span data-stu-id="34de6-163">NOTES</span></span>

## <span data-ttu-id="34de6-164">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="34de6-164">RELATED LINKS</span></span>

[<span data-ttu-id="34de6-165">Set-AzDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="34de6-165">Set-AzDataLakeStoreItemAclEntry</span></span>](./Set-AzDataLakeStoreItemAclEntry.md)


