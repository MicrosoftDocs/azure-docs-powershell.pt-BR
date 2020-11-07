---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/enable-azstorageblobdeleteretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Enable-AzStorageBlobDeleteRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Enable-AzStorageBlobDeleteRetentionPolicy.md
ms.openlocfilehash: fdac081aa6edc5ac43c98800ad2d857cb8f62b09
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93773745"
---
# <span data-ttu-id="7c24d-101">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="7c24d-101">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>

## <span data-ttu-id="7c24d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7c24d-102">SYNOPSIS</span></span>
<span data-ttu-id="7c24d-103">Habilite a política de retenção de exclusão para o serviço de blob de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="7c24d-103">Enable delete retention policy for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="7c24d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7c24d-104">SYNTAX</span></span>

### <span data-ttu-id="7c24d-105">AccountName (padrão)</span><span class="sxs-lookup"><span data-stu-id="7c24d-105">AccountName (Default)</span></span>
```
Enable-AzStorageBlobDeleteRetentionPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -RetentionDays <Int32> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7c24d-106">Accountobject</span><span class="sxs-lookup"><span data-stu-id="7c24d-106">AccountObject</span></span>
```
Enable-AzStorageBlobDeleteRetentionPolicy -StorageAccount <PSStorageAccount> -RetentionDays <Int32> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7c24d-107">BlobServicePropertiesResourceId</span><span class="sxs-lookup"><span data-stu-id="7c24d-107">BlobServicePropertiesResourceId</span></span>
```
Enable-AzStorageBlobDeleteRetentionPolicy [-ResourceId] <String> -RetentionDays <Int32> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7c24d-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7c24d-108">DESCRIPTION</span></span>
<span data-ttu-id="7c24d-109">O cmdlet **Enable-AzStorageBlobDeleteRetentionPolicy** permite excluir a política de retenção para o serviço blob de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="7c24d-109">The **Enable-AzStorageBlobDeleteRetentionPolicy** cmdlet enables delete retention policy for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="7c24d-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7c24d-110">EXAMPLES</span></span>

### <span data-ttu-id="7c24d-111">Exemplo 1: habilitar a política de retenção de exclusão para o serviço blob</span><span class="sxs-lookup"><span data-stu-id="7c24d-111">Example 1: Enable delete retention policy for the Blob service</span></span>
```
C:\PS>Enable-AzStorageBlobDeleteRetentionPolicy -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -PassThru -RetentionDays 4

Enabled Days
------- ----
   True    4
```

<span data-ttu-id="7c24d-112">Esse comando habilita a política de retenção de exclusão para o serviço BLOB e define os dias de retenção de blob excluídos como 4.</span><span class="sxs-lookup"><span data-stu-id="7c24d-112">This command enables delete retention policy for the Blob service, and set deleted blob retention days to 4.</span></span>

## <span data-ttu-id="7c24d-113">OS</span><span class="sxs-lookup"><span data-stu-id="7c24d-113">PARAMETERS</span></span>

### <span data-ttu-id="7c24d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c24d-114">-DefaultProfile</span></span>
<span data-ttu-id="7c24d-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7c24d-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7c24d-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7c24d-116">-PassThru</span></span>
<span data-ttu-id="7c24d-117">Display Serviceproperties</span><span class="sxs-lookup"><span data-stu-id="7c24d-117">Display ServiceProperties</span></span>

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

### <span data-ttu-id="7c24d-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7c24d-118">-ResourceGroupName</span></span>
<span data-ttu-id="7c24d-119">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="7c24d-119">Resource Group Name.</span></span>

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

### <span data-ttu-id="7c24d-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7c24d-120">-ResourceId</span></span>
<span data-ttu-id="7c24d-121">Insira uma ID de recurso da conta de armazenamento ou uma ID do recurso de propriedades do serviço BLOB.</span><span class="sxs-lookup"><span data-stu-id="7c24d-121">Input a Storage account Resource Id, or a Blob service properties Resource Id.</span></span>

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

### <span data-ttu-id="7c24d-122">-RetentionDays</span><span class="sxs-lookup"><span data-stu-id="7c24d-122">-RetentionDays</span></span>
<span data-ttu-id="7c24d-123">Define o número de dias de retenção para o DeleteRetentionPolicy.</span><span class="sxs-lookup"><span data-stu-id="7c24d-123">Sets the number of retention days for the DeleteRetentionPolicy.</span></span>

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

### <span data-ttu-id="7c24d-124">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="7c24d-124">-StorageAccount</span></span>
<span data-ttu-id="7c24d-125">Objeto da conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="7c24d-125">Storage account object</span></span>

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

### <span data-ttu-id="7c24d-126">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="7c24d-126">-StorageAccountName</span></span>
<span data-ttu-id="7c24d-127">Nome da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="7c24d-127">Storage Account Name.</span></span>

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

### <span data-ttu-id="7c24d-128">-Confirme</span><span class="sxs-lookup"><span data-stu-id="7c24d-128">-Confirm</span></span>
<span data-ttu-id="7c24d-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7c24d-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7c24d-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7c24d-130">-WhatIf</span></span>
<span data-ttu-id="7c24d-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="7c24d-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7c24d-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="7c24d-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7c24d-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c24d-133">CommonParameters</span></span>
<span data-ttu-id="7c24d-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7c24d-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c24d-135">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7c24d-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c24d-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7c24d-136">INPUTS</span></span>

### <span data-ttu-id="7c24d-137">Microsoft. Azure. Commands. Management. Storage. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="7c24d-137">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="7c24d-138">System. String</span><span class="sxs-lookup"><span data-stu-id="7c24d-138">System.String</span></span>

## <span data-ttu-id="7c24d-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7c24d-139">OUTPUTS</span></span>

### <span data-ttu-id="7c24d-140">Microsoft. Azure. Commands. Management. Storage. Models. PSBlobServiceProperties</span><span class="sxs-lookup"><span data-stu-id="7c24d-140">Microsoft.Azure.Commands.Management.Storage.Models.PSBlobServiceProperties</span></span>

## <span data-ttu-id="7c24d-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7c24d-141">NOTES</span></span>

## <span data-ttu-id="7c24d-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7c24d-142">RELATED LINKS</span></span>