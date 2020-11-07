---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azdatalakegen2item
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzDataLakeGen2Item.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzDataLakeGen2Item.md
ms.openlocfilehash: edd65cc10ca90592225b6b9deb04167202510a2e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "93956131"
---
# <span data-ttu-id="eb3c1-101">Get-AzDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="eb3c1-101">Get-AzDataLakeGen2Item</span></span>

## <span data-ttu-id="eb3c1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="eb3c1-102">SYNOPSIS</span></span>
<span data-ttu-id="eb3c1-103">Obtém os detalhes de um arquivo ou diretório em um sistema de arquivos.</span><span class="sxs-lookup"><span data-stu-id="eb3c1-103">Gets the details of a file or directory in a filesystem.</span></span>

## <span data-ttu-id="eb3c1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="eb3c1-104">SYNTAX</span></span>

```
Get-AzDataLakeGen2Item [-FileSystem] <String> [-Path <String>] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="eb3c1-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="eb3c1-105">DESCRIPTION</span></span>
<span data-ttu-id="eb3c1-106">O cmdlet **Get-AzDataLakeGen2Item** Obtém os detalhes de um arquivo ou diretório em um sistema de arquivos em uma conta de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="eb3c1-106">The **Get-AzDataLakeGen2Item** cmdlet gets the details of a file or directory in a Filesystem in an Azure storage account.</span></span>
<span data-ttu-id="eb3c1-107">Este cmdlet só funcionará se o namespace hierárquico estiver habilitado para a conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="eb3c1-107">This cmdlet only works if Hierarchical Namespace is enabled for the Storage account.</span></span> <span data-ttu-id="eb3c1-108">Esse tipo de conta pode ser criado por meio da execução do cmdlet "New-AzStorageAccount" com "-EnableHierarchicalNamespace $true".</span><span class="sxs-lookup"><span data-stu-id="eb3c1-108">This kind of account can be created by run "New-AzStorageAccount" cmdlet with "-EnableHierarchicalNamespace $true".</span></span>

## <span data-ttu-id="eb3c1-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="eb3c1-109">EXAMPLES</span></span>

### <span data-ttu-id="eb3c1-110">Exemplo 1: obter um diretório de um sistema de arquivos e mostrar os detalhes</span><span class="sxs-lookup"><span data-stu-id="eb3c1-110">Example 1: Get a directory from a Filesystem, and show the details</span></span>
```
PS C:\> $dir1 = Get-AzDataLakeGen2Item -FileSystem "filesystem1" -Path "dir1/"
PS C:\> $dir1

   FileSystem Name: filesystem1

Path                 IsDirectory  Length          LastModified         Permissions  Owner                Group               
----                 -----------  ------          ------------         -----------  -----                -----               
dir1                 True                         2020-03-23 09:15:56Z rwx---rwx    $superuser           $superuser     
 
PS C:\WINDOWS\system32> $dir1.ACL

DefaultScope AccessControlType EntityId Permissions
------------ ----------------- -------- -----------
False        User                       rwx        
False        Group                      ---        
False        Other                      rwx      

PS C:\WINDOWS\system32> $dir1.Permissions

Owner        : Execute, Write, Read
Group        : None
Other        : Execute, Write, Read
StickyBit    : False
ExtendedAcls : False

PS C:\WINDOWS\system32> $dir1.Properties.Metadata

Key          Value 
---          ----- 
hdi_isfolder true  
tag1         value1
tag2         value2

PS C:\WINDOWS\system32> $dir1.Properties

LastModified          : 3/23/2020 9:15:56 AM +00:00
CreatedOn             : 3/23/2020 9:15:56 AM +00:00
Metadata              : {[hdi_isfolder, true], [tag1, value1], [tag2, value2]}
CopyCompletedOn       : 1/1/0001 12:00:00 AM +00:00
CopyStatusDescription : 
CopyId                : 
CopyProgress          : 
CopySource            : 
CopyStatus            : Pending
IsIncrementalCopy     : False
LeaseDuration         : Infinite
LeaseState            : Available
LeaseStatus           : Unlocked
ContentLength         : 0
ContentType           : application/octet-stream
ETag                  : "0x8D7CF0ACBA35FA8"
ContentHash           : 
ContentEncoding       : UDF12
ContentDisposition    : 
ContentLanguage       : 
CacheControl          : READ
AcceptRanges          : bytes
IsServerEncrypted     : True
EncryptionKeySha256   : 
AccessTier            : Cool
ArchiveStatus         : 
AccessTierChangedOn   : 1/1/0001 12:00:00 AM +00:00
```

<span data-ttu-id="eb3c1-111">Esse comando obtém um diretório de um sistema de arquivos e mostra os detalhes.</span><span class="sxs-lookup"><span data-stu-id="eb3c1-111">This command gets a directory from a Filesystem, and show the details.</span></span>

### <span data-ttu-id="eb3c1-112">Exemplo 2: obter um arquivo de um sistema de arquivos</span><span class="sxs-lookup"><span data-stu-id="eb3c1-112">Example 2: Get a file from a Filesystem</span></span>
```
PS C:\> Get-AzDataLakeGen2Item -FileSystem "filesystem1" -Path "dir1/file1"

   FileSystem Name: filesystem1

Path                 IsDirectory  Length          LastModified         Permissions  Owner                Group               
----                 -----------  ------          ------------         -----------  -----                -----               
dir1/file1           False        1024            2020-03-23 09:20:37Z rwx---rwx    $superuser           $superuser
```

<span data-ttu-id="eb3c1-113">Esse comando obtém os detalhes de um arquivo de um sistema de arquivos.</span><span class="sxs-lookup"><span data-stu-id="eb3c1-113">This command gets the details of a file from a Filesystem.</span></span> 

## <span data-ttu-id="eb3c1-114">OS</span><span class="sxs-lookup"><span data-stu-id="eb3c1-114">PARAMETERS</span></span>

### <span data-ttu-id="eb3c1-115">-Contexto</span><span class="sxs-lookup"><span data-stu-id="eb3c1-115">-Context</span></span>
<span data-ttu-id="eb3c1-116">Objeto de contexto de armazenamento do Azure</span><span class="sxs-lookup"><span data-stu-id="eb3c1-116">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="eb3c1-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb3c1-117">-DefaultProfile</span></span>
<span data-ttu-id="eb3c1-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="eb3c1-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eb3c1-119">-FileSystem</span><span class="sxs-lookup"><span data-stu-id="eb3c1-119">-FileSystem</span></span>
<span data-ttu-id="eb3c1-120">Nome do sistema de arquivos</span><span class="sxs-lookup"><span data-stu-id="eb3c1-120">FileSystem name</span></span>

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

### <span data-ttu-id="eb3c1-121">-Caminho</span><span class="sxs-lookup"><span data-stu-id="eb3c1-121">-Path</span></span>
<span data-ttu-id="eb3c1-122">O caminho no sistema de arquivos especificado que deve ser recuperado.</span><span class="sxs-lookup"><span data-stu-id="eb3c1-122">The path in the specified Filesystem that should be retrieved.</span></span>
<span data-ttu-id="eb3c1-123">Pode ser um arquivo ou diretório no formato "Directory/file.txt" ou "directory1/directory2/".</span><span class="sxs-lookup"><span data-stu-id="eb3c1-123">Can be a file or directory In the format 'directory/file.txt' or 'directory1/directory2/'.</span></span>
<span data-ttu-id="eb3c1-124">Não especifique esse parâmetro para obter o diretório raiz do sistema de arquivos.</span><span class="sxs-lookup"><span data-stu-id="eb3c1-124">Not specify this parameter to get the root directory of the Filesystem.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="eb3c1-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb3c1-125">CommonParameters</span></span>
<span data-ttu-id="eb3c1-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eb3c1-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb3c1-127">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eb3c1-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb3c1-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="eb3c1-128">INPUTS</span></span>

### <span data-ttu-id="eb3c1-129">System. String</span><span class="sxs-lookup"><span data-stu-id="eb3c1-129">System.String</span></span>

### <span data-ttu-id="eb3c1-130">Microsoft. Azure. Commands. Common. Authentication. Abstractings. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="eb3c1-130">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="eb3c1-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="eb3c1-131">OUTPUTS</span></span>

### <span data-ttu-id="eb3c1-132">Microsoft. WindowsAzure. Commands. Common. Storage. ResourceModel. AzureDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="eb3c1-132">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item</span></span>

## <span data-ttu-id="eb3c1-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="eb3c1-133">NOTES</span></span>

## <span data-ttu-id="eb3c1-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="eb3c1-134">RELATED LINKS</span></span>
