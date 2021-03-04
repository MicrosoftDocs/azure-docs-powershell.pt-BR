---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/remove-azdatalakegen2aclrecursive
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzDataLakeGen2AclRecursive.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzDataLakeGen2AclRecursive.md
ms.openlocfilehash: db999e2cf473fc62a2c8463e8e08ab8c46bc6ac1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887657"
---
# <span data-ttu-id="ef324-101">Remove-AzDataLakeGen2AclRecursive</span><span class="sxs-lookup"><span data-stu-id="ef324-101">Remove-AzDataLakeGen2AclRecursive</span></span>

## <span data-ttu-id="ef324-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ef324-102">SYNOPSIS</span></span>
<span data-ttu-id="ef324-103">Remova a ACL recursivamente no caminho especificado.</span><span class="sxs-lookup"><span data-stu-id="ef324-103">Remove ACL recursively on the specified path.</span></span> 

## <span data-ttu-id="ef324-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="ef324-104">SYNTAX</span></span>

```
Remove-AzDataLakeGen2AclRecursive [-FileSystem] <String> [[-Path] <String>] [-ContinuationToken <String>]
 -Acl <PSPathAccessControlEntry[]> [-ContinueOnFailure] [-BatchSize <Int32>] [-MaxBatchCount <Int32>] [-AsJob]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ef324-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="ef324-105">DESCRIPTION</span></span>
<span data-ttu-id="ef324-106">O cmdlet **Remove-AzDataLakeGen2AclRecursive** remove a ACL recursivamente no caminho especificado.</span><span class="sxs-lookup"><span data-stu-id="ef324-106">The **Remove-AzDataLakeGen2AclRecursive** cmdlet removes ACL recursively on the specified path.</span></span> <span data-ttu-id="ef324-107">As entradas ACL no ACL original, que tem o mesmo AccessControlType, DefaultScope e EntityId com entradas ACL de entrada (mesmo com permissão diferente) serão removidas.</span><span class="sxs-lookup"><span data-stu-id="ef324-107">The ACL entries in original ACL, which has same AccessControlType, DefaultScope and EntityId with input ACL entries (even with different permission) wil lbe removed.</span></span>

## <span data-ttu-id="ef324-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ef324-108">EXAMPLES</span></span>

### <span data-ttu-id="ef324-109">Exemplo 1: Remover recursivamente a ACL em uma directiria raiz do sistema de arquivos</span><span class="sxs-lookup"><span data-stu-id="ef324-109">Example 1: Remove ACL recursively on a root directiry of filesystem</span></span>
```
PS C:\>$acl = Set-AzDataLakeGen2ItemAclObject -AccessControlType user -EntityId $id -Permission r-x -DefaultScope
PS C:\>$acl = Set-AzDataLakeGen2ItemAclObject -AccessControlType user -EntityId $id -Permission r-x -InputObject $acl
PS C:\> Remove-AzDataLakeGen2AclRecursive -FileSystem "filesystem1" -Acl $acl -Context $ctx
WARNING: To find the ACL Entry to remove, will only compare AccessControlType, DefaultScope and EntityId, will omit Permission.

FailedEntries                   : 
TotalDirectoriesSuccessfulCount : 7
TotalFilesSuccessfulCount       : 5
TotalFailureCount               : 0
ContinuationToken               :
```

<span data-ttu-id="ef324-110">Este comando primeiro cria um objeto ACL com 2 entradas de acl e remove recursivamente a ACL em um diretório raiz de um sistema de arquivos.</span><span class="sxs-lookup"><span data-stu-id="ef324-110">This command first creates an ACL object with 2 acl entries, then removes ACL recursively on a root directory of a file system.</span></span>

### <span data-ttu-id="ef324-111">Exemplo 2: Remover recursivamente a ACL em um diretório</span><span class="sxs-lookup"><span data-stu-id="ef324-111">Example 2: Remove ACL recursively on a directory</span></span>
```
PS C:\> $result = Remove-AzDataLakeGen2AclRecursive -FileSystem "filesystem1" -Path "dir1" -Acl $acl  -Context $ctx
WARNING: To find the ACL Entry to remove, will only compare AccessControlType, DefaultScope and EntityId, will omit Permission.

PS C:\> $result

FailedEntries                   : {dir1/dir2/file4}
TotalDirectoriesSuccessfulCount : 500
TotalFilesSuccessfulCount       : 2500
TotalFailureCount               : 1
ContinuationToken               : VBaHi5TfyO2ai1wYTRhIL2FjbGNibjA2c3RmATAxRDVEN0UzRENFQzZCRTAvYWRsc3Rlc3QyATAxRDY2M0ZCQTZBN0JGQTkvZGlyMC9kaXIxL2ZpbGUzFgAAAA==

PS C:\> $result.FailedEntries

Name            IsDirectory ErrorMessage                                                                   
----            ----------- ------------                                                                   
dir0/dir2/file4       False This request is not authorized to perform this operation using this permission.

# user need fix the failed item , then can resume with ContinuationToken

PS C:\> $result = Remove-AzDataLakeGen2AclRecursive -FileSystem "filesystem1" -Path "dir1" -Acl $acl -ContinuationToken $result.ContinuationToken -Context $ctx
WARNING: To find the ACL Entry to remove, will only compare AccessControlType, DefaultScope and EntityId, will omit Permission.

PS C:\> $result

FailedEntries                   : 
TotalDirectoriesSuccessfulCount : 100
TotalFilesSuccessfulCount       : 1000
TotalFailureCount               : 0
ContinuationToken               :
```

<span data-ttu-id="ef324-112">Este comando primeiro remove a ACL recursivamente em um diretório e falha e, em seguida, retoma com ContinuationToken após o usuário corrigir o arquivo com falha.</span><span class="sxs-lookup"><span data-stu-id="ef324-112">This command first removes ACL recursively on a directory and failed, then resume with ContinuationToken after user fix the failed file.</span></span>

### <span data-ttu-id="ef324-113">Exemplo 3: Remover parte recursiva de ACL por parte</span><span class="sxs-lookup"><span data-stu-id="ef324-113">Example 3: Remove ACL recursively chunk by chunk</span></span>
```
$token = $null
$TotalDirectoriesSuccess = 0
$TotalFilesSuccess = 0
$totalFailure = 0
$FailedEntries = New-Object System.Collections.Generic.List[System.Object]
do
{
    $result = Remove-AzDataLakeGen2AclRecursive -FileSystem "filesystem1" -Path "dir1" -Acl $acl  -BatchSize 1000 -MaxBatchCount 50 -ContinuationToken $token -Context $ctx

    # echo $result
    $TotalFilesSuccess += $result.TotalFilesSuccessfulCount
    $TotalDirectoriesSuccess += $result.TotalDirectoriesSuccessfulCount
    $totalFailure += $result.TotalFailureCount
    $FailedEntries += $result.FailedEntries
    $token = $result.ContinuationToken
}while (($token -ne $null) -and ($result.TotalFailureCount -eq 0))
echo ""
echo "[Result Summary]"
echo "TotalDirectoriesSuccessfulCount: `t$($TotalDirectoriesSuccess)"
echo "TotalFilesSuccessfulCount: `t`t`t$($TotalFilesSuccess)"
echo "TotalFailureCount: `t`t`t`t`t$($totalFailure)"
echo "ContinuationToken: `t`t`t`t`t$($token)"
echo "FailedEntries:"$($FailedEntries | ft)
```

<span data-ttu-id="ef324-114">Este script removerá a ACL rescursivamente em parte de diretório por parte, com tamanho de parte como BatchSize \* MaxBatchCount.</span><span class="sxs-lookup"><span data-stu-id="ef324-114">This script will remove ACL rescursively on directory chunk by chunk, with chunk size as BatchSize \* MaxBatchCount.</span></span> <span data-ttu-id="ef324-115">O tamanho da parte é 50000 neste script.</span><span class="sxs-lookup"><span data-stu-id="ef324-115">Chunk size is 50000 in this script.</span></span>

### <span data-ttu-id="ef324-116">Exemplo 4: Remover recursivamente a ACL em um diretório e ContinuarOnFailure e, em seguida, retomar de falhas uma a uma</span><span class="sxs-lookup"><span data-stu-id="ef324-116">Example 4: Remove ACL recursively on a directory and ContinueOnFailure, then resume from failures one by one</span></span>
```
PS C:\> $result = Remove-AzDataLakeGen2AclRecursive -FileSystem "filesystem1" -Path "dir1" -Acl $acl -ContinueOnFailure -Context $ctx

PS C:\> $result

FailedEntries                   : {dir0/dir1/file1, dir0/dir2/file4}
TotalDirectoriesSuccessfulCount : 100
TotalFilesSuccessfulCount       : 500
TotalFailureCount               : 2
ContinuationToken               : VBaHi5TfyO2ai1wYTRhIL2FjbGNibjA2c3RmATAxRDVEN0UzRENFQzZCRTAvYWRsc3Rlc3QyATAxRDY2M0ZCQTZBN0JGQTkvZGlyMC9kaXIxL2ZpbGUzFgAAAA==

PS C:\> $result.FailedEntries

Name            IsDirectory ErrorMessage                                                                   
----            ----------- ------------                                                                   
dir0/dir1/file1       False This request is not authorized to perform this operation using this permission.
dir0/dir2/file4       False This request is not authorized to perform this operation using this permission.

# user need fix the failed item , then can resume with ContinuationToken

PS C:\> foreach ($path in $result.FailedEntries.Name)
        {
            # user code to fix failed entry in $path
            
            #set ACL again
            Remove-AzDataLakeGen2AclRecursive -FileSystem "filesystem1" -Path $path -Acl $acl -Context $ctx
        }
```

<span data-ttu-id="ef324-117">Este comando primeiro remove a ACL recursivamente para um diretório com ContinueOnFailure e alguns itens falharam e, em seguida, retoma os itens com falha um por um.</span><span class="sxs-lookup"><span data-stu-id="ef324-117">This command first removes ACL recursively to a directory with ContinueOnFailure, and some items failed, then resume the failed items one by one.</span></span>

## <span data-ttu-id="ef324-118">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="ef324-118">PARAMETERS</span></span>

### <span data-ttu-id="ef324-119">-Acl</span><span class="sxs-lookup"><span data-stu-id="ef324-119">-Acl</span></span>
<span data-ttu-id="ef324-120">A lista de controles de acesso POSIX para definir recursivamente para o arquivo ou diretório.</span><span class="sxs-lookup"><span data-stu-id="ef324-120">The POSIX access control list to set recursively for the file or directory.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSPathAccessControlEntry[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef324-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ef324-121">-AsJob</span></span>
<span data-ttu-id="ef324-122">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="ef324-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ef324-123">-BatchSize</span><span class="sxs-lookup"><span data-stu-id="ef324-123">-BatchSize</span></span>
<span data-ttu-id="ef324-124">Se o tamanho do conjunto de dados exceder o tamanho do lote, a operação será dividida em várias solicitações para que o progresso possa ser rastreado.</span><span class="sxs-lookup"><span data-stu-id="ef324-124">If data set size exceeds batch size then operation will be split into multiple requests so that progress can be tracked.</span></span>
<span data-ttu-id="ef324-125">O tamanho do lote deve estar entre 1 e 2000.</span><span class="sxs-lookup"><span data-stu-id="ef324-125">Batch size should be between 1 and 2000.</span></span>
<span data-ttu-id="ef324-126">O padrão é 2000.</span><span class="sxs-lookup"><span data-stu-id="ef324-126">Default is 2000.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef324-127">-Context</span><span class="sxs-lookup"><span data-stu-id="ef324-127">-Context</span></span>
<span data-ttu-id="ef324-128">Objeto de contexto de armazenamento do Azure</span><span class="sxs-lookup"><span data-stu-id="ef324-128">Azure Storage Context Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ef324-129">-ContinuationToken</span><span class="sxs-lookup"><span data-stu-id="ef324-129">-ContinuationToken</span></span>
<span data-ttu-id="ef324-130">Token de Continuação.</span><span class="sxs-lookup"><span data-stu-id="ef324-130">Continuation Token.</span></span>

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

### <span data-ttu-id="ef324-131">-ContinueOnFailure</span><span class="sxs-lookup"><span data-stu-id="ef324-131">-ContinueOnFailure</span></span>
<span data-ttu-id="ef324-132">De definir esse parâmetro para ignorar falhas e continuar a proceeing com a operação em outras sub-entidades do diretório.</span><span class="sxs-lookup"><span data-stu-id="ef324-132">Set this parameter to ignore failures and continue proceeing with the operation on other sub-entities of the directory.</span></span> <span data-ttu-id="ef324-133">Por padrão, a operação terminará rapidamente ao encontrar falhas.</span><span class="sxs-lookup"><span data-stu-id="ef324-133">Default the operation will terminate quickly on encountering failures.</span></span>

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

### <span data-ttu-id="ef324-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef324-134">-DefaultProfile</span></span>
<span data-ttu-id="ef324-135">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ef324-135">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef324-136">-FileSystem</span><span class="sxs-lookup"><span data-stu-id="ef324-136">-FileSystem</span></span>
<span data-ttu-id="ef324-137">Nome do FileSystem</span><span class="sxs-lookup"><span data-stu-id="ef324-137">FileSystem name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ef324-138">-MaxBatchCount</span><span class="sxs-lookup"><span data-stu-id="ef324-138">-MaxBatchCount</span></span>
<span data-ttu-id="ef324-139">Número máximo de lotes que a operação de Controle de Acesso de alteração única pode ser executada.</span><span class="sxs-lookup"><span data-stu-id="ef324-139">Maximum number of batches that single change Access Control operation can execute.</span></span> <span data-ttu-id="ef324-140">Se o tamanho do conjunto de dados exceder MaxBatchCount multiplique BatchSize, o token de continuação será retornado.</span><span class="sxs-lookup"><span data-stu-id="ef324-140">If data set size exceeds MaxBatchCount multiply BatchSize, continuation token will be return.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef324-141">-Path</span><span class="sxs-lookup"><span data-stu-id="ef324-141">-Path</span></span>
<span data-ttu-id="ef324-142">O caminho no FileSystem especificado que para alterar a Acl recursivamente.</span><span class="sxs-lookup"><span data-stu-id="ef324-142">The path in the specified FileSystem that to change Acl recursively.</span></span>
<span data-ttu-id="ef324-143">Pode ser um arquivo ou diretório.</span><span class="sxs-lookup"><span data-stu-id="ef324-143">Can be a file or directory.</span></span>
<span data-ttu-id="ef324-144">No formato 'directory/file.txt' ou 'directory1/directory2/'.</span><span class="sxs-lookup"><span data-stu-id="ef324-144">In the format 'directory/file.txt' or 'directory1/directory2/'.</span></span>
<span data-ttu-id="ef324-145">Ignore definir esse parâmetro para alterar recursivamente a Acl do diretório raiz do Sistema de Arquivos.</span><span class="sxs-lookup"><span data-stu-id="ef324-145">Skip set this parameter to change Acl recursively from root directory of the Filesystem.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ef324-146">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ef324-146">-Confirm</span></span>
<span data-ttu-id="ef324-147">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ef324-147">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef324-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ef324-148">-WhatIf</span></span>
<span data-ttu-id="ef324-149">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="ef324-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ef324-150">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ef324-150">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef324-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef324-151">CommonParameters</span></span>
<span data-ttu-id="ef324-152">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ef324-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef324-153">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ef324-153">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef324-154">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ef324-154">INPUTS</span></span>

### <span data-ttu-id="ef324-155">System.String</span><span class="sxs-lookup"><span data-stu-id="ef324-155">System.String</span></span>

### <span data-ttu-id="ef324-156">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="ef324-156">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="ef324-157">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="ef324-157">OUTPUTS</span></span>

### <span data-ttu-id="ef324-158">System.String</span><span class="sxs-lookup"><span data-stu-id="ef324-158">System.String</span></span>

## <span data-ttu-id="ef324-159">NOTES</span><span class="sxs-lookup"><span data-stu-id="ef324-159">NOTES</span></span>

## <span data-ttu-id="ef324-160">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ef324-160">RELATED LINKS</span></span>
