---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/get-azstorageblobserviceproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageBlobServiceProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageBlobServiceProperty.md
ms.openlocfilehash: 72e26a8fbb059db78fcdfa56721bed94e388ef55
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891985"
---
# <span data-ttu-id="38ff7-101">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="38ff7-101">Get-AzStorageBlobServiceProperty</span></span>

## <span data-ttu-id="38ff7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="38ff7-102">SYNOPSIS</span></span>
<span data-ttu-id="38ff7-103">Obtém propriedades de serviço para serviços blob de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="38ff7-103">Gets service properties for Azure Storage Blob services.</span></span>

## <span data-ttu-id="38ff7-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="38ff7-104">SYNTAX</span></span>

### <span data-ttu-id="38ff7-105">AccountName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="38ff7-105">AccountName (Default)</span></span>
```
Get-AzStorageBlobServiceProperty [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="38ff7-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="38ff7-106">AccountObject</span></span>
```
Get-AzStorageBlobServiceProperty -StorageAccount <PSStorageAccount> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="38ff7-107">BlobServicePropertiesResourceId</span><span class="sxs-lookup"><span data-stu-id="38ff7-107">BlobServicePropertiesResourceId</span></span>
```
Get-AzStorageBlobServiceProperty [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="38ff7-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="38ff7-108">DESCRIPTION</span></span>
<span data-ttu-id="38ff7-109">O cmdlet **Get-AzStorageBlobServiceProperty** obtém as propriedades de serviço dos serviços blob de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="38ff7-109">The **Get-AzStorageBlobServiceProperty** cmdlet gets the service properties for Azure Storage Blob services.</span></span>

## <span data-ttu-id="38ff7-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="38ff7-110">EXAMPLES</span></span>

### <span data-ttu-id="38ff7-111">Exemplo 1: Obter a propriedade de serviços blob de armazenamento do Azure de uma conta de armazenamento especificada</span><span class="sxs-lookup"><span data-stu-id="38ff7-111">Example 1: Get  Azure Storage Blob services property of a specified Storage Account</span></span>
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

<span data-ttu-id="38ff7-112">Este comando obtém a propriedade Blob services de uma Conta de Armazenamento especificada.</span><span class="sxs-lookup"><span data-stu-id="38ff7-112">This command gets the Blob services property of a specified Storage Account.</span></span>

## <span data-ttu-id="38ff7-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="38ff7-113">PARAMETERS</span></span>

### <span data-ttu-id="38ff7-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38ff7-114">-DefaultProfile</span></span>
<span data-ttu-id="38ff7-115">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="38ff7-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="38ff7-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="38ff7-116">-ResourceGroupName</span></span>
<span data-ttu-id="38ff7-117">Nome do Grupo de Recursos.</span><span class="sxs-lookup"><span data-stu-id="38ff7-117">Resource Group Name.</span></span>

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

### <span data-ttu-id="38ff7-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="38ff7-118">-ResourceId</span></span>
<span data-ttu-id="38ff7-119">ID do Recurso de Propriedades do Serviço blob.</span><span class="sxs-lookup"><span data-stu-id="38ff7-119">Blob Service Properties Resource Id.</span></span>

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

### <span data-ttu-id="38ff7-120">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="38ff7-120">-StorageAccount</span></span>
<span data-ttu-id="38ff7-121">Objeto de conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="38ff7-121">Storage account object</span></span>

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

### <span data-ttu-id="38ff7-122">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="38ff7-122">-StorageAccountName</span></span>
<span data-ttu-id="38ff7-123">Nome da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="38ff7-123">Storage Account Name.</span></span>

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

### <span data-ttu-id="38ff7-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38ff7-124">CommonParameters</span></span>
<span data-ttu-id="38ff7-125">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="38ff7-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38ff7-126">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="38ff7-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38ff7-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="38ff7-127">INPUTS</span></span>

### <span data-ttu-id="38ff7-128">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="38ff7-128">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="38ff7-129">System.String</span><span class="sxs-lookup"><span data-stu-id="38ff7-129">System.String</span></span>

## <span data-ttu-id="38ff7-130">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="38ff7-130">OUTPUTS</span></span>

### <span data-ttu-id="38ff7-131">Microsoft.Azure.Commands.Management.Storage.Models.PSBlobServiceProperties</span><span class="sxs-lookup"><span data-stu-id="38ff7-131">Microsoft.Azure.Commands.Management.Storage.Models.PSBlobServiceProperties</span></span>

## <span data-ttu-id="38ff7-132">NOTES</span><span class="sxs-lookup"><span data-stu-id="38ff7-132">NOTES</span></span>

## <span data-ttu-id="38ff7-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="38ff7-133">RELATED LINKS</span></span>
