---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azdatalakegen2aclrecursive
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzDataLakeGen2AclRecursive.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzDataLakeGen2AclRecursive.md
ms.openlocfilehash: 25b1c275aeed7ca56c4c2b873bdf4b9a79eb756b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115641"
---
# <span data-ttu-id="16f83-101">Set-AzDataLakeGen2AclRecursive</span><span class="sxs-lookup"><span data-stu-id="16f83-101">Set-AzDataLakeGen2AclRecursive</span></span>

## <span data-ttu-id="16f83-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="16f83-102">SYNOPSIS</span></span>
<span data-ttu-id="16f83-103">Definir ACL recursivamente no caminho especificado.</span><span class="sxs-lookup"><span data-stu-id="16f83-103">Set ACL recursively on the specified path.</span></span> 

## <span data-ttu-id="16f83-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="16f83-104">SYNTAX</span></span>

```
Set-AzDataLakeGen2AclRecursive [-FileSystem] <String> [[-Path] <String>] [-ContinuationToken <String>]
 -Acl <PSPathAccessControlEntry[]> [-ContinueOnFailure] [-BatchSize <Int32>] [-MaxBatchCount <Int32>] [-AsJob]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="16f83-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="16f83-105">DESCRIPTION</span></span>
<span data-ttu-id="16f83-106">O cmdlet **Set-AzDataLakeGen2AclRecursive** define a ACL recursivamente no caminho especificado.</span><span class="sxs-lookup"><span data-stu-id="16f83-106">The **Set-AzDataLakeGen2AclRecursive** cmdlet sets ACL recursively on the specified path.</span></span> <span data-ttu-id="16f83-107">O ACL de entrada substituirá completamente o ACL original.</span><span class="sxs-lookup"><span data-stu-id="16f83-107">The input ACL will replace original ACL completely.</span></span>

## <span data-ttu-id="16f83-108">Exemplos</span><span class="sxs-lookup"><span data-stu-id="16f83-108">EXAMPLES</span></span>

### <span data-ttu-id="16f83-109">Exemplo 1: Definir ACL recursivamente em um diretório</span><span class="sxs-lookup"><span data-stu-id="16f83-109">Example 1: Set ACL recursively on a directory</span></span>
```
PS C:\>$acl = New-AzDataLakeGen2ItemAclObject -AccessControlType user -Permission rwx 
PS C:\>$acl = New-AzDataLakeGen2ItemAclObject -AccessControlType group -Permission rw- -InputObject $acl 
PS C:\>$acl = New-AzDataLakeGen2ItemAclObject -AccessControlType other -Permission "rw-" -InputObject $acl
PS C:\> Set-AzDataLakeGen2AclRecursive -FileSystem "filesystem1" -Path "dir1" -Acl $acl -Context $ctx

FailedEntries                   : 
TotalDirectoriesSuccessfulCount : 7
TotalFilesSuccessfulCount       : 5
TotalFailureCount               : 0
ContinuationToken               :
```

<span data-ttu-id="16f83-110">Esse comando primeiro cria um objeto ACL com 3 entradas de acl e, em seguida, define a ACL recursivamente em um diretório.</span><span class="sxs-lookup"><span data-stu-id="16f83-110">This command first creates an ACL object with 3 acl entries, then sets ACL recursively on a directory.</span></span>

### <span data-ttu-id="16f83-111">Exemplo 2: Definir ACL recursivamente em um diretório raiz de sistema de arquivos</span><span class="sxs-lookup"><span data-stu-id="16f83-111">Example 2: Set ACL recursively on a root directory of filesystem</span></span>
```
PS C:\> $result = Set-AzDataLakeGen2AclRecursive -FileSystem "filesystem1" -Acl $acl  -Context $ctx

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

PS C:\> $result = Set-AzDataLakeGen2AclRecursive -FileSystem "filesystem1" -Acl $acl -ContinuationToken $result.ContinuationToken -Context $ctx

PS C:\> $result

FailedEntries                   : 
TotalDirectoriesSuccessfulCount : 100
TotalFilesSuccessfulCount       : 1000
TotalFailureCount               : 0
ContinuationToken               :
```

<span data-ttu-id="16f83-112">Esse comando primeiro define a ACL recursivamente como um diretório raiz e falha e, em seguida, retoma com ContinuationToken depois que o usuário corrige o arquivo com falha.</span><span class="sxs-lookup"><span data-stu-id="16f83-112">This command first sets ACL recursively to a root directory and failed, then resume with ContinuationToken after user fix the failed file.</span></span>

### <span data-ttu-id="16f83-113">Exemplo 3: Definir ACL de forma recursiva de forma recursiva por bloco</span><span class="sxs-lookup"><span data-stu-id="16f83-113">Example 3: Set ACL recursively chunk by chunk</span></span>
```
$token = $null
$TotalDirectoriesSuccess = 0
$TotalFilesSuccess = 0
$totalFailure = 0
$FailedEntries = New-Object System.Collections.Generic.List[System.Object]
do
{
    $result = Set-AzDataLakeGen2AclRecursive -FileSystem "filesystem1" -Path "dir1" -Acl $acl  -BatchSize 100 -MaxBatchCount 2 -ContinuationToken $token -Context $ctx

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

<span data-ttu-id="16f83-114">Esse script define a ACL rescursivamente em bloco de diretório por bloco, com tamanho de bloco como BatchSize \* MaxBatchCount.</span><span class="sxs-lookup"><span data-stu-id="16f83-114">This script sets ACL rescursively on directory chunk by chunk, with chunk size as BatchSize \* MaxBatchCount.</span></span> <span data-ttu-id="16f83-115">O tamanho do bloco é 200 neste script.</span><span class="sxs-lookup"><span data-stu-id="16f83-115">Chunk size is 200 in this script.</span></span>

### <span data-ttu-id="16f83-116">Exemplo 4: Definir a ACL recursivamente em um diretório e ContinuarOnFailure e retomar das falhas um por um</span><span class="sxs-lookup"><span data-stu-id="16f83-116">Example 4: Set ACL recursively on a directory and ContinueOnFailure, then resume from failures one by one</span></span>
```
PS C:\> $result = Set-AzDataLakeGen2AclRecursive -FileSystem "filesystem1" -Path "dir1" -Acl $acl -ContinueOnFailure -Context $ctx

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

<span data-ttu-id="16f83-117">Esse comando primeiro define a ACL recursivamente para um diretório com o ContinueOnFailure e alguns itens falharam e, em seguida, retome os itens com falha um por um.</span><span class="sxs-lookup"><span data-stu-id="16f83-117">This command first sets ACL recursively to a directory with ContinueOnFailure, and some items failed, then resume the failed items one by one.</span></span>

## <span data-ttu-id="16f83-118">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="16f83-118">PARAMETERS</span></span>

### <span data-ttu-id="16f83-119">-Acl</span><span class="sxs-lookup"><span data-stu-id="16f83-119">-Acl</span></span>
<span data-ttu-id="16f83-120">A lista de controles de acesso POSIX para definir recursivamente para o arquivo ou diretório.</span><span class="sxs-lookup"><span data-stu-id="16f83-120">The POSIX access control list to set recursively for the file or directory.</span></span>

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

### <span data-ttu-id="16f83-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="16f83-121">-AsJob</span></span>
<span data-ttu-id="16f83-122">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="16f83-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="16f83-123">-BatchSize</span><span class="sxs-lookup"><span data-stu-id="16f83-123">-BatchSize</span></span>
<span data-ttu-id="16f83-124">Se o tamanho do conjunto de dados exceder o tamanho do lote, a operação será dividida em várias solicitações para que o progresso possa ser acompanhado.</span><span class="sxs-lookup"><span data-stu-id="16f83-124">If data set size exceeds batch size then operation will be split into multiple requests so that progress can be tracked.</span></span>
<span data-ttu-id="16f83-125">O tamanho do lote deve estar entre 1 e 2000.</span><span class="sxs-lookup"><span data-stu-id="16f83-125">Batch size should be between 1 and 2000.</span></span>
<span data-ttu-id="16f83-126">O padrão é 2000.</span><span class="sxs-lookup"><span data-stu-id="16f83-126">Default is 2000.</span></span>

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

### <span data-ttu-id="16f83-127">-Contexto</span><span class="sxs-lookup"><span data-stu-id="16f83-127">-Context</span></span>
<span data-ttu-id="16f83-128">Objeto de contexto de armazenamento do Azure</span><span class="sxs-lookup"><span data-stu-id="16f83-128">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="16f83-129">-ContinuationToken</span><span class="sxs-lookup"><span data-stu-id="16f83-129">-ContinuationToken</span></span>
<span data-ttu-id="16f83-130">Token de Continuação.</span><span class="sxs-lookup"><span data-stu-id="16f83-130">Continuation Token.</span></span>

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

### <span data-ttu-id="16f83-131">-ContinueOnFailure</span><span class="sxs-lookup"><span data-stu-id="16f83-131">-ContinueOnFailure</span></span>
<span data-ttu-id="16f83-132">De definir este parâmetro para ignorar falhas e continuar proceeing com a operação em outras sub-entidades do diretório.</span><span class="sxs-lookup"><span data-stu-id="16f83-132">Set this parameter to ignore failures and continue proceeing with the operation on other sub-entities of the directory.</span></span> <span data-ttu-id="16f83-133">Por padrão, a operação terminará rapidamente ao encontrar falhas.</span><span class="sxs-lookup"><span data-stu-id="16f83-133">Default the operation will terminate quickly on encountering failures.</span></span>

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

### <span data-ttu-id="16f83-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16f83-134">-DefaultProfile</span></span>
<span data-ttu-id="16f83-135">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="16f83-135">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="16f83-136">-FileSystem</span><span class="sxs-lookup"><span data-stu-id="16f83-136">-FileSystem</span></span>
<span data-ttu-id="16f83-137">Nome do Sistema de Arquivos</span><span class="sxs-lookup"><span data-stu-id="16f83-137">FileSystem name</span></span>

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

### <span data-ttu-id="16f83-138">-MaxBatchCount</span><span class="sxs-lookup"><span data-stu-id="16f83-138">-MaxBatchCount</span></span>
<span data-ttu-id="16f83-139">Número máximo de lotes que podem ser executados com uma única alteração na operação do Controle de Acesso.</span><span class="sxs-lookup"><span data-stu-id="16f83-139">Maximum number of batches that single change Access Control operation can execute.</span></span> <span data-ttu-id="16f83-140">Se o tamanho do conjunto de dados exceder MaxBatchCount multiplicar LoteSize, o token de continuação será retornada.</span><span class="sxs-lookup"><span data-stu-id="16f83-140">If data set size exceeds MaxBatchCount multiply BatchSize, continuation token will be return.</span></span>

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

### <span data-ttu-id="16f83-141">-Caminho</span><span class="sxs-lookup"><span data-stu-id="16f83-141">-Path</span></span>
<span data-ttu-id="16f83-142">O caminho no Sistema de Arquivos especificado que para alterar o Acl recursivamente.</span><span class="sxs-lookup"><span data-stu-id="16f83-142">The path in the specified FileSystem that to change Acl recursively.</span></span>
<span data-ttu-id="16f83-143">Pode ser um arquivo ou diretório.</span><span class="sxs-lookup"><span data-stu-id="16f83-143">Can be a file or directory.</span></span>
<span data-ttu-id="16f83-144">No formato "diretório/file.txt" ou "diretório1/diretório2/".</span><span class="sxs-lookup"><span data-stu-id="16f83-144">In the format 'directory/file.txt' or 'directory1/directory2/'.</span></span>
<span data-ttu-id="16f83-145">Ignore definir esse parâmetro para alterar o Acl recursivamente do diretório raiz do sistema de arquivos.</span><span class="sxs-lookup"><span data-stu-id="16f83-145">Skip set this parameter to change Acl recursively from root directory of the Filesystem.</span></span>

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

### <span data-ttu-id="16f83-146">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="16f83-146">-Confirm</span></span>
<span data-ttu-id="16f83-147">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="16f83-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="16f83-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="16f83-148">-WhatIf</span></span>
<span data-ttu-id="16f83-149">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="16f83-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="16f83-150">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="16f83-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="16f83-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16f83-151">CommonParameters</span></span>
<span data-ttu-id="16f83-152">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="16f83-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16f83-153">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="16f83-153">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16f83-154">Entradas</span><span class="sxs-lookup"><span data-stu-id="16f83-154">INPUTS</span></span>

### <span data-ttu-id="16f83-155">System.String</span><span class="sxs-lookup"><span data-stu-id="16f83-155">System.String</span></span>

### <span data-ttu-id="16f83-156">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="16f83-156">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="16f83-157">Saídas</span><span class="sxs-lookup"><span data-stu-id="16f83-157">OUTPUTS</span></span>

### <span data-ttu-id="16f83-158">System.String</span><span class="sxs-lookup"><span data-stu-id="16f83-158">System.String</span></span>

## <span data-ttu-id="16f83-159">Notas</span><span class="sxs-lookup"><span data-stu-id="16f83-159">NOTES</span></span>

## <span data-ttu-id="16f83-160">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="16f83-160">RELATED LINKS</span></span>
