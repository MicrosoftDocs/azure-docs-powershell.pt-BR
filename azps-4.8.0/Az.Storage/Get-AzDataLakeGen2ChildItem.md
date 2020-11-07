---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azdatalakegen2childitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzDataLakeGen2ChildItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzDataLakeGen2ChildItem.md
ms.openlocfilehash: 9160eabf2492969ad7fa3916791854abd4ef6c44
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "93956130"
---
# <span data-ttu-id="773e0-101">Get-AzDataLakeGen2ChildItem</span><span class="sxs-lookup"><span data-stu-id="773e0-101">Get-AzDataLakeGen2ChildItem</span></span>

## <span data-ttu-id="773e0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="773e0-102">SYNOPSIS</span></span>
<span data-ttu-id="773e0-103">Lista subdiretórios e arquivos de um diretório ou raiz do sistema de arquivos.</span><span class="sxs-lookup"><span data-stu-id="773e0-103">Lists sub directorys and files from a directory or filesystem root.</span></span>

## <span data-ttu-id="773e0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="773e0-104">SYNTAX</span></span>

```
Get-AzDataLakeGen2ChildItem [-FileSystem] <String> [[-Path] <String>] [-FetchProperty] [-Recurse]
 [-MaxCount <Int32>] [-ContinuationToken <String>] [-AsJob] [-OutputUserPrincipalName]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="773e0-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="773e0-105">DESCRIPTION</span></span>
<span data-ttu-id="773e0-106">O cmdlet **Get-AzDataLakeGen2ChildItem** lista subdiretórios e arquivos em um diretório ou sistema de arquivos em uma conta de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="773e0-106">The **Get-AzDataLakeGen2ChildItem** cmdlet lists sub directorys and files in a directory or Filesystem in an Azure storage account.</span></span>
<span data-ttu-id="773e0-107">Este cmdlet só funcionará se o namespace hierárquico estiver habilitado para a conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="773e0-107">This cmdlet only works if Hierarchical Namespace is enabled for the Storage account.</span></span> <span data-ttu-id="773e0-108">Esse tipo de conta pode ser criado por meio da execução do cmdlet "New-AzStorageAccount" com "-EnableHierarchicalNamespace $true".</span><span class="sxs-lookup"><span data-stu-id="773e0-108">This kind of account can be created by run "New-AzStorageAccount" cmdlet with "-EnableHierarchicalNamespace $true".</span></span>

## <span data-ttu-id="773e0-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="773e0-109">EXAMPLES</span></span>

### <span data-ttu-id="773e0-110">Exemplo 1: listar os subitens diretos de um sistema de arquivos</span><span class="sxs-lookup"><span data-stu-id="773e0-110">Example 1: List the direct sub items from a Filesystem</span></span>
```
PS C:\>Get-AzDataLakeGen2ChildItem -FileSystem "filesystem1" 

   FileSystem Name: filesystem1

Path                 IsDirectory  Length          LastModified         Permissions  Owner                Group               
----                 -----------  ------          ------------         -----------  -----                -----               
dir1                 True                         2020-03-13 13:07:34Z rwxr-x---    $superuser           $superuser          
dir2                 True                         2020-03-23 09:28:36Z rwxr-x---    $superuser           $superuser
```

<span data-ttu-id="773e0-111">Esse comando lista os subitens diretos de um sistema de arquivos</span><span class="sxs-lookup"><span data-stu-id="773e0-111">This command lists the direct sub items from a Filesystem</span></span>

### <span data-ttu-id="773e0-112">Exemplo 2: lista recursivamente de um diretório e busca Propriedades/ACL</span><span class="sxs-lookup"><span data-stu-id="773e0-112">Example 2: List recursively from a directory, and fetch Properties/ACL</span></span>
```
PS C:\>Get-AzDataLakeGen2ChildItem -FileSystem "filesystem1" -Path "dir1/" -Recurse -FetchProperty

   FileSystem Name: filesystem1

Path                 IsDirectory  Length          LastModified         Permissions  Owner                Group               
----                 -----------  ------          ------------         -----------  -----                -----               
dir1/dir3            True                         2020-03-23 09:34:31Z rwx---rwx    $superuser           $superuser          
dir1/file1           False        1024            2020-03-23 09:29:18Z rwx---rwx    $superuser           $superuser           
dir1/testfile_1K_0   False        1024            2020-03-23 09:29:21Z rw-r-----    $superuser           $superuser
```

<span data-ttu-id="773e0-113">Esse comando lista os subitens diretos de um sistema de arquivos</span><span class="sxs-lookup"><span data-stu-id="773e0-113">This command lists the direct sub items from a Filesystem</span></span>

### <span data-ttu-id="773e0-114">Exemplo 3: Listar itens recursivamente de um sistema de arquivos em vários lotes</span><span class="sxs-lookup"><span data-stu-id="773e0-114">Example 3: List items recursively from a Filesystem in multiple batches</span></span>
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

<span data-ttu-id="773e0-115">Este exemplo usa os parâmetros *MaxCount* e *ContinuationToken* para listar itens recursivamente de um sistema de arquivos em vários lotes.</span><span class="sxs-lookup"><span data-stu-id="773e0-115">This example uses the *MaxCount* and *ContinuationToken* parameters to list items recursively from a Filesystem in multiple batches.</span></span>
<span data-ttu-id="773e0-116">Os quatro primeiros comandos atribuem valores a variáveis a serem usadas no exemplo.</span><span class="sxs-lookup"><span data-stu-id="773e0-116">The first four commands assign values to variables to use in the example.</span></span>
<span data-ttu-id="773e0-117">O quinto comando especifica uma instrução **do while** que usa o cmdlet **Get-AzDataLakeGen2ChildItem** para listar itens.</span><span class="sxs-lookup"><span data-stu-id="773e0-117">The fifth command specifies a **Do-While** statement that uses the **Get-AzDataLakeGen2ChildItem** cmdlet to list items.</span></span>
<span data-ttu-id="773e0-118">A instrução inclui o token de continuação armazenado na variável $Token.</span><span class="sxs-lookup"><span data-stu-id="773e0-118">The statement includes the continuation token stored in the $Token variable.</span></span>
<span data-ttu-id="773e0-119">$Token altera o valor conforme o loop é executado.</span><span class="sxs-lookup"><span data-stu-id="773e0-119">$Token changes value as the loop runs.</span></span>
<span data-ttu-id="773e0-120">O comando final usa o comando **Echo** para exibir o total.</span><span class="sxs-lookup"><span data-stu-id="773e0-120">The final command uses the **Echo** command to display the total.</span></span>

## <span data-ttu-id="773e0-121">OS</span><span class="sxs-lookup"><span data-stu-id="773e0-121">PARAMETERS</span></span>

### <span data-ttu-id="773e0-122">-AsJob</span><span class="sxs-lookup"><span data-stu-id="773e0-122">-AsJob</span></span>
<span data-ttu-id="773e0-123">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="773e0-123">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="773e0-124">-Contexto</span><span class="sxs-lookup"><span data-stu-id="773e0-124">-Context</span></span>
<span data-ttu-id="773e0-125">Objeto de contexto de armazenamento do Azure</span><span class="sxs-lookup"><span data-stu-id="773e0-125">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="773e0-126">-ContinuationToken</span><span class="sxs-lookup"><span data-stu-id="773e0-126">-ContinuationToken</span></span>
<span data-ttu-id="773e0-127">Token de continuação.</span><span class="sxs-lookup"><span data-stu-id="773e0-127">Continuation Token.</span></span>

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

### <span data-ttu-id="773e0-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="773e0-128">-DefaultProfile</span></span>
<span data-ttu-id="773e0-129">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="773e0-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="773e0-130">-Fetchproperty</span><span class="sxs-lookup"><span data-stu-id="773e0-130">-FetchProperty</span></span>
<span data-ttu-id="773e0-131">Busque as propriedades e a ACL do item datalake.</span><span class="sxs-lookup"><span data-stu-id="773e0-131">Fetch the datalake item properties and ACL.</span></span>

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

### <span data-ttu-id="773e0-132">-FileSystem</span><span class="sxs-lookup"><span data-stu-id="773e0-132">-FileSystem</span></span>
<span data-ttu-id="773e0-133">Nome do sistema de arquivos</span><span class="sxs-lookup"><span data-stu-id="773e0-133">FileSystem name</span></span>

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

### <span data-ttu-id="773e0-134">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="773e0-134">-MaxCount</span></span>
<span data-ttu-id="773e0-135">A contagem máx dos BLOBs que podem retornar.</span><span class="sxs-lookup"><span data-stu-id="773e0-135">The max count of the blobs that can return.</span></span>

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

### <span data-ttu-id="773e0-136">-OutputUserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="773e0-136">-OutputUserPrincipalName</span></span>
<span data-ttu-id="773e0-137">Se speicify esse parâmetro, os valores de identidade do usuário retornados nos campos Owner e Group de cada entrada de lista serão transformados de IDs de objeto do Azure Active Directory para nomes de usuário principal.</span><span class="sxs-lookup"><span data-stu-id="773e0-137">If speicify this parameter, the user identity values returned in the owner and group fields of each list entry will be transformed from Azure Active Directory Object IDs to User Principal Names.</span></span> <span data-ttu-id="773e0-138">Se não speicify esse parâmetro, os valores serão retornados como IDs de objeto do Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="773e0-138">If not speicify this parameter, the values will be returned as Azure Active Directory Object IDs.</span></span> <span data-ttu-id="773e0-139">Observe que as IDs de objeto de grupo e aplicativo não são traduzidas porque elas não têm nomes amigáveis exclusivos.</span><span class="sxs-lookup"><span data-stu-id="773e0-139">Note that group and application Object IDs are not translated because they do not have unique friendly names.</span></span>

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

### <span data-ttu-id="773e0-140">-Caminho</span><span class="sxs-lookup"><span data-stu-id="773e0-140">-Path</span></span>
<span data-ttu-id="773e0-141">O caminho no sistema de arquivos especificado que deve ser recuperado.</span><span class="sxs-lookup"><span data-stu-id="773e0-141">The path in the specified Filesystem that should be retrieved.</span></span>
<span data-ttu-id="773e0-142">Deve ser um diretório, no formato ' directory1/directory2/'.</span><span class="sxs-lookup"><span data-stu-id="773e0-142">Should be a directory, in the format 'directory1/directory2/'.</span></span>

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

### <span data-ttu-id="773e0-143">-Recurse</span><span class="sxs-lookup"><span data-stu-id="773e0-143">-Recurse</span></span>
<span data-ttu-id="773e0-144">Indica se o item filho será obtido recursivamente.</span><span class="sxs-lookup"><span data-stu-id="773e0-144">Indicates if will recursively get the Child Item.</span></span>
<span data-ttu-id="773e0-145">O padrão é falso.</span><span class="sxs-lookup"><span data-stu-id="773e0-145">The default is false.</span></span>

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

### <span data-ttu-id="773e0-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="773e0-146">CommonParameters</span></span>
<span data-ttu-id="773e0-147">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="773e0-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="773e0-148">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="773e0-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="773e0-149">SENSORES</span><span class="sxs-lookup"><span data-stu-id="773e0-149">INPUTS</span></span>

### <span data-ttu-id="773e0-150">System. String</span><span class="sxs-lookup"><span data-stu-id="773e0-150">System.String</span></span>

### <span data-ttu-id="773e0-151">Microsoft. Azure. Commands. Common. Authentication. Abstractings. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="773e0-151">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="773e0-152">EXIBE</span><span class="sxs-lookup"><span data-stu-id="773e0-152">OUTPUTS</span></span>

### <span data-ttu-id="773e0-153">Microsoft. WindowsAzure. Commands. Common. Storage. ResourceModel. AzureDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="773e0-153">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item</span></span>

## <span data-ttu-id="773e0-154">INFORMA</span><span class="sxs-lookup"><span data-stu-id="773e0-154">NOTES</span></span>

## <span data-ttu-id="773e0-155">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="773e0-155">RELATED LINKS</span></span>
