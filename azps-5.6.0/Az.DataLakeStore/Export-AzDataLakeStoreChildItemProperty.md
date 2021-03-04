---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
online version: https://docs.microsoft.com/powershell/module/az.datalakestore/export-azdatalakestorechilditemproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Export-AzDataLakeStoreChildItemProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Export-AzDataLakeStoreChildItemProperty.md
ms.openlocfilehash: 0f43c372901dbfd571343584f0ca8479d5b7081e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101893360"
---
# <span data-ttu-id="c558d-101">Export-AzDataLakeStoreChildItemProperty</span><span class="sxs-lookup"><span data-stu-id="c558d-101">Export-AzDataLakeStoreChildItemProperty</span></span>

## <span data-ttu-id="c558d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c558d-102">SYNOPSIS</span></span>
<span data-ttu-id="c558d-103">Exporta as propriedades (Uso de disco e Acl) para toda a árvore do caminho especificado para um caminho de saída</span><span class="sxs-lookup"><span data-stu-id="c558d-103">Exports the properties (Disk usage and Acl) for the entire tree from the specified path to a output path</span></span>

## <span data-ttu-id="c558d-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="c558d-104">SYNTAX</span></span>

### <span data-ttu-id="c558d-105">GetDiskUsage</span><span class="sxs-lookup"><span data-stu-id="c558d-105">GetDiskUsage</span></span>
```
Export-AzDataLakeStoreChildItemProperty [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-OutputPath] <String> [-SaveToAdl] [-IncludeFile] [-MaximumDepth <Int32>] [-Concurrency <Int32>]
 [-GetDiskUsage] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c558d-106">GetAllProperties</span><span class="sxs-lookup"><span data-stu-id="c558d-106">GetAllProperties</span></span>
```
Export-AzDataLakeStoreChildItemProperty [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-OutputPath] <String> [-SaveToAdl] [-IncludeFile] [-MaximumDepth <Int32>] [-Concurrency <Int32>]
 [-GetDiskUsage] [-GetAcl] [-HideConsistentAcl] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c558d-107">GetAclDump</span><span class="sxs-lookup"><span data-stu-id="c558d-107">GetAclDump</span></span>
```
Export-AzDataLakeStoreChildItemProperty [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-OutputPath] <String> [-SaveToAdl] [-IncludeFile] [-MaximumDepth <Int32>] [-Concurrency <Int32>] [-GetAcl]
 [-HideConsistentAcl] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c558d-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="c558d-108">DESCRIPTION</span></span>
<span data-ttu-id="c558d-109">**Export-AzDataLakeStoreChildItemProperty** é usada para relatar o uso de espaço ou/e ACL do ADLS para o diretório determinado e seus sub diretórios e arquivos.</span><span class="sxs-lookup"><span data-stu-id="c558d-109">The **Export-AzDataLakeStoreChildItemProperty** is used to report the ADLS space usage or/and ACL usage for the given directory and it's sub directories and files.</span></span>

## <span data-ttu-id="c558d-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c558d-110">EXAMPLES</span></span>

### <span data-ttu-id="c558d-111">Exemplo 1: Obter o uso do disco e o uso de ACL para todos os subdiretários e arquivos</span><span class="sxs-lookup"><span data-stu-id="c558d-111">Example 1: Get the disk usage and ACL usage for all subdirectories and files</span></span>
```
PS C:\> Export-AzDataLakeStoreChildItemProperty -Account ContosoADL -Path /a -OutputPath "C:\Users\contoso\Desktop\DumpFile.txt" -GetAcl -GetDiskUsage -IncludeFile
```

<span data-ttu-id="c558d-112">Obter o uso do disco e o uso de ACL para todos os subdiretários e arquivos em /a.</span><span class="sxs-lookup"><span data-stu-id="c558d-112">Get the disk usage and ACL usage for all subdirectories and files under /a.</span></span> <span data-ttu-id="c558d-113">IncludeFile garante que o uso também seja relatado para arquivos</span><span class="sxs-lookup"><span data-stu-id="c558d-113">IncludeFile ensures the usage is reported for files also</span></span>

### <span data-ttu-id="c558d-114">Exemplo 2: Obter o uso de ACL para todos os subdireários e arquivos com o ACL consistente oculto</span><span class="sxs-lookup"><span data-stu-id="c558d-114">Example 2: Get the ACL usage for all subdirectories and files with the consistent ACL hidden</span></span>
```
PS C:\> $fullAcl="user:contoso-userid:--x|user::rwx|other::---|group::rwx"
PS C:\> $newFullAcl = $fullAcl.Split("{|}");
PS C:\> Set-AzDataLakeStoreItemAcl -Account ContosoADL -Path /a -Acl $newFullAcl -Recurse -Debug

PS C:\> Export-AzDataLakeStoreChildItemProperty -Account ContosoADL -Path /a -OutputPath "C:\Users\contoso\Desktop\DumpFile.txt" -GetAcl -HideConsistentAcl -IncludeFile
```

<span data-ttu-id="c558d-115">Obter o uso de ACL para todos os subdireários e arquivos em /a.</span><span class="sxs-lookup"><span data-stu-id="c558d-115">Get the ACL usage for all subdirectories and files under /a.</span></span> <span data-ttu-id="c558d-116">IncludeFile garante que o uso também seja relatado para arquivos.</span><span class="sxs-lookup"><span data-stu-id="c558d-116">IncludeFile ensures the usage is reported for files also.</span></span> <span data-ttu-id="c558d-117">HideconsistentAcl neste caso mostrará a Acl de /a, não são filhos, pois todas as crianças têm a mesma acl de /a.</span><span class="sxs-lookup"><span data-stu-id="c558d-117">HideconsistentAcl in this case will show the Acl of /a, not it's children since all of the children has same acl as /a.</span></span> <span data-ttu-id="c558d-118">Esse sinalizador ignora a saída acl da subárvore se todas as acls são iguais à raiz.</span><span class="sxs-lookup"><span data-stu-id="c558d-118">This flag skips the acl output of subtree if all it's acls are same as the root.</span></span>

## <span data-ttu-id="c558d-119">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="c558d-119">PARAMETERS</span></span>

### <span data-ttu-id="c558d-120">-Account</span><span class="sxs-lookup"><span data-stu-id="c558d-120">-Account</span></span>
<span data-ttu-id="c558d-121">A conta do Data Lake Store para executar a operação do sistema de arquivos em</span><span class="sxs-lookup"><span data-stu-id="c558d-121">The Data Lake Store account to execute the filesystem operation in</span></span>

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

### <span data-ttu-id="c558d-122">-Concurrency</span><span class="sxs-lookup"><span data-stu-id="c558d-122">-Concurrency</span></span>
<span data-ttu-id="c558d-123">Indica o número de arquivos/diretórios processados em paralelo.</span><span class="sxs-lookup"><span data-stu-id="c558d-123">Indicates the number of files/directories processed in parallel.</span></span>
<span data-ttu-id="c558d-124">O padrão será calculado como um melhor esforço com base na especificação do sistema.</span><span class="sxs-lookup"><span data-stu-id="c558d-124">Default will be computed as a best effort based on system specification.</span></span>

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

### <span data-ttu-id="c558d-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c558d-125">-DefaultProfile</span></span>
<span data-ttu-id="c558d-126">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c558d-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c558d-127">-GetAcl</span><span class="sxs-lookup"><span data-stu-id="c558d-127">-GetAcl</span></span>
<span data-ttu-id="c558d-128">Recupera a acl começando do caminho raiz</span><span class="sxs-lookup"><span data-stu-id="c558d-128">Retrieves the acl starting from the root path</span></span>

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

### <span data-ttu-id="c558d-129">-GetDiskUsage</span><span class="sxs-lookup"><span data-stu-id="c558d-129">-GetDiskUsage</span></span>
<span data-ttu-id="c558d-130">Recupera o uso do disco começando pelo caminho raiz</span><span class="sxs-lookup"><span data-stu-id="c558d-130">Retrieves the disk usage starting from the root path</span></span>

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

### <span data-ttu-id="c558d-131">-HideConsistentAcl</span><span class="sxs-lookup"><span data-stu-id="c558d-131">-HideConsistentAcl</span></span>
<span data-ttu-id="c558d-132">Não mostre a subárvore de diretório se as ACLs são as mesmas em toda a subárvore inteira.</span><span class="sxs-lookup"><span data-stu-id="c558d-132">Do not show directory subtree if the ACLs are the same throughout the entire subtree.</span></span> <span data-ttu-id="c558d-133">Isso torna mais fácil ver apenas os caminhos até os quais as ACLs diferem. Por exemplo, se todos os arquivos e pastas em /a/b são os mesmos, não mostre a subárvore /a/b e apenas a saída /a/b com 'True' na coluna Consistente ACLNão pode ser definido se IncludeFiles não estiver definido, porque a Acl consistente não pode ser determinada sem recuperar acls para os arquivos.</span><span class="sxs-lookup"><span data-stu-id="c558d-133">This makes it easier to see only the paths up to which the ACLs differ.For example if all files and folders under /a/b are the same, do not show the subtreeunder /a/b, and just output /a/b with 'True' in the Consistent ACL columnCannot be set if IncludeFiles is not set, because consistent Acl cannot be determined without retrieving acls for the files.</span></span>

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

### <span data-ttu-id="c558d-134">-IncludeFile</span><span class="sxs-lookup"><span data-stu-id="c558d-134">-IncludeFile</span></span>
<span data-ttu-id="c558d-135">Mostrar estatísticas no nível do arquivo (o padrão é mostrar somente informações no nível do diretório)</span><span class="sxs-lookup"><span data-stu-id="c558d-135">Show stats at file level (default is to show directory-level info only)</span></span>

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

### <span data-ttu-id="c558d-136">-MaximumDepth</span><span class="sxs-lookup"><span data-stu-id="c558d-136">-MaximumDepth</span></span>
<span data-ttu-id="c558d-137">Profundidade máxima do diretório raiz até qual uso de disco ou acl é exibido</span><span class="sxs-lookup"><span data-stu-id="c558d-137">Maximum depth from the root directory till which disk usage or acl is displayed</span></span>

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

### <span data-ttu-id="c558d-138">-OutputPath</span><span class="sxs-lookup"><span data-stu-id="c558d-138">-OutputPath</span></span>
<span data-ttu-id="c558d-139">Caminho para o arquivo de saída.</span><span class="sxs-lookup"><span data-stu-id="c558d-139">Path to output file.</span></span> <span data-ttu-id="c558d-140">Pode ser um caminho local ou caminho do Adl.</span><span class="sxs-lookup"><span data-stu-id="c558d-140">Can be a Local path or Adl Path.</span></span> <span data-ttu-id="c558d-141">Por padrão, ele é local.</span><span class="sxs-lookup"><span data-stu-id="c558d-141">By default it is local.</span></span> <span data-ttu-id="c558d-142">Se SaveToAdl for especificado, ele será um caminho ADL na mesma conta</span><span class="sxs-lookup"><span data-stu-id="c558d-142">If SaveToAdl is specified then it is an ADL path in the same account</span></span>

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

### <span data-ttu-id="c558d-143">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c558d-143">-PassThru</span></span>
<span data-ttu-id="c558d-144">Indica que uma resposta booleana deve ser retornada indicando o resultado da operação de exclusão.</span><span class="sxs-lookup"><span data-stu-id="c558d-144">Indicates a boolean response should be returned indicating the result of the delete operation.</span></span>

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

### <span data-ttu-id="c558d-145">-Path</span><span class="sxs-lookup"><span data-stu-id="c558d-145">-Path</span></span>
<span data-ttu-id="c558d-146">O caminho na conta do Data Lake especificada que deve ser recuperado.</span><span class="sxs-lookup"><span data-stu-id="c558d-146">The path in the specified Data Lake account that should be retrieve.</span></span>
<span data-ttu-id="c558d-147">Pode ser um arquivo ou pasta No formato '/folder/file.txt', onde o primeiro '/' após o DNS indica a raiz do sistema de arquivos.</span><span class="sxs-lookup"><span data-stu-id="c558d-147">Can be a file or folder In the format '/folder/file.txt', where the first '/' after the DNS indicates the root of the file system.</span></span>

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

### <span data-ttu-id="c558d-148">-SaveToAdl</span><span class="sxs-lookup"><span data-stu-id="c558d-148">-SaveToAdl</span></span>
<span data-ttu-id="c558d-149">Se passado, salva o arquivo de despejo no ADL.</span><span class="sxs-lookup"><span data-stu-id="c558d-149">If passed then saves the dump file to ADL.</span></span>
<span data-ttu-id="c558d-150">O DumpFile será um caminho ADL nesse caso</span><span class="sxs-lookup"><span data-stu-id="c558d-150">The DumpFile wil be a ADL path in that case</span></span>

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

### <span data-ttu-id="c558d-151">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c558d-151">-Confirm</span></span>
<span data-ttu-id="c558d-152">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c558d-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c558d-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c558d-153">-WhatIf</span></span>
<span data-ttu-id="c558d-154">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="c558d-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c558d-155">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c558d-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c558d-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c558d-156">CommonParameters</span></span>
<span data-ttu-id="c558d-157">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c558d-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c558d-158">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c558d-158">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c558d-159">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c558d-159">INPUTS</span></span>

### <span data-ttu-id="c558d-160">System.String</span><span class="sxs-lookup"><span data-stu-id="c558d-160">System.String</span></span>

### <span data-ttu-id="c558d-161">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="c558d-161">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="c558d-162">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="c558d-162">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="c558d-163">System.Int32</span><span class="sxs-lookup"><span data-stu-id="c558d-163">System.Int32</span></span>

## <span data-ttu-id="c558d-164">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="c558d-164">OUTPUTS</span></span>

### <span data-ttu-id="c558d-165">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="c558d-165">System.Boolean</span></span>

## <span data-ttu-id="c558d-166">NOTES</span><span class="sxs-lookup"><span data-stu-id="c558d-166">NOTES</span></span>

## <span data-ttu-id="c558d-167">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c558d-167">RELATED LINKS</span></span>
