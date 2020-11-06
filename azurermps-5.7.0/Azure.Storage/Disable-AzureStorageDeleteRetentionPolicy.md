---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/disable-azurestoragedeleteretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Disable-AzureStorageDeleteRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Disable-AzureStorageDeleteRetentionPolicy.md
ms.openlocfilehash: d3de0cc49eb0e36572daa9e4cfbbb41c0db0936a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93602182"
---
# <span data-ttu-id="0cc6c-101">Disable-AzureStorageDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="0cc6c-101">Disable-AzureStorageDeleteRetentionPolicy</span></span>

## <span data-ttu-id="0cc6c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0cc6c-102">SYNOPSIS</span></span>
<span data-ttu-id="0cc6c-103">Desabilite a política de retenção de exclusão para o serviço de blob de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="0cc6c-103">Disable delete retention policy  for the Azure Storage Blob service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0cc6c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0cc6c-104">SYNTAX</span></span>

```
Disable-AzureStorageDeleteRetentionPolicy [-PassThru] [-Context <IStorageContext>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0cc6c-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="0cc6c-105">DESCRIPTION</span></span>
<span data-ttu-id="0cc6c-106">O cmdlet **Disable-AzureStorageDeleteRetentionPolicy** desabilita a política de retenção de exclusão para o serviço de blob de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="0cc6c-106">The **Disable-AzureStorageDeleteRetentionPolicy** cmdlet disables delete retention policy for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="0cc6c-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0cc6c-107">EXAMPLES</span></span>

### <span data-ttu-id="0cc6c-108">Exemplo 1: desabilitar a política de retenção de exclusão para o serviço blob</span><span class="sxs-lookup"><span data-stu-id="0cc6c-108">Example 1: Disable delete retention policy for the Blob service</span></span>
```
C:\PS>Disable-AzureStorageDeleteRetentionPolicy
```

<span data-ttu-id="0cc6c-109">Este comando desabilita a política de retenção de exclusão do serviço BLOB.</span><span class="sxs-lookup"><span data-stu-id="0cc6c-109">This command disables delete retention policy for the Blob service.</span></span>

## <span data-ttu-id="0cc6c-110">OS</span><span class="sxs-lookup"><span data-stu-id="0cc6c-110">PARAMETERS</span></span>

### <span data-ttu-id="0cc6c-111">-Contexto</span><span class="sxs-lookup"><span data-stu-id="0cc6c-111">-Context</span></span>
<span data-ttu-id="0cc6c-112">Objeto de contexto de armazenamento do Azure</span><span class="sxs-lookup"><span data-stu-id="0cc6c-112">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="0cc6c-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0cc6c-113">-PassThru</span></span>
<span data-ttu-id="0cc6c-114">Exibir DeleteRetentionPolicyProperties</span><span class="sxs-lookup"><span data-stu-id="0cc6c-114">Display DeleteRetentionPolicyProperties</span></span>

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

### <span data-ttu-id="0cc6c-115">-Confirme</span><span class="sxs-lookup"><span data-stu-id="0cc6c-115">-Confirm</span></span>
<span data-ttu-id="0cc6c-116">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0cc6c-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0cc6c-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0cc6c-117">-WhatIf</span></span>
<span data-ttu-id="0cc6c-118">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="0cc6c-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0cc6c-119">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="0cc6c-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0cc6c-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0cc6c-120">CommonParameters</span></span>
<span data-ttu-id="0cc6c-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0cc6c-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0cc6c-122">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0cc6c-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0cc6c-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="0cc6c-123">INPUTS</span></span>

### <span data-ttu-id="0cc6c-124">Microsoft. Azure. Commands. Common. Authentication. Abstractings. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="0cc6c-124">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="0cc6c-125">EXIBE</span><span class="sxs-lookup"><span data-stu-id="0cc6c-125">OUTPUTS</span></span>

### <span data-ttu-id="0cc6c-126">Microsoft. WindowsAzure. Commands. Storage. Model. resourcemode. PSSeriviceProperties</span><span class="sxs-lookup"><span data-stu-id="0cc6c-126">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceMode.PSSeriviceProperties</span></span>

## <span data-ttu-id="0cc6c-127">INFORMA</span><span class="sxs-lookup"><span data-stu-id="0cc6c-127">NOTES</span></span>

## <span data-ttu-id="0cc6c-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0cc6c-128">RELATED LINKS</span></span>

