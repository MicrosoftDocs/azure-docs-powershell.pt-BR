---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/export-azdatalakestorechilditemproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Export-AzDataLakeStoreChildItemProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Export-AzDataLakeStoreChildItemProperty.md
ms.openlocfilehash: 25615684db8b78a461b39b1a8cfc159d42a56883
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93940511"
---
# <span data-ttu-id="d2019-101">Export-AzDataLakeStoreChildItemProperty</span><span class="sxs-lookup"><span data-stu-id="d2019-101">Export-AzDataLakeStoreChildItemProperty</span></span>

## <span data-ttu-id="d2019-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d2019-102">SYNOPSIS</span></span>
<span data-ttu-id="d2019-103">Exporta as propriedades (uso de disco e ACL) para a árvore inteira do caminho especificado para um caminho de saída</span><span class="sxs-lookup"><span data-stu-id="d2019-103">Exports the properties (Disk usage and Acl) for the entire tree from the specified path to a output path</span></span>

## <span data-ttu-id="d2019-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d2019-104">SYNTAX</span></span>

### <span data-ttu-id="d2019-105">GetDiskUsage</span><span class="sxs-lookup"><span data-stu-id="d2019-105">GetDiskUsage</span></span>
```
Export-AzDataLakeStoreChildItemProperty [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-OutputPath] <String> [-SaveToAdl] [-IncludeFile] [-MaximumDepth <Int32>] [-Concurrency <Int32>]
 [-GetDiskUsage] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d2019-106">GetAllProperties</span><span class="sxs-lookup"><span data-stu-id="d2019-106">GetAllProperties</span></span>
```
Export-AzDataLakeStoreChildItemProperty [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-OutputPath] <String> [-SaveToAdl] [-IncludeFile] [-MaximumDepth <Int32>] [-Concurrency <Int32>]
 [-GetDiskUsage] [-GetAcl] [-HideConsistentAcl] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d2019-107">GetAclDump</span><span class="sxs-lookup"><span data-stu-id="d2019-107">GetAclDump</span></span>
```
Export-AzDataLakeStoreChildItemProperty [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-OutputPath] <String> [-SaveToAdl] [-IncludeFile] [-MaximumDepth <Int32>] [-Concurrency <Int32>] [-GetAcl]
 [-HideConsistentAcl] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d2019-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d2019-108">DESCRIPTION</span></span>
<span data-ttu-id="d2019-109">O **Export-AzDataLakeStoreChildItemProperty** é usado para denunciar o uso de espaço de ADLS ou/e o uso de ACL para o diretório fornecido, e ele é subdiretórios e arquivos.</span><span class="sxs-lookup"><span data-stu-id="d2019-109">The **Export-AzDataLakeStoreChildItemProperty** is used to report the ADLS space usage or/and ACL usage for the given directory and it's sub directories and files.</span></span>

## <span data-ttu-id="d2019-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d2019-110">EXAMPLES</span></span>

### <span data-ttu-id="d2019-111">Exemplo 1: obter o uso de disco e o uso de ACL para todas as subpastas e arquivos</span><span class="sxs-lookup"><span data-stu-id="d2019-111">Example 1: Get the disk usage and ACL usage for all subdirectories and files</span></span>
```
PS C:\> Export-AzDataLakeStoreChildItemProperty -Account ContosoADL -Path /a -OutputPath "C:\Users\contoso\Desktop\DumpFile.txt" -GetAcl -GetDiskUsage -IncludeFile
```

<span data-ttu-id="d2019-112">Obter o uso de disco e a ACL para todas as subpastas e arquivos em/a.</span><span class="sxs-lookup"><span data-stu-id="d2019-112">Get the disk usage and ACL usage for all subdirectories and files under /a.</span></span> <span data-ttu-id="d2019-113">Includefile garante que o uso seja reportado para arquivos também</span><span class="sxs-lookup"><span data-stu-id="d2019-113">IncludeFile ensures the usage is reported for files also</span></span>

### <span data-ttu-id="d2019-114">Exemplo 2: obter o uso de ACL para todas as subpastas e arquivos com a ACL consistente oculta</span><span class="sxs-lookup"><span data-stu-id="d2019-114">Example 2: Get the ACL usage for all subdirectories and files with the consistent ACL hidden</span></span>
```
PS C:\> $fullAcl="user:contoso-userid:--x|user::rwx|other::---|group::rwx"
PS C:\> $newFullAcl = $fullAcl.Split("{|}");
PS C:\> Set-AzDataLakeStoreItemAcl -Account ContosoADL -Path /a -Acl $newFullAcl -Recurse -Debug

PS C:\> Export-AzDataLakeStoreChildItemProperty -Account ContosoADL -Path /a -OutputPath "C:\Users\contoso\Desktop\DumpFile.txt" -GetAcl -HideConsistentAcl -IncludeFile
```

<span data-ttu-id="d2019-115">Obter o uso de ACL para todas as subpastas e arquivos em/a.</span><span class="sxs-lookup"><span data-stu-id="d2019-115">Get the ACL usage for all subdirectories and files under /a.</span></span> <span data-ttu-id="d2019-116">Includefile garante que o uso também seja reportado para arquivos.</span><span class="sxs-lookup"><span data-stu-id="d2019-116">IncludeFile ensures the usage is reported for files also.</span></span> <span data-ttu-id="d2019-117">HideconsistentAcl, nesse caso, mostrará a ACL de/a, não é filho, pois todos os filhos têm a mesma ACL como/a.</span><span class="sxs-lookup"><span data-stu-id="d2019-117">HideconsistentAcl in this case will show the Acl of /a, not it's children since all of the children has same acl as /a.</span></span> <span data-ttu-id="d2019-118">Esse sinalizador ignora a saída de ACL da subárvore se todas elas forem ACLs iguais à raiz.</span><span class="sxs-lookup"><span data-stu-id="d2019-118">This flag skips the acl output of subtree if all it's acls are same as the root.</span></span>

## <span data-ttu-id="d2019-119">OS</span><span class="sxs-lookup"><span data-stu-id="d2019-119">PARAMETERS</span></span>

### <span data-ttu-id="d2019-120">-Conta</span><span class="sxs-lookup"><span data-stu-id="d2019-120">-Account</span></span>
<span data-ttu-id="d2019-121">A conta do data Lake Store para executar a operação do sistema de arquivos no</span><span class="sxs-lookup"><span data-stu-id="d2019-121">The Data Lake Store account to execute the filesystem operation in</span></span>

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

### <span data-ttu-id="d2019-122">-Simultaneidade</span><span class="sxs-lookup"><span data-stu-id="d2019-122">-Concurrency</span></span>
<span data-ttu-id="d2019-123">Indica o número de arquivos/pastas processados em paralelo.</span><span class="sxs-lookup"><span data-stu-id="d2019-123">Indicates the number of files/directories processed in parallel.</span></span>
<span data-ttu-id="d2019-124">O padrão será calculado como um melhor esforço com base na especificação do sistema.</span><span class="sxs-lookup"><span data-stu-id="d2019-124">Default will be computed as a best effort based on system specification.</span></span>

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

### <span data-ttu-id="d2019-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2019-125">-DefaultProfile</span></span>
<span data-ttu-id="d2019-126">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d2019-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d2019-127">-GetAcl</span><span class="sxs-lookup"><span data-stu-id="d2019-127">-GetAcl</span></span>
<span data-ttu-id="d2019-128">Recupera a ACL começando do caminho raiz</span><span class="sxs-lookup"><span data-stu-id="d2019-128">Retrieves the acl starting from the root path</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GetAllProperties, GetAclDump
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d2019-129">-GetDiskUsage</span><span class="sxs-lookup"><span data-stu-id="d2019-129">-GetDiskUsage</span></span>
<span data-ttu-id="d2019-130">Recupera o uso do disco começando do caminho raiz</span><span class="sxs-lookup"><span data-stu-id="d2019-130">Retrieves the disk usage starting from the root path</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GetDiskUsage, GetAllProperties
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d2019-131">-HideConsistentAcl</span><span class="sxs-lookup"><span data-stu-id="d2019-131">-HideConsistentAcl</span></span>
<span data-ttu-id="d2019-132">Não mostrar subárvore de diretório se as ACLs forem iguais em toda a subárvore.</span><span class="sxs-lookup"><span data-stu-id="d2019-132">Do not show directory subtree if the ACLs are the same throughout the entire subtree.</span></span> <span data-ttu-id="d2019-133">Isso facilita a visualização apenas dos caminhos até os quais as ACLs são diferentes. Por exemplo, se todos os arquivos e pastas em/a/b forem iguais, não mostre o subtreeunder/a/b e apenas a saída de/a/b com ' true ' na ACL consistente columnCannot ser definidas se IncludeFiles não estiver definido, porque a ACL consistente não pode ser determinada sem recuperar ACLs para os arquivos.</span><span class="sxs-lookup"><span data-stu-id="d2019-133">This makes it easier to see only the paths up to which the ACLs differ.For example if all files and folders under /a/b are the same, do not show the subtreeunder /a/b, and just output /a/b with 'True' in the Consistent ACL columnCannot be set if IncludeFiles is not set, because consistent Acl cannot be determined without retrieving acls for the files.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GetAllProperties, GetAclDump
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d2019-134">-Includefile</span><span class="sxs-lookup"><span data-stu-id="d2019-134">-IncludeFile</span></span>
<span data-ttu-id="d2019-135">Mostrar estatísticas em nível de arquivo (o padrão é mostrar somente informações no nível do diretório)</span><span class="sxs-lookup"><span data-stu-id="d2019-135">Show stats at file level (default is to show directory-level info only)</span></span>

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

### <span data-ttu-id="d2019-136">-MaximumDepth</span><span class="sxs-lookup"><span data-stu-id="d2019-136">-MaximumDepth</span></span>
<span data-ttu-id="d2019-137">Profundidade máxima do diretório raiz até a qual o uso do disco ou ACL é exibido</span><span class="sxs-lookup"><span data-stu-id="d2019-137">Maximum depth from the root directory till which disk usage or acl is displayed</span></span>

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

### <span data-ttu-id="d2019-138">-OutputPath</span><span class="sxs-lookup"><span data-stu-id="d2019-138">-OutputPath</span></span>
<span data-ttu-id="d2019-139">Caminho para o arquivo de saída.</span><span class="sxs-lookup"><span data-stu-id="d2019-139">Path to output file.</span></span> <span data-ttu-id="d2019-140">Pode ser um caminho local ou caminho ADL.</span><span class="sxs-lookup"><span data-stu-id="d2019-140">Can be a Local path or Adl Path.</span></span> <span data-ttu-id="d2019-141">Por padrão, é local.</span><span class="sxs-lookup"><span data-stu-id="d2019-141">By default it is local.</span></span> <span data-ttu-id="d2019-142">Se SaveToAdl for especificado, será um caminho ADL na mesma conta</span><span class="sxs-lookup"><span data-stu-id="d2019-142">If SaveToAdl is specified then it is an ADL path in the same account</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d2019-143">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d2019-143">-PassThru</span></span>
<span data-ttu-id="d2019-144">Indica que uma resposta booliana deve ser retornada indicando o resultado da operação de exclusão.</span><span class="sxs-lookup"><span data-stu-id="d2019-144">Indicates a boolean response should be returned indicating the result of the delete operation.</span></span>

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

### <span data-ttu-id="d2019-145">-Caminho</span><span class="sxs-lookup"><span data-stu-id="d2019-145">-Path</span></span>
<span data-ttu-id="d2019-146">O caminho na conta data Lake especificada que deve ser recuperada.</span><span class="sxs-lookup"><span data-stu-id="d2019-146">The path in the specified Data Lake account that should be retrieve.</span></span>
<span data-ttu-id="d2019-147">Pode ser um arquivo ou uma pasta no formato '/Folder/file.txt ', em que o primeiro '/' após o DNS indica a raiz do sistema de arquivos.</span><span class="sxs-lookup"><span data-stu-id="d2019-147">Can be a file or folder In the format '/folder/file.txt', where the first '/' after the DNS indicates the root of the file system.</span></span>

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

### <span data-ttu-id="d2019-148">-SaveToAdl</span><span class="sxs-lookup"><span data-stu-id="d2019-148">-SaveToAdl</span></span>
<span data-ttu-id="d2019-149">Se passado, salva o arquivo de despejo no ADL.</span><span class="sxs-lookup"><span data-stu-id="d2019-149">If passed then saves the dump file to ADL.</span></span>
<span data-ttu-id="d2019-150">O dumpfile ouvirá ser um caminho ADL nesse caso</span><span class="sxs-lookup"><span data-stu-id="d2019-150">The DumpFile wil be a ADL path in that case</span></span>

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

### <span data-ttu-id="d2019-151">-Confirme</span><span class="sxs-lookup"><span data-stu-id="d2019-151">-Confirm</span></span>
<span data-ttu-id="d2019-152">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d2019-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d2019-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d2019-153">-WhatIf</span></span>
<span data-ttu-id="d2019-154">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="d2019-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d2019-155">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d2019-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d2019-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2019-156">CommonParameters</span></span>
<span data-ttu-id="d2019-157">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d2019-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2019-158">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d2019-158">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2019-159">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d2019-159">INPUTS</span></span>

### <span data-ttu-id="d2019-160">System. String</span><span class="sxs-lookup"><span data-stu-id="d2019-160">System.String</span></span>

### <span data-ttu-id="d2019-161">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="d2019-161">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="d2019-162">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="d2019-162">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="d2019-163">System. Int32</span><span class="sxs-lookup"><span data-stu-id="d2019-163">System.Int32</span></span>

## <span data-ttu-id="d2019-164">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d2019-164">OUTPUTS</span></span>

### <span data-ttu-id="d2019-165">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d2019-165">System.Boolean</span></span>

## <span data-ttu-id="d2019-166">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d2019-166">NOTES</span></span>

## <span data-ttu-id="d2019-167">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d2019-167">RELATED LINKS</span></span>
