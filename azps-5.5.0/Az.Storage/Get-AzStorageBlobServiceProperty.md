---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageblobserviceproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageBlobServiceProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageBlobServiceProperty.md
ms.openlocfilehash: 7cdef2f35180712d0751149a85e4a422a868c389
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115669"
---
# <span data-ttu-id="b45a6-101">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="b45a6-101">Get-AzStorageBlobServiceProperty</span></span>

## <span data-ttu-id="b45a6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b45a6-102">SYNOPSIS</span></span>
<span data-ttu-id="b45a6-103">Obtém propriedades de serviço para os serviços de Blob de Armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="b45a6-103">Gets service properties for Azure Storage Blob services.</span></span>

## <span data-ttu-id="b45a6-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b45a6-104">SYNTAX</span></span>

### <span data-ttu-id="b45a6-105">Nomeda Conta (Padrão)</span><span class="sxs-lookup"><span data-stu-id="b45a6-105">AccountName (Default)</span></span>
```
Get-AzStorageBlobServiceProperty [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b45a6-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="b45a6-106">AccountObject</span></span>
```
Get-AzStorageBlobServiceProperty -StorageAccount <PSStorageAccount> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b45a6-107">BlobServicePropertiesResourceId</span><span class="sxs-lookup"><span data-stu-id="b45a6-107">BlobServicePropertiesResourceId</span></span>
```
Get-AzStorageBlobServiceProperty [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b45a6-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="b45a6-108">DESCRIPTION</span></span>
<span data-ttu-id="b45a6-109">O cmdlet **Get-AzStorageBserviceProperty** obtém as propriedades de serviço dos serviços de Blob de Armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="b45a6-109">The **Get-AzStorageBlobServiceProperty** cmdlet gets the service properties for Azure Storage Blob services.</span></span>

## <span data-ttu-id="b45a6-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="b45a6-110">EXAMPLES</span></span>

### <span data-ttu-id="b45a6-111">Exemplo 1: Obter a propriedade serviços de Blob de Armazenamento do Azure de uma Conta de Armazenamento especificada</span><span class="sxs-lookup"><span data-stu-id="b45a6-111">Example 1: Get  Azure Storage Blob services property of a specified Storage Account</span></span>
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

<span data-ttu-id="b45a6-112">Esse comando obtém a propriedade de serviços Blob de uma Conta de Armazenamento especificada.</span><span class="sxs-lookup"><span data-stu-id="b45a6-112">This command gets the Blob services property of a specified Storage Account.</span></span>

## <span data-ttu-id="b45a6-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b45a6-113">PARAMETERS</span></span>

### <span data-ttu-id="b45a6-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b45a6-114">-DefaultProfile</span></span>
<span data-ttu-id="b45a6-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b45a6-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b45a6-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b45a6-116">-ResourceGroupName</span></span>
<span data-ttu-id="b45a6-117">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="b45a6-117">Resource Group Name.</span></span>

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

### <span data-ttu-id="b45a6-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b45a6-118">-ResourceId</span></span>
<span data-ttu-id="b45a6-119">Blob Service Properties Resource Id.</span><span class="sxs-lookup"><span data-stu-id="b45a6-119">Blob Service Properties Resource Id.</span></span>

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

### <span data-ttu-id="b45a6-120">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="b45a6-120">-StorageAccount</span></span>
<span data-ttu-id="b45a6-121">Objeto de conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="b45a6-121">Storage account object</span></span>

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

### <span data-ttu-id="b45a6-122">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="b45a6-122">-StorageAccountName</span></span>
<span data-ttu-id="b45a6-123">Nome da Conta de Armazenamento.</span><span class="sxs-lookup"><span data-stu-id="b45a6-123">Storage Account Name.</span></span>

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

### <span data-ttu-id="b45a6-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b45a6-124">CommonParameters</span></span>
<span data-ttu-id="b45a6-125">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b45a6-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b45a6-126">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b45a6-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b45a6-127">Entradas</span><span class="sxs-lookup"><span data-stu-id="b45a6-127">INPUTS</span></span>

### <span data-ttu-id="b45a6-128">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="b45a6-128">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="b45a6-129">System.String</span><span class="sxs-lookup"><span data-stu-id="b45a6-129">System.String</span></span>

## <span data-ttu-id="b45a6-130">Saídas</span><span class="sxs-lookup"><span data-stu-id="b45a6-130">OUTPUTS</span></span>

### <span data-ttu-id="b45a6-131">Microsoft.Azure.Commands.Management.Storage.Models.PSBserviceProperties</span><span class="sxs-lookup"><span data-stu-id="b45a6-131">Microsoft.Azure.Commands.Management.Storage.Models.PSBlobServiceProperties</span></span>

## <span data-ttu-id="b45a6-132">Notas</span><span class="sxs-lookup"><span data-stu-id="b45a6-132">NOTES</span></span>

## <span data-ttu-id="b45a6-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b45a6-133">RELATED LINKS</span></span>
