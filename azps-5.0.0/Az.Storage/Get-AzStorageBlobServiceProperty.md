---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageblobserviceproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageBlobServiceProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageBlobServiceProperty.md
ms.openlocfilehash: 7cdef2f35180712d0751149a85e4a422a868c389
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94125331"
---
# <span data-ttu-id="04797-101">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="04797-101">Get-AzStorageBlobServiceProperty</span></span>

## <span data-ttu-id="04797-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="04797-102">SYNOPSIS</span></span>
<span data-ttu-id="04797-103">Obtém as propriedades de serviço dos serviços de blob do repositório do Azure.</span><span class="sxs-lookup"><span data-stu-id="04797-103">Gets service properties for Azure Storage Blob services.</span></span>

## <span data-ttu-id="04797-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="04797-104">SYNTAX</span></span>

### <span data-ttu-id="04797-105">AccountName (padrão)</span><span class="sxs-lookup"><span data-stu-id="04797-105">AccountName (Default)</span></span>
```
Get-AzStorageBlobServiceProperty [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="04797-106">Accountobject</span><span class="sxs-lookup"><span data-stu-id="04797-106">AccountObject</span></span>
```
Get-AzStorageBlobServiceProperty -StorageAccount <PSStorageAccount> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="04797-107">BlobServicePropertiesResourceId</span><span class="sxs-lookup"><span data-stu-id="04797-107">BlobServicePropertiesResourceId</span></span>
```
Get-AzStorageBlobServiceProperty [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="04797-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="04797-108">DESCRIPTION</span></span>
<span data-ttu-id="04797-109">O cmdlet **Get-AzStorageBlobServiceProperty** Obtém as propriedades de serviço dos serviços de blob do repositório do Azure.</span><span class="sxs-lookup"><span data-stu-id="04797-109">The **Get-AzStorageBlobServiceProperty** cmdlet gets the service properties for Azure Storage Blob services.</span></span>

## <span data-ttu-id="04797-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="04797-110">EXAMPLES</span></span>

### <span data-ttu-id="04797-111">Exemplo 1: obter a propriedade serviços de blob do armazenamento do Azure de uma conta de armazenamento especificada</span><span class="sxs-lookup"><span data-stu-id="04797-111">Example 1: Get  Azure Storage Blob services property of a specified Storage Account</span></span>
```powershell
PS C:\> Get-AzStorageBlobServiceProperty -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount"

StorageAccountName            : mystorageaccount
ResourceGroupName             : myresourcegroup
DefaultServiceVersion         : 
DeleteRetentionPolicy.Enabled : False
DeleteRetentionPolicy.Days    : 
RestorePolicy.Enabled         : 
RestorePolicy.Days            : 
ChangeFeed                    : True
IsVersioningEnabled           : True
```

<span data-ttu-id="04797-112">Esse comando obtém a propriedade serviços de blob de uma conta de armazenamento especificada.</span><span class="sxs-lookup"><span data-stu-id="04797-112">This command gets the Blob services property of a specified Storage Account.</span></span>

## <span data-ttu-id="04797-113">OS</span><span class="sxs-lookup"><span data-stu-id="04797-113">PARAMETERS</span></span>

### <span data-ttu-id="04797-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04797-114">-DefaultProfile</span></span>
<span data-ttu-id="04797-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="04797-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="04797-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="04797-116">-ResourceGroupName</span></span>
<span data-ttu-id="04797-117">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="04797-117">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04797-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="04797-118">-ResourceId</span></span>
<span data-ttu-id="04797-119">ID do recurso de propriedades do serviço BLOB.</span><span class="sxs-lookup"><span data-stu-id="04797-119">Blob Service Properties Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: BlobServicePropertiesResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="04797-120">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="04797-120">-StorageAccount</span></span>
<span data-ttu-id="04797-121">Objeto da conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="04797-121">Storage account object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount
Parameter Sets: AccountObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="04797-122">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="04797-122">-StorageAccountName</span></span>
<span data-ttu-id="04797-123">Nome da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="04797-123">Storage Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases: AccountName, Name

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04797-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04797-124">CommonParameters</span></span>
<span data-ttu-id="04797-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="04797-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04797-126">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="04797-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04797-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="04797-127">INPUTS</span></span>

### <span data-ttu-id="04797-128">Microsoft. Azure. Commands. Management. Storage. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="04797-128">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="04797-129">System. String</span><span class="sxs-lookup"><span data-stu-id="04797-129">System.String</span></span>

## <span data-ttu-id="04797-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="04797-130">OUTPUTS</span></span>

### <span data-ttu-id="04797-131">Microsoft. Azure. Commands. Management. Storage. Models. PSBlobServiceProperties</span><span class="sxs-lookup"><span data-stu-id="04797-131">Microsoft.Azure.Commands.Management.Storage.Models.PSBlobServiceProperties</span></span>

## <span data-ttu-id="04797-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="04797-132">NOTES</span></span>

## <span data-ttu-id="04797-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="04797-133">RELATED LINKS</span></span>
