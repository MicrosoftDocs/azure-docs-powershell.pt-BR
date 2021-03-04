---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/disable-azstorageblobdeleteretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Disable-AzStorageBlobDeleteRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Disable-AzStorageBlobDeleteRetentionPolicy.md
ms.openlocfilehash: f4ffd20a835a8357972c9f8b9209d505fd311c1a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888073"
---
# <span data-ttu-id="54743-101">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="54743-101">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>

## <span data-ttu-id="54743-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="54743-102">SYNOPSIS</span></span>
<span data-ttu-id="54743-103">Desabilite a política de retenção de exclusão para o serviço blob de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="54743-103">Disable delete retention policy for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="54743-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="54743-104">SYNTAX</span></span>

### <span data-ttu-id="54743-105">AccountName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="54743-105">AccountName (Default)</span></span>
```
Disable-AzStorageBlobDeleteRetentionPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="54743-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="54743-106">AccountObject</span></span>
```
Disable-AzStorageBlobDeleteRetentionPolicy -StorageAccount <PSStorageAccount> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="54743-107">BlobServicePropertiesResourceId</span><span class="sxs-lookup"><span data-stu-id="54743-107">BlobServicePropertiesResourceId</span></span>
```
Disable-AzStorageBlobDeleteRetentionPolicy [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="54743-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="54743-108">DESCRIPTION</span></span>
<span data-ttu-id="54743-109">O cmdlet **Disable-AzStorageBlobDeleteRetentionPolicy** desabilita a política de retenção de exclusão para o serviço blob de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="54743-109">The **Disable-AzStorageBlobDeleteRetentionPolicy** cmdlet disables delete retention policy for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="54743-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="54743-110">EXAMPLES</span></span>

### <span data-ttu-id="54743-111">Exemplo 1: Desabilitar a política de retenção de exclusão para o serviço Blob</span><span class="sxs-lookup"><span data-stu-id="54743-111">Example 1: Disable delete retention policy for the Blob service</span></span>
```
C:\PS>Disable-AzStorageBlobDeleteRetentionPolicy -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -PassThru

Enabled Days
------- ----
  False
```

<span data-ttu-id="54743-112">Este comando desabilita a política de retenção de exclusão para o serviço Blob.</span><span class="sxs-lookup"><span data-stu-id="54743-112">This command disables delete retention policy for the Blob service.</span></span>

## <span data-ttu-id="54743-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="54743-113">PARAMETERS</span></span>

### <span data-ttu-id="54743-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54743-114">-DefaultProfile</span></span>
<span data-ttu-id="54743-115">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="54743-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="54743-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="54743-116">-PassThru</span></span>
<span data-ttu-id="54743-117">Exibir ServiceProperties</span><span class="sxs-lookup"><span data-stu-id="54743-117">Display ServiceProperties</span></span>

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

### <span data-ttu-id="54743-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="54743-118">-ResourceGroupName</span></span>
<span data-ttu-id="54743-119">Nome do Grupo de Recursos.</span><span class="sxs-lookup"><span data-stu-id="54743-119">Resource Group Name.</span></span>

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

### <span data-ttu-id="54743-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="54743-120">-ResourceId</span></span>
<span data-ttu-id="54743-121">Input a Storage account Resource Id, or a Blob service properties Resource Id.</span><span class="sxs-lookup"><span data-stu-id="54743-121">Input a Storage account Resource Id, or a Blob service properties Resource Id.</span></span>

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

### <span data-ttu-id="54743-122">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="54743-122">-StorageAccount</span></span>
<span data-ttu-id="54743-123">Objeto de conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="54743-123">Storage account object</span></span>

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

### <span data-ttu-id="54743-124">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="54743-124">-StorageAccountName</span></span>
<span data-ttu-id="54743-125">Nome da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="54743-125">Storage Account Name.</span></span>

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

### <span data-ttu-id="54743-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="54743-126">-Confirm</span></span>
<span data-ttu-id="54743-127">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="54743-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="54743-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="54743-128">-WhatIf</span></span>
<span data-ttu-id="54743-129">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="54743-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="54743-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="54743-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="54743-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54743-131">CommonParameters</span></span>
<span data-ttu-id="54743-132">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="54743-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54743-133">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="54743-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54743-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="54743-134">INPUTS</span></span>

### <span data-ttu-id="54743-135">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="54743-135">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="54743-136">System.String</span><span class="sxs-lookup"><span data-stu-id="54743-136">System.String</span></span>

## <span data-ttu-id="54743-137">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="54743-137">OUTPUTS</span></span>

### <span data-ttu-id="54743-138">Microsoft.Azure.Commands.Management.Storage.Models.PSDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="54743-138">Microsoft.Azure.Commands.Management.Storage.Models.PSDeleteRetentionPolicy</span></span>

## <span data-ttu-id="54743-139">NOTES</span><span class="sxs-lookup"><span data-stu-id="54743-139">NOTES</span></span>

## <span data-ttu-id="54743-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="54743-140">RELATED LINKS</span></span>
