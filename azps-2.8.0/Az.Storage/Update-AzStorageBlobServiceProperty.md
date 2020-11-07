---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/update-azstorageblobserviceproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzStorageBlobServiceProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzStorageBlobServiceProperty.md
ms.openlocfilehash: 195bc966bb47bf921eb0150272cfb9af6d73c63a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93774039"
---
# <span data-ttu-id="8dd73-101">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="8dd73-101">Update-AzStorageBlobServiceProperty</span></span>

## <span data-ttu-id="8dd73-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8dd73-102">SYNOPSIS</span></span>
<span data-ttu-id="8dd73-103">Modifica as propriedades do serviço do serviço blob de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="8dd73-103">Modifies the service properties for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="8dd73-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8dd73-104">SYNTAX</span></span>

### <span data-ttu-id="8dd73-105">AccountName (padrão)</span><span class="sxs-lookup"><span data-stu-id="8dd73-105">AccountName (Default)</span></span>
```
Update-AzStorageBlobServiceProperty [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-DefaultServiceVersion <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8dd73-106">Accountobject</span><span class="sxs-lookup"><span data-stu-id="8dd73-106">AccountObject</span></span>
```
Update-AzStorageBlobServiceProperty -StorageAccount <PSStorageAccount> [-DefaultServiceVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8dd73-107">BlobServicePropertiesResourceId</span><span class="sxs-lookup"><span data-stu-id="8dd73-107">BlobServicePropertiesResourceId</span></span>
```
Update-AzStorageBlobServiceProperty [-ResourceId] <String> [-DefaultServiceVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8dd73-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8dd73-108">DESCRIPTION</span></span>
<span data-ttu-id="8dd73-109">O cmdlet **Update-AzStorageBlobServiceProperty** modifica as propriedades do serviço do serviço de blob do armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="8dd73-109">The **Update-AzStorageBlobServiceProperty** cmdlet modifies the service properties for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="8dd73-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8dd73-110">EXAMPLES</span></span>

### <span data-ttu-id="8dd73-111">Exemplo 1: definir o serviço de blob DefaultServiceVersion para 2018-03-28</span><span class="sxs-lookup"><span data-stu-id="8dd73-111">Example 1: Set Blob service DefaultServiceVersion to 2018-03-28</span></span>
```
C:\PS> Update-AzStorageBlobServiceProperty -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -DefaultServiceVersion 2018-03-28 

StorageAccountName ResourceGroupName DefaultServiceVersion DeleteRetentionPolicy.Enabled DeleteRetentionPolicy.Days
------------------ ----------------- --------------------- ----------------------------- --------------------------
myresourcegroup    mystorageaccount  2018-03-28            False
```

<span data-ttu-id="8dd73-112">Esse comando define o DefaultServiceVersion do serviço de BLOB para 2018-03-28.</span><span class="sxs-lookup"><span data-stu-id="8dd73-112">This command sets the DefaultServiceVersion of Blob Service to 2018-03-28.</span></span>

## <span data-ttu-id="8dd73-113">OS</span><span class="sxs-lookup"><span data-stu-id="8dd73-113">PARAMETERS</span></span>

### <span data-ttu-id="8dd73-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8dd73-114">-DefaultProfile</span></span>
<span data-ttu-id="8dd73-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8dd73-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8dd73-116">-DefaultServiceVersion</span><span class="sxs-lookup"><span data-stu-id="8dd73-116">-DefaultServiceVersion</span></span>
<span data-ttu-id="8dd73-117">Versão de serviço padrão a ser definida</span><span class="sxs-lookup"><span data-stu-id="8dd73-117">Default Service Version to Set</span></span>

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

### <span data-ttu-id="8dd73-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8dd73-118">-ResourceGroupName</span></span>
<span data-ttu-id="8dd73-119">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="8dd73-119">Resource Group Name.</span></span>

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

### <span data-ttu-id="8dd73-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8dd73-120">-ResourceId</span></span>
<span data-ttu-id="8dd73-121">Insira uma ID de recurso da conta de armazenamento ou uma ID do recurso de propriedades do serviço BLOB.</span><span class="sxs-lookup"><span data-stu-id="8dd73-121">Input a Storage account Resource Id, or a Blob service properties Resource Id.</span></span>

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

### <span data-ttu-id="8dd73-122">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="8dd73-122">-StorageAccount</span></span>
<span data-ttu-id="8dd73-123">Objeto da conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="8dd73-123">Storage account object</span></span>

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

### <span data-ttu-id="8dd73-124">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="8dd73-124">-StorageAccountName</span></span>
<span data-ttu-id="8dd73-125">Nome da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="8dd73-125">Storage Account Name.</span></span>

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

### <span data-ttu-id="8dd73-126">-Confirme</span><span class="sxs-lookup"><span data-stu-id="8dd73-126">-Confirm</span></span>
<span data-ttu-id="8dd73-127">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8dd73-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8dd73-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8dd73-128">-WhatIf</span></span>
<span data-ttu-id="8dd73-129">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="8dd73-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8dd73-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="8dd73-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8dd73-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8dd73-131">CommonParameters</span></span>
<span data-ttu-id="8dd73-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8dd73-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8dd73-133">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8dd73-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8dd73-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8dd73-134">INPUTS</span></span>

### <span data-ttu-id="8dd73-135">Microsoft. Azure. Commands. Management. Storage. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="8dd73-135">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="8dd73-136">System. String</span><span class="sxs-lookup"><span data-stu-id="8dd73-136">System.String</span></span>

## <span data-ttu-id="8dd73-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8dd73-137">OUTPUTS</span></span>

### <span data-ttu-id="8dd73-138">Microsoft. Azure. Commands. Management. Storage. Models. PSBlobServiceProperties</span><span class="sxs-lookup"><span data-stu-id="8dd73-138">Microsoft.Azure.Commands.Management.Storage.Models.PSBlobServiceProperties</span></span>

## <span data-ttu-id="8dd73-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8dd73-139">NOTES</span></span>

## <span data-ttu-id="8dd73-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8dd73-140">RELATED LINKS</span></span>
