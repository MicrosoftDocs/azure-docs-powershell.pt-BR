---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/get-azdatalakegen2childitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzDataLakeGen2ChildItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzDataLakeGen2ChildItem.md
ms.openlocfilehash: 3505d9b07e1d56936a002b45bfeee7929823f4be
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889602"
---
# <span data-ttu-id="47758-101">Get-AzDataLakeGen2ChildItem</span><span class="sxs-lookup"><span data-stu-id="47758-101">Get-AzDataLakeGen2ChildItem</span></span>

## <span data-ttu-id="47758-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="47758-102">SYNOPSIS</span></span>
<span data-ttu-id="47758-103">Lista subdados e arquivos de uma raiz de diretório ou sistema de arquivos.</span><span class="sxs-lookup"><span data-stu-id="47758-103">Lists sub directorys and files from a directory or filesystem root.</span></span>

## <span data-ttu-id="47758-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="47758-104">SYNTAX</span></span>

```
Get-AzDataLakeGen2ChildItem [-FileSystem] <String> [[-Path] <String>] [-FetchProperty] [-Recurse]
 [-MaxCount <Int32>] [-ContinuationToken <String>] [-AsJob] [-OutputUserPrincipalName]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="47758-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="47758-105">DESCRIPTION</span></span>
<span data-ttu-id="47758-106">O cmdlet **Get-AzDataLakeGen2ChildItem** lista subdados e arquivos em um diretório ou Filesystem em uma conta de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="47758-106">The **Get-AzDataLakeGen2ChildItem** cmdlet lists sub directorys and files in a directory or Filesystem in an Azure storage account.</span></span>
<span data-ttu-id="47758-107">Esse cmdlet só funcionará se Namespace Hierárquico estiver habilitado para a conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="47758-107">This cmdlet only works if Hierarchical Namespace is enabled for the Storage account.</span></span> <span data-ttu-id="47758-108">Esse tipo de conta pode ser criada com o cmdlet "New-AzStorageAccount" com "-EnableHierarchicalNamespace $true".</span><span class="sxs-lookup"><span data-stu-id="47758-108">This kind of account can be created by run "New-AzStorageAccount" cmdlet with "-EnableHierarchicalNamespace $true".</span></span>

## <span data-ttu-id="47758-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="47758-109">EXAMPLES</span></span>

### <span data-ttu-id="47758-110">Exemplo 1: listar os sub-itens diretos de um sistema de arquivos</span><span class="sxs-lookup"><span data-stu-id="47758-110">Example 1: List the direct sub items from a Filesystem</span></span>
```
PS C:\>Get-AzDataLakeGen2ChildItem -FileSystem "filesystem1" 

   FileSystem Name: filesystem1

Path                 IsDirectory  Length          LastModified         Permissions  Owner                Group               
----                 -----------  ------          ------------         -----------  -----                -----               
dir1                 True                         2020-03-13 13:07:34Z rwxr-x---    $superuser           $superuser          
dir2                 True                         2020-03-23 09:28:36Z rwxr-x---    $superuser           $superuser
```

<span data-ttu-id="47758-111">Este comando lista os sub-itens diretos de um sistema de arquivos</span><span class="sxs-lookup"><span data-stu-id="47758-111">This command lists the direct sub items from a Filesystem</span></span>

### <span data-ttu-id="47758-112">Exemplo 2: Listar recursivamente de um diretório e buscar Propriedades/ACL</span><span class="sxs-lookup"><span data-stu-id="47758-112">Example 2: List recursively from a directory, and fetch Properties/ACL</span></span>
```
PS C:\>Get-AzDataLakeGen2ChildItem -FileSystem "filesystem1" -Path "dir1/" -Recurse -FetchProperty

   FileSystem Name: filesystem1

Path                 IsDirectory  Length          LastModified         Permissions  Owner                Group               
----                 -----------  ------          ------------         -----------  -----                -----               
dir1/dir3            True                         2020-03-23 09:34:31Z rwx---rwx    $superuser           $superuser          
dir1/file1           False        1024            2020-03-23 09:29:18Z rwx---rwx    $superuser           $superuser           
dir1/testfile_1K_0   False        1024            2020-03-23 09:29:21Z rw-r-----    $superuser           $superuser
```

<span data-ttu-id="47758-113">Este comando lista os sub-itens diretos de um sistema de arquivos</span><span class="sxs-lookup"><span data-stu-id="47758-113">This command lists the direct sub items from a Filesystem</span></span>

### <span data-ttu-id="47758-114">Exemplo 3: Listar itens recursivamente de um sistema de arquivos em vários lotes</span><span class="sxs-lookup"><span data-stu-id="47758-114">Example 3: List items recursively from a Filesystem in multiple batches</span></span>
```
PS C:\> $MaxReturn = 10000
PS C:\> $FileSystemName = "filesystem1"
PS C:\> $Total = 0
PS C:\> $Token = $Null
PS C:\> do
 {
     $items = Get-AzDataLakeGen2ChildItem -FileSystem $FileSystemName -Recurse -MaxCount $MaxReturn  -ContinuationToken $Token
     $Total += $items.Count
     if($items.Length -le 0) { Break;}
     $Token = $items[$items.Count -1].ContinuationToken;
 }
 While ($Token -ne $Null)
PS C:\> Echo "Total $Total items in Filesystem $FileSystemName"
```

<span data-ttu-id="47758-115">Este exemplo usa os *parâmetros MaxCount* e *ContinuationToken* para listar itens recursivamente de um sistema de arquivos em vários lotes.</span><span class="sxs-lookup"><span data-stu-id="47758-115">This example uses the *MaxCount* and *ContinuationToken* parameters to list items recursively from a Filesystem in multiple batches.</span></span>
<span data-ttu-id="47758-116">Os quatro primeiros comandos atribuem valores a variáveis a ser usadas no exemplo.</span><span class="sxs-lookup"><span data-stu-id="47758-116">The first four commands assign values to variables to use in the example.</span></span>
<span data-ttu-id="47758-117">O quinto comando especifica uma instrução **Do-While** que usa o cmdlet **Get-AzDataLakeGen2ChildItem** para listar itens.</span><span class="sxs-lookup"><span data-stu-id="47758-117">The fifth command specifies a **Do-While** statement that uses the **Get-AzDataLakeGen2ChildItem** cmdlet to list items.</span></span>
<span data-ttu-id="47758-118">A instrução inclui o token de continuação armazenado na variável $Token.</span><span class="sxs-lookup"><span data-stu-id="47758-118">The statement includes the continuation token stored in the $Token variable.</span></span>
<span data-ttu-id="47758-119">$Token altera o valor à medida que o loop é executado.</span><span class="sxs-lookup"><span data-stu-id="47758-119">$Token changes value as the loop runs.</span></span>
<span data-ttu-id="47758-120">O comando final usa o **comando Echo** para exibir o total.</span><span class="sxs-lookup"><span data-stu-id="47758-120">The final command uses the **Echo** command to display the total.</span></span>

## <span data-ttu-id="47758-121">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="47758-121">PARAMETERS</span></span>

### <span data-ttu-id="47758-122">-AsJob</span><span class="sxs-lookup"><span data-stu-id="47758-122">-AsJob</span></span>
<span data-ttu-id="47758-123">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="47758-123">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="47758-124">-Context</span><span class="sxs-lookup"><span data-stu-id="47758-124">-Context</span></span>
<span data-ttu-id="47758-125">Objeto de contexto de armazenamento do Azure</span><span class="sxs-lookup"><span data-stu-id="47758-125">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="47758-126">-ContinuationToken</span><span class="sxs-lookup"><span data-stu-id="47758-126">-ContinuationToken</span></span>
<span data-ttu-id="47758-127">Token de Continuação.</span><span class="sxs-lookup"><span data-stu-id="47758-127">Continuation Token.</span></span>

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

### <span data-ttu-id="47758-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47758-128">-DefaultProfile</span></span>
<span data-ttu-id="47758-129">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="47758-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="47758-130">-FetchProperty</span><span class="sxs-lookup"><span data-stu-id="47758-130">-FetchProperty</span></span>
<span data-ttu-id="47758-131">Busque as propriedades do item datalake e ACL.</span><span class="sxs-lookup"><span data-stu-id="47758-131">Fetch the datalake item properties and ACL.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: FetchPermission

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47758-132">-FileSystem</span><span class="sxs-lookup"><span data-stu-id="47758-132">-FileSystem</span></span>
<span data-ttu-id="47758-133">Nome do FileSystem</span><span class="sxs-lookup"><span data-stu-id="47758-133">FileSystem name</span></span>

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

### <span data-ttu-id="47758-134">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="47758-134">-MaxCount</span></span>
<span data-ttu-id="47758-135">A contagem máxima dos blobs que podem retornar.</span><span class="sxs-lookup"><span data-stu-id="47758-135">The max count of the blobs that can return.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47758-136">-OutputUserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="47758-136">-OutputUserPrincipalName</span></span>
<span data-ttu-id="47758-137">Se este parâmetro for speicify, os valores de identidade do usuário retornados nos campos proprietário e grupo de cada entrada de lista serão transformados de IDs de objeto do Azure Active Directory para Nomes principais de usuário.</span><span class="sxs-lookup"><span data-stu-id="47758-137">If speicify this parameter, the user identity values returned in the owner and group fields of each list entry will be transformed from Azure Active Directory Object IDs to User Principal Names.</span></span> <span data-ttu-id="47758-138">Se não especar esse parâmetro, os valores serão retornados como IDs de objeto do Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="47758-138">If not speicify this parameter, the values will be returned as Azure Active Directory Object IDs.</span></span> <span data-ttu-id="47758-139">Observe que as IDs de objeto do grupo e do aplicativo não são traduzidas porque não têm nomes amigáveis exclusivos.</span><span class="sxs-lookup"><span data-stu-id="47758-139">Note that group and application Object IDs are not translated because they do not have unique friendly names.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: UserPrincipalName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47758-140">-Path</span><span class="sxs-lookup"><span data-stu-id="47758-140">-Path</span></span>
<span data-ttu-id="47758-141">O caminho no sistema de arquivos especificado que deve ser recuperado.</span><span class="sxs-lookup"><span data-stu-id="47758-141">The path in the specified Filesystem that should be retrieved.</span></span>
<span data-ttu-id="47758-142">Deve ser um diretório, no formato 'directory1/directory2/'.</span><span class="sxs-lookup"><span data-stu-id="47758-142">Should be a directory, in the format 'directory1/directory2/'.</span></span>

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

### <span data-ttu-id="47758-143">-Recurse</span><span class="sxs-lookup"><span data-stu-id="47758-143">-Recurse</span></span>
<span data-ttu-id="47758-144">Indica se o Item Filho será recursivamente.</span><span class="sxs-lookup"><span data-stu-id="47758-144">Indicates if will recursively get the Child Item.</span></span>
<span data-ttu-id="47758-145">O padrão é false.</span><span class="sxs-lookup"><span data-stu-id="47758-145">The default is false.</span></span>

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

### <span data-ttu-id="47758-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47758-146">CommonParameters</span></span>
<span data-ttu-id="47758-147">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="47758-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47758-148">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="47758-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47758-149">INPUTS</span><span class="sxs-lookup"><span data-stu-id="47758-149">INPUTS</span></span>

### <span data-ttu-id="47758-150">System.String</span><span class="sxs-lookup"><span data-stu-id="47758-150">System.String</span></span>

### <span data-ttu-id="47758-151">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="47758-151">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="47758-152">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="47758-152">OUTPUTS</span></span>

### <span data-ttu-id="47758-153">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="47758-153">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item</span></span>

## <span data-ttu-id="47758-154">NOTES</span><span class="sxs-lookup"><span data-stu-id="47758-154">NOTES</span></span>

## <span data-ttu-id="47758-155">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="47758-155">RELATED LINKS</span></span>
