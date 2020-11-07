---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/update-azstorageblobserviceproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzStorageBlobServiceProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzStorageBlobServiceProperty.md
ms.openlocfilehash: b7d6299af3f56dd8f09c73171ab6630cbbb9bc96
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93942524"
---
# <span data-ttu-id="c094a-101">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="c094a-101">Update-AzStorageBlobServiceProperty</span></span>

## <span data-ttu-id="c094a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c094a-102">SYNOPSIS</span></span>
<span data-ttu-id="c094a-103">Modifica as propriedades do serviço do serviço blob de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="c094a-103">Modifies the service properties for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="c094a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c094a-104">SYNTAX</span></span>

### <span data-ttu-id="c094a-105">AccountName (padrão)</span><span class="sxs-lookup"><span data-stu-id="c094a-105">AccountName (Default)</span></span>
```
Update-AzStorageBlobServiceProperty [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-DefaultServiceVersion <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c094a-106">Accountobject</span><span class="sxs-lookup"><span data-stu-id="c094a-106">AccountObject</span></span>
```
Update-AzStorageBlobServiceProperty -StorageAccount <PSStorageAccount> [-DefaultServiceVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c094a-107">BlobServicePropertiesResourceId</span><span class="sxs-lookup"><span data-stu-id="c094a-107">BlobServicePropertiesResourceId</span></span>
```
Update-AzStorageBlobServiceProperty [-ResourceId] <String> [-DefaultServiceVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c094a-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c094a-108">DESCRIPTION</span></span>
<span data-ttu-id="c094a-109">O cmdlet **Update-AzStorageBlobServiceProperty** modifica as propriedades do serviço do serviço de blob do armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="c094a-109">The **Update-AzStorageBlobServiceProperty** cmdlet modifies the service properties for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="c094a-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c094a-110">EXAMPLES</span></span>

### <span data-ttu-id="c094a-111">Exemplo 1: definir o serviço de blob DefaultServiceVersion para 2018-03-28</span><span class="sxs-lookup"><span data-stu-id="c094a-111">Example 1: Set Blob service DefaultServiceVersion to 2018-03-28</span></span>
```
C:\PS> Update-AzStorageBlobServiceProperty -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -DefaultServiceVersion 2018-03-28 

StorageAccountName ResourceGroupName DefaultServiceVersion DeleteRetentionPolicy.Enabled DeleteRetentionPolicy.Days
------------------ ----------------- --------------------- ----------------------------- --------------------------
myresourcegroup    mystorageaccount  2018-03-28            False                                                   
```

<span data-ttu-id="c094a-112">Esse comando define o DefaultServiceVersion do serviço de BLOB para 2018-03-28.</span><span class="sxs-lookup"><span data-stu-id="c094a-112">This command sets the DefaultServiceVersion of Blob Service to 2018-03-28.</span></span>

## <span data-ttu-id="c094a-113">OS</span><span class="sxs-lookup"><span data-stu-id="c094a-113">PARAMETERS</span></span>

### <span data-ttu-id="c094a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c094a-114">-DefaultProfile</span></span>
<span data-ttu-id="c094a-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c094a-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c094a-116">-DefaultServiceVersion</span><span class="sxs-lookup"><span data-stu-id="c094a-116">-DefaultServiceVersion</span></span>
<span data-ttu-id="c094a-117">Versão de serviço padrão a ser definida</span><span class="sxs-lookup"><span data-stu-id="c094a-117">Default Service Version to Set</span></span>

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

### <span data-ttu-id="c094a-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c094a-118">-ResourceGroupName</span></span>
<span data-ttu-id="c094a-119">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="c094a-119">Resource Group Name.</span></span>

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

### <span data-ttu-id="c094a-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c094a-120">-ResourceId</span></span>
<span data-ttu-id="c094a-121">Insira uma ID de recurso da conta de armazenamento ou uma ID do recurso de propriedades do serviço BLOB.</span><span class="sxs-lookup"><span data-stu-id="c094a-121">Input a Storage account Resource Id, or a Blob service properties Resource Id.</span></span>

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

### <span data-ttu-id="c094a-122">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="c094a-122">-StorageAccount</span></span>
<span data-ttu-id="c094a-123">Objeto da conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="c094a-123">Storage account object</span></span>

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

### <span data-ttu-id="c094a-124">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="c094a-124">-StorageAccountName</span></span>
<span data-ttu-id="c094a-125">Nome da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="c094a-125">Storage Account Name.</span></span>

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

### <span data-ttu-id="c094a-126">-Confirme</span><span class="sxs-lookup"><span data-stu-id="c094a-126">-Confirm</span></span>
<span data-ttu-id="c094a-127">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c094a-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c094a-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c094a-128">-WhatIf</span></span>
<span data-ttu-id="c094a-129">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="c094a-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c094a-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c094a-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c094a-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c094a-131">CommonParameters</span></span>
<span data-ttu-id="c094a-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c094a-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c094a-133">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c094a-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c094a-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c094a-134">INPUTS</span></span>

### <span data-ttu-id="c094a-135">Microsoft. Azure. Commands. Management. Storage. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="c094a-135">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="c094a-136">System. String</span><span class="sxs-lookup"><span data-stu-id="c094a-136">System.String</span></span>

## <span data-ttu-id="c094a-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c094a-137">OUTPUTS</span></span>

### <span data-ttu-id="c094a-138">Microsoft. Azure. Commands. Management. Storage. Models. PSBlobServiceProperties</span><span class="sxs-lookup"><span data-stu-id="c094a-138">Microsoft.Azure.Commands.Management.Storage.Models.PSBlobServiceProperties</span></span>

## <span data-ttu-id="c094a-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c094a-139">NOTES</span></span>

## <span data-ttu-id="c094a-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c094a-140">RELATED LINKS</span></span>
