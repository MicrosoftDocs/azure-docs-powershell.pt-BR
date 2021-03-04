---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/enable-azstorageblobdeleteretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Enable-AzStorageBlobDeleteRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Enable-AzStorageBlobDeleteRetentionPolicy.md
ms.openlocfilehash: 9a4afaa1a67d9f1f9bffa0fdf6c7b40c7cf72b13
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888058"
---
# <span data-ttu-id="bcdf0-101">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="bcdf0-101">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>

## <span data-ttu-id="bcdf0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bcdf0-102">SYNOPSIS</span></span>
<span data-ttu-id="bcdf0-103">Habilitar a política de retenção de exclusão para o serviço blob de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="bcdf0-103">Enable delete retention policy for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="bcdf0-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="bcdf0-104">SYNTAX</span></span>

### <span data-ttu-id="bcdf0-105">AccountName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="bcdf0-105">AccountName (Default)</span></span>
```
Enable-AzStorageBlobDeleteRetentionPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -RetentionDays <Int32> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bcdf0-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="bcdf0-106">AccountObject</span></span>
```
Enable-AzStorageBlobDeleteRetentionPolicy -StorageAccount <PSStorageAccount> -RetentionDays <Int32> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bcdf0-107">BlobServicePropertiesResourceId</span><span class="sxs-lookup"><span data-stu-id="bcdf0-107">BlobServicePropertiesResourceId</span></span>
```
Enable-AzStorageBlobDeleteRetentionPolicy [-ResourceId] <String> -RetentionDays <Int32> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bcdf0-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="bcdf0-108">DESCRIPTION</span></span>
<span data-ttu-id="bcdf0-109">O cmdlet **Enable-AzStorageBlobDeleteRetentionPolicy** permite excluir a política de retenção para o serviço blob de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="bcdf0-109">The **Enable-AzStorageBlobDeleteRetentionPolicy** cmdlet enables delete retention policy for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="bcdf0-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="bcdf0-110">EXAMPLES</span></span>

### <span data-ttu-id="bcdf0-111">Exemplo 1: Habilitar a política de retenção de exclusão para o serviço Blob</span><span class="sxs-lookup"><span data-stu-id="bcdf0-111">Example 1: Enable delete retention policy for the Blob service</span></span>
```
C:\PS>Enable-AzStorageBlobDeleteRetentionPolicy -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -PassThru -RetentionDays 4

Enabled Days
------- ----
   True    4
```

<span data-ttu-id="bcdf0-112">Esse comando permite excluir a política de retenção para o serviço Blob e definir os dias de retenção de blob excluídos como 4.</span><span class="sxs-lookup"><span data-stu-id="bcdf0-112">This command enables delete retention policy for the Blob service, and set deleted blob retention days to 4.</span></span>

## <span data-ttu-id="bcdf0-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="bcdf0-113">PARAMETERS</span></span>

### <span data-ttu-id="bcdf0-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bcdf0-114">-DefaultProfile</span></span>
<span data-ttu-id="bcdf0-115">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="bcdf0-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bcdf0-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bcdf0-116">-PassThru</span></span>
<span data-ttu-id="bcdf0-117">Exibir ServiceProperties</span><span class="sxs-lookup"><span data-stu-id="bcdf0-117">Display ServiceProperties</span></span>

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

### <span data-ttu-id="bcdf0-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bcdf0-118">-ResourceGroupName</span></span>
<span data-ttu-id="bcdf0-119">Nome do Grupo de Recursos.</span><span class="sxs-lookup"><span data-stu-id="bcdf0-119">Resource Group Name.</span></span>

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

### <span data-ttu-id="bcdf0-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bcdf0-120">-ResourceId</span></span>
<span data-ttu-id="bcdf0-121">Input a Storage account Resource Id, or a Blob service properties Resource Id.</span><span class="sxs-lookup"><span data-stu-id="bcdf0-121">Input a Storage account Resource Id, or a Blob service properties Resource Id.</span></span>

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

### <span data-ttu-id="bcdf0-122">-RetentionDays</span><span class="sxs-lookup"><span data-stu-id="bcdf0-122">-RetentionDays</span></span>
<span data-ttu-id="bcdf0-123">Define o número de dias de retenção para DeleteRetentionPolicy.</span><span class="sxs-lookup"><span data-stu-id="bcdf0-123">Sets the number of retention days for the DeleteRetentionPolicy.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: Days

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bcdf0-124">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="bcdf0-124">-StorageAccount</span></span>
<span data-ttu-id="bcdf0-125">Objeto de conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="bcdf0-125">Storage account object</span></span>

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

### <span data-ttu-id="bcdf0-126">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="bcdf0-126">-StorageAccountName</span></span>
<span data-ttu-id="bcdf0-127">Nome da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="bcdf0-127">Storage Account Name.</span></span>

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

### <span data-ttu-id="bcdf0-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bcdf0-128">-Confirm</span></span>
<span data-ttu-id="bcdf0-129">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bcdf0-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bcdf0-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bcdf0-130">-WhatIf</span></span>
<span data-ttu-id="bcdf0-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="bcdf0-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bcdf0-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="bcdf0-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bcdf0-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bcdf0-133">CommonParameters</span></span>
<span data-ttu-id="bcdf0-134">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bcdf0-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bcdf0-135">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bcdf0-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bcdf0-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="bcdf0-136">INPUTS</span></span>

### <span data-ttu-id="bcdf0-137">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="bcdf0-137">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="bcdf0-138">System.String</span><span class="sxs-lookup"><span data-stu-id="bcdf0-138">System.String</span></span>

## <span data-ttu-id="bcdf0-139">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="bcdf0-139">OUTPUTS</span></span>

### <span data-ttu-id="bcdf0-140">Microsoft.Azure.Commands.Management.Storage.Models.PSBlobServiceProperties</span><span class="sxs-lookup"><span data-stu-id="bcdf0-140">Microsoft.Azure.Commands.Management.Storage.Models.PSBlobServiceProperties</span></span>

## <span data-ttu-id="bcdf0-141">NOTES</span><span class="sxs-lookup"><span data-stu-id="bcdf0-141">NOTES</span></span>

## <span data-ttu-id="bcdf0-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bcdf0-142">RELATED LINKS</span></span>
