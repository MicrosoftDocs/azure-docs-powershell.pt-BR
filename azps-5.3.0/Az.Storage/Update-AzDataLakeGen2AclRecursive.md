---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/update-azdatalakegen2aclrecursive
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzDataLakeGen2AclRecursive.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzDataLakeGen2AclRecursive.md
ms.openlocfilehash: 80b1816dff686db7e84bf876fd74f9642389b42f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98271291"
---
# <span data-ttu-id="25cf9-101">Update-AzDataLakeGen2AclRecursive</span><span class="sxs-lookup"><span data-stu-id="25cf9-101">Update-AzDataLakeGen2AclRecursive</span></span>

## <span data-ttu-id="25cf9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="25cf9-102">SYNOPSIS</span></span>
<span data-ttu-id="25cf9-103">Atualize a ACL recursivamente no caminho especificado.</span><span class="sxs-lookup"><span data-stu-id="25cf9-103">Update ACL recursively on the specified path.</span></span> 

## <span data-ttu-id="25cf9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="25cf9-104">SYNTAX</span></span>

```
Update-AzDataLakeGen2AclRecursive [-FileSystem] <String> [[-Path] <String>] [-ContinuationToken <String>]
 -Acl <PSPathAccessControlEntry[]> [-ContinueOnFailure] [-BatchSize <Int32>] [-MaxBatchCount <Int32>] [-AsJob]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="25cf9-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="25cf9-105">DESCRIPTION</span></span>
<span data-ttu-id="25cf9-106">O cmdlet **Update-AzDataLakeGen2AclRecursive** atualiza a ACL recursivamente no caminho especificado.</span><span class="sxs-lookup"><span data-stu-id="25cf9-106">The **Update-AzDataLakeGen2AclRecursive** cmdlet updates ACL recursively on the specified path.</span></span> <span data-ttu-id="25cf9-107">A ACL de entrada mesclará a ACL original: se a entrada ACL com o mesmo AccessControlType/EntityId/DefaultScope existir, a permissão atualizar; Adicione uma nova entrada de ACL.</span><span class="sxs-lookup"><span data-stu-id="25cf9-107">The input ACL will merge the the original ACL: If ACL entry with same AccessControlType/EntityId/DefaultScope exist, update permission; else add a new ACL entry.</span></span>

## <span data-ttu-id="25cf9-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="25cf9-108">EXAMPLES</span></span>

### <span data-ttu-id="25cf9-109">Exemplo 1: atualizar a ACL recursivamente em um directiry de raiz do sistema de arquivos</span><span class="sxs-lookup"><span data-stu-id="25cf9-109">Example 1: Update ACL recursively on a root directiry of filesystem</span></span>
```
PS C:\>$acl = New-AzDataLakeGen2ItemAclObject -AccessControlType user -Permission rwx 
PS C:\>$acl = New-AzDataLakeGen2ItemAclObject -AccessControlType group -Permission rw- -InputObject $acl 
PS C:\>$acl = New-AzDataLakeGen2ItemAclObject -AccessControlType other -Permission "rw-" -InputObject $acl
PS C:\> Update-AzDataLakeGen2AclRecursive -FileSystem "filesystem1" -Acl $acl -Context $ctx

FailedEntries                   : 
TotalDirectoriesSuccessfulCount : 7
TotalFilesSuccessfulCount       : 5
TotalFailureCount               : 0
ContinuationToken               :
```

<span data-ttu-id="25cf9-110">Esse comando primeiro cria um objeto ACL com 3 entradas ACL e, em seguida, atualiza a ACL recursivamente em um diretório raiz de um sistema de arquivos.</span><span class="sxs-lookup"><span data-stu-id="25cf9-110">This command first creates an ACL object with 3 acl entries, then updates ACL recursively on a root directory of a file system.</span></span>

### <span data-ttu-id="25cf9-111">Exemplo 2: Atualize a ACL recursivamente em um diretório e retome da falha com ContinuationToken</span><span class="sxs-lookup"><span data-stu-id="25cf9-111">Example 2: Update ACL recursively on a directory, and resume from failure with ContinuationToken</span></span>
```
PS C:\> $result = Update-AzDataLakeGen2AclRecursive -FileSystem "filesystem1" -Path "dir1" -Acl $acl  -Context $ctx

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

PS C:\> $result = Update-AzDataLakeGen2AclRecursive -FileSystem "filesystem1" -Path "dir1" -Acl $acl -ContinuationToken $result.ContinuationToken -Context $ctx

PS C:\> $result

FailedEntries                   : 
TotalDirectoriesSuccessfulCount : 100
TotalFilesSuccessfulCount       : 1000
TotalFailureCount               : 0
ContinuationToken               :
```

<span data-ttu-id="25cf9-112">Esse comando atualiza a ACL recursivamente para um diretório e falhou, depois retome com ContinuationToken após corrigir o arquivo com falha.</span><span class="sxs-lookup"><span data-stu-id="25cf9-112">This command first updateds ACL recursively to a directory and failed, then resume with ContinuationToken after user fix the failed file.</span></span>

### <span data-ttu-id="25cf9-113">Exemplo 3: atualizar a ACL recursivamente o bloco por parte</span><span class="sxs-lookup"><span data-stu-id="25cf9-113">Example 3: Update ACL recursively chunk by chunk</span></span>
```
$ContinueOnFailure = $true # Set it to $false if want to terminate the operation quickly on encountering failures
$token = $null
$TotalDirectoriesSuccess = 0
$TotalFilesSuccess = 0
$totalFailure = 0
$FailedEntries = New-Object System.Collections.Generic.List[System.Object]
do
{
    
    if ($ContinueOnFailure)
    {
        $result = Update-AzDataLakeGen2AclRecursive -FileSystem "filesystem1" -Path "dir1" -Acl $acl  -BatchSize 100 -MaxBatchCount 50 -ContinuationToken $token -Context $ctx -ContinueOnFailure
    }
    else
    {
        $result = Update-AzDataLakeGen2AclRecursive -FileSystem "filesystem1" -Path "dir1" -Acl $acl  -BatchSize 100 -MaxBatchCount 50 -ContinuationToken $token -Context $ctx
    }

    # echo $result
    $TotalFilesSuccess += $result.TotalFilesSuccessfulCount
    $TotalDirectoriesSuccess += $result.TotalDirectoriesSuccessfulCount
    $totalFailure += $result.TotalFailureCount
    $FailedEntries += $result.FailedEntries
    $token = $result.ContinuationToken
}while (($token -ne $null) -and (($ContinueOnFailure) -or ($result.TotalFailureCount -eq 0)))
echo ""
echo "[Result Summary]"
echo "TotalDirectoriesSuccessfulCount: `t$($TotalDirectoriesSuccess)"
echo "TotalFilesSuccessfulCount: `t`t`t$($TotalFilesSuccess)"
echo "TotalFailureCount: `t`t`t`t`t$($totalFailure)"
echo "ContinuationToken: `t`t`t`t`t$($token)"
echo "FailedEntries:"$($FailedEntries | ft)
```

<span data-ttu-id="25cf9-114">Esse script atualizará a ACL rescursively na parte do diretório por parte, com tamanho da parte como BatchSize \* MaxBatchCount.</span><span class="sxs-lookup"><span data-stu-id="25cf9-114">This script will update ACL rescursively on directory chunk by chunk, with chunk size as BatchSize \* MaxBatchCount.</span></span> <span data-ttu-id="25cf9-115">O tamanho da parte é 5000 neste script.</span><span class="sxs-lookup"><span data-stu-id="25cf9-115">Chunk size is 5000 in this script.</span></span>

### <span data-ttu-id="25cf9-116">Exemplo 4: Atualize a ACL recursivamente em um diretório e ContinueOnFailure, em seguida, retome das falhas um por vez</span><span class="sxs-lookup"><span data-stu-id="25cf9-116">Example 4: Update ACL recursively on a directory and ContinueOnFailure, then resume from failures one by one</span></span>
```
PS C:\> $result = Update-AzDataLakeGen2AclRecursive -FileSystem "filesystem1" -Path "dir1" -Acl $acl -ContinueOnFailure -Context $ctx

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
            Set-AzDataLakeGen2AclRecursive -FileSystem "filesystem1" -Path $path -Acl $acl -Context $ctx
        }
```

<span data-ttu-id="25cf9-117">Esse comando atualiza a ACL recursivamente para um diretório com ContinueOnFailure e alguns itens falharam e retomará um por um.</span><span class="sxs-lookup"><span data-stu-id="25cf9-117">This command first updateds ACL recursively to a directory with ContinueOnFailure, and some items failed, then resume the failed items one by one.</span></span>

## <span data-ttu-id="25cf9-118">OS</span><span class="sxs-lookup"><span data-stu-id="25cf9-118">PARAMETERS</span></span>

### <span data-ttu-id="25cf9-119">-ACL</span><span class="sxs-lookup"><span data-stu-id="25cf9-119">-Acl</span></span>
<span data-ttu-id="25cf9-120">A lista de controle de acesso POSIX para definir recursivamente para o arquivo ou pasta.</span><span class="sxs-lookup"><span data-stu-id="25cf9-120">The POSIX access control list to set recursively for the file or directory.</span></span>

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

### <span data-ttu-id="25cf9-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="25cf9-121">-AsJob</span></span>
<span data-ttu-id="25cf9-122">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="25cf9-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="25cf9-123">-BatchSize</span><span class="sxs-lookup"><span data-stu-id="25cf9-123">-BatchSize</span></span>
<span data-ttu-id="25cf9-124">Se o tamanho do conjunto de dados exceder o tamanho do lote, a operação será dividida em várias solicitações para que o progresso possa ser rastreado.</span><span class="sxs-lookup"><span data-stu-id="25cf9-124">If data set size exceeds batch size then operation will be split into multiple requests so that progress can be tracked.</span></span>
<span data-ttu-id="25cf9-125">O tamanho do lote deve estar entre 1 e 2000.</span><span class="sxs-lookup"><span data-stu-id="25cf9-125">Batch size should be between 1 and 2000.</span></span>
<span data-ttu-id="25cf9-126">O padrão é 2000.</span><span class="sxs-lookup"><span data-stu-id="25cf9-126">Default is 2000.</span></span>

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

### <span data-ttu-id="25cf9-127">-Contexto</span><span class="sxs-lookup"><span data-stu-id="25cf9-127">-Context</span></span>
<span data-ttu-id="25cf9-128">Objeto de contexto de armazenamento do Azure</span><span class="sxs-lookup"><span data-stu-id="25cf9-128">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="25cf9-129">-ContinuationToken</span><span class="sxs-lookup"><span data-stu-id="25cf9-129">-ContinuationToken</span></span>
<span data-ttu-id="25cf9-130">Token de continuação.</span><span class="sxs-lookup"><span data-stu-id="25cf9-130">Continuation Token.</span></span>

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

### <span data-ttu-id="25cf9-131">-ContinueOnFailure</span><span class="sxs-lookup"><span data-stu-id="25cf9-131">-ContinueOnFailure</span></span>
<span data-ttu-id="25cf9-132">Defina esse parâmetro para ignorar falhas e continuar a proceeing com a operação em outras subentidades do diretório.</span><span class="sxs-lookup"><span data-stu-id="25cf9-132">Set this parameter to ignore failures and continue proceeing with the operation on other sub-entities of the directory.</span></span> <span data-ttu-id="25cf9-133">Padrão a operação será terminada rapidamente em caso de falhas.</span><span class="sxs-lookup"><span data-stu-id="25cf9-133">Default the operation will terminate quickly on encountering failures.</span></span>

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

### <span data-ttu-id="25cf9-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25cf9-134">-DefaultProfile</span></span>
<span data-ttu-id="25cf9-135">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="25cf9-135">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="25cf9-136">-FileSystem</span><span class="sxs-lookup"><span data-stu-id="25cf9-136">-FileSystem</span></span>
<span data-ttu-id="25cf9-137">Nome do sistema de arquivos</span><span class="sxs-lookup"><span data-stu-id="25cf9-137">FileSystem name</span></span>

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

### <span data-ttu-id="25cf9-138">-MaxBatchCount</span><span class="sxs-lookup"><span data-stu-id="25cf9-138">-MaxBatchCount</span></span>
<span data-ttu-id="25cf9-139">Número máximo de lotes que a operação de controle de acesso de alteração única pode executar.</span><span class="sxs-lookup"><span data-stu-id="25cf9-139">Maximum number of batches that single change Access Control operation can execute.</span></span> <span data-ttu-id="25cf9-140">Se o tamanho do conjunto de dados exceder MaxBatchCount o BatchSize de multiplicação, o token de continuação será retornado.</span><span class="sxs-lookup"><span data-stu-id="25cf9-140">If data set size exceeds MaxBatchCount multiply BatchSize, continuation token will be return.</span></span>

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

### <span data-ttu-id="25cf9-141">-Caminho</span><span class="sxs-lookup"><span data-stu-id="25cf9-141">-Path</span></span>
<span data-ttu-id="25cf9-142">O caminho no sistema de arquivos especificado que altera a ACL recursivamente.</span><span class="sxs-lookup"><span data-stu-id="25cf9-142">The path in the specified FileSystem that to change Acl recursively.</span></span>
<span data-ttu-id="25cf9-143">Pode ser um arquivo ou diretório.</span><span class="sxs-lookup"><span data-stu-id="25cf9-143">Can be a file or directory.</span></span>
<span data-ttu-id="25cf9-144">No formato "diretório/file.txt" ou "directory1/directory2/".</span><span class="sxs-lookup"><span data-stu-id="25cf9-144">In the format 'directory/file.txt' or 'directory1/directory2/'.</span></span>
<span data-ttu-id="25cf9-145">Skip defina esse parâmetro para alterar a ACL recursivamente do diretório raiz do sistema de arquivos.</span><span class="sxs-lookup"><span data-stu-id="25cf9-145">Skip set this parameter to change Acl recursively from root directory of the Filesystem.</span></span>

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

### <span data-ttu-id="25cf9-146">-Confirme</span><span class="sxs-lookup"><span data-stu-id="25cf9-146">-Confirm</span></span>
<span data-ttu-id="25cf9-147">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="25cf9-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="25cf9-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="25cf9-148">-WhatIf</span></span>
<span data-ttu-id="25cf9-149">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="25cf9-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="25cf9-150">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="25cf9-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="25cf9-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25cf9-151">CommonParameters</span></span>
<span data-ttu-id="25cf9-152">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="25cf9-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25cf9-153">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="25cf9-153">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25cf9-154">SENSORES</span><span class="sxs-lookup"><span data-stu-id="25cf9-154">INPUTS</span></span>

### <span data-ttu-id="25cf9-155">System. String</span><span class="sxs-lookup"><span data-stu-id="25cf9-155">System.String</span></span>

### <span data-ttu-id="25cf9-156">Microsoft. Azure. Commands. Common. Authentication. Abstractings. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="25cf9-156">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="25cf9-157">EXIBE</span><span class="sxs-lookup"><span data-stu-id="25cf9-157">OUTPUTS</span></span>

### <span data-ttu-id="25cf9-158">System. String</span><span class="sxs-lookup"><span data-stu-id="25cf9-158">System.String</span></span>

## <span data-ttu-id="25cf9-159">INFORMA</span><span class="sxs-lookup"><span data-stu-id="25cf9-159">NOTES</span></span>

## <span data-ttu-id="25cf9-160">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="25cf9-160">RELATED LINKS</span></span>
