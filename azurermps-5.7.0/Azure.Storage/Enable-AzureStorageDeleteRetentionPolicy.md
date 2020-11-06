---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/enable-azurestoragedeleteretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Enable-AzureStorageDeleteRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Enable-AzureStorageDeleteRetentionPolicy.md
ms.openlocfilehash: f8303a9d87a2bd5312732bd01eb3d42bd1e0a285
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427729"
---
# <span data-ttu-id="241bd-101">Enable-AzureStorageDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="241bd-101">Enable-AzureStorageDeleteRetentionPolicy</span></span>

## <span data-ttu-id="241bd-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="241bd-102">SYNOPSIS</span></span>
<span data-ttu-id="241bd-103">Habilite a política de retenção de exclusão para o serviço de blob de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="241bd-103">Enable delete retention policy  for the Azure Storage Blob service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="241bd-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="241bd-104">SYNTAX</span></span>

```
Enable-AzureStorageDeleteRetentionPolicy [-RetentionDays] <Int32> [-PassThru] [-Context <IStorageContext>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="241bd-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="241bd-105">DESCRIPTION</span></span>
<span data-ttu-id="241bd-106">O cmdlet **Enable-AzureStorageDeleteRetentionPolicy** permite excluir a política de retenção para o serviço blob de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="241bd-106">The **Enable-AzureStorageDeleteRetentionPolicy** cmdlet enables delete retention policy for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="241bd-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="241bd-107">EXAMPLES</span></span>

### <span data-ttu-id="241bd-108">Exemplo 1: habilitar a política de retenção de exclusão para o serviço blob</span><span class="sxs-lookup"><span data-stu-id="241bd-108">Example 1: Enable delete retention policy for the Blob service</span></span>
```
C:\PS>Enable-AzureStorageDeleteRetentionPolicy -RetentionDays 3
```

<span data-ttu-id="241bd-109">Esse comando habilita a política de retenção de exclusão para o serviço BLOB e define os dias de retenção de blob excluídos como 3.</span><span class="sxs-lookup"><span data-stu-id="241bd-109">This command enables delete retention policy for the Blob service, and set deleted blob retention days to 3.</span></span>

## <span data-ttu-id="241bd-110">OS</span><span class="sxs-lookup"><span data-stu-id="241bd-110">PARAMETERS</span></span>

### <span data-ttu-id="241bd-111">-Contexto</span><span class="sxs-lookup"><span data-stu-id="241bd-111">-Context</span></span>
<span data-ttu-id="241bd-112">Objeto de contexto de armazenamento do Azure</span><span class="sxs-lookup"><span data-stu-id="241bd-112">Azure Storage Context Object</span></span>

```yaml
Type: IStorageContext
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="241bd-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="241bd-113">-PassThru</span></span>
<span data-ttu-id="241bd-114">Exibir DeleteRetentionPolicyProperties</span><span class="sxs-lookup"><span data-stu-id="241bd-114">Display DeleteRetentionPolicyProperties</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="241bd-115">-RetentionDays</span><span class="sxs-lookup"><span data-stu-id="241bd-115">-RetentionDays</span></span>
<span data-ttu-id="241bd-116">Define o número de dias de retenção para o DeleteRetentionPolicy.</span><span class="sxs-lookup"><span data-stu-id="241bd-116">Sets the number of retention days for the DeleteRetentionPolicy.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: Days

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="241bd-117">-Confirme</span><span class="sxs-lookup"><span data-stu-id="241bd-117">-Confirm</span></span>
<span data-ttu-id="241bd-118">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="241bd-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="241bd-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="241bd-119">-WhatIf</span></span>
<span data-ttu-id="241bd-120">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="241bd-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="241bd-121">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="241bd-121">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="241bd-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="241bd-122">CommonParameters</span></span>
<span data-ttu-id="241bd-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="241bd-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="241bd-124">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="241bd-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="241bd-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="241bd-125">INPUTS</span></span>

### <span data-ttu-id="241bd-126">Microsoft. Azure. Commands. Common. Authentication. Abstractings. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="241bd-126">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="241bd-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="241bd-127">OUTPUTS</span></span>

### <span data-ttu-id="241bd-128">Microsoft. WindowsAzure. Storage. Shared. Protocol. DeleteRetentionPolicyProperties</span><span class="sxs-lookup"><span data-stu-id="241bd-128">Microsoft.WindowsAzure.Storage.Shared.Protocol.DeleteRetentionPolicyProperties</span></span>

## <span data-ttu-id="241bd-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="241bd-129">NOTES</span></span>

## <span data-ttu-id="241bd-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="241bd-130">RELATED LINKS</span></span>

