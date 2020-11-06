---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
ms.assetid: 11AAA319-DDBB-4156-9BE7-4DE8B80A904C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storage/get-azurermstorageusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Get-AzureRmStorageUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Get-AzureRmStorageUsage.md
ms.openlocfilehash: c63573da3c12eb54329d05f49615057d0595b77c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431281"
---
# <span data-ttu-id="e7e41-101">Get-AzureRmStorageUsage</span><span class="sxs-lookup"><span data-stu-id="e7e41-101">Get-AzureRmStorageUsage</span></span>

## <span data-ttu-id="e7e41-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e7e41-102">SYNOPSIS</span></span>
<span data-ttu-id="e7e41-103">Obtém o uso do recurso de armazenamento da assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="e7e41-103">Gets the Storage resource usage of the current subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e7e41-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e7e41-104">SYNTAX</span></span>

```
Get-AzureRmStorageUsage [-Location <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e7e41-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e7e41-105">DESCRIPTION</span></span>
<span data-ttu-id="e7e41-106">O cmdlet **Get-AzureRmStorageUsage** Obtém o uso do recurso do armazenamento do Azure para a assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="e7e41-106">The **Get-AzureRmStorageUsage** cmdlet gets the resource usage for Azure Storage for the current subscription.</span></span>

## <span data-ttu-id="e7e41-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e7e41-107">EXAMPLES</span></span>

### <span data-ttu-id="e7e41-108">Exemplo 1: obter o uso dos recursos de armazenamento</span><span class="sxs-lookup"><span data-stu-id="e7e41-108">Example 1: Get the storage resources usage</span></span>
```
PS C:\>Get-AzureRmStorageUsage
```

<span data-ttu-id="e7e41-109">Este comando obtém o uso dos recursos de armazenamento da assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="e7e41-109">This command gets the Storage resources usage of the current subscription.</span></span>
 

### <span data-ttu-id="e7e41-110">Exemplo 2: obter o uso dos recursos de armazenamento do local especificado</span><span class="sxs-lookup"><span data-stu-id="e7e41-110">Example 2: Get the storage resources usage of specified location</span></span>
```
PS C:\>Get-AzureRmStorageUsage -Location 'West US'

LocalizedName : Storage Accounts
Name          : StorageAccounts
Unit          : Count
CurrentValue  : 18
Limit         : 250
```

<span data-ttu-id="e7e41-111">Esse comando obtém o uso dos recursos de armazenamento do local especificado sob a assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="e7e41-111">This command gets the Storage resources usage of the specified location under the current subscription.</span></span>

## <span data-ttu-id="e7e41-112">OS</span><span class="sxs-lookup"><span data-stu-id="e7e41-112">PARAMETERS</span></span>

### <span data-ttu-id="e7e41-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7e41-113">-DefaultProfile</span></span>
<span data-ttu-id="e7e41-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e7e41-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7e41-115">-Local</span><span class="sxs-lookup"><span data-stu-id="e7e41-115">-Location</span></span>
<span data-ttu-id="e7e41-116">Indique para obter o uso de recursos de armazenamento no local especificado.</span><span class="sxs-lookup"><span data-stu-id="e7e41-116">Indicate to get Storage resources usage on the specified location.</span></span>
<span data-ttu-id="e7e41-117">Se não for especificado, receberá o uso de recursos de armazenamento em todos os locais sob a assinatura.</span><span class="sxs-lookup"><span data-stu-id="e7e41-117">If not specified, will get Storage resources usage on all locations under the subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7e41-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7e41-118">CommonParameters</span></span>
<span data-ttu-id="e7e41-119">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e7e41-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7e41-120">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e7e41-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7e41-121">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e7e41-121">INPUTS</span></span>

### <span data-ttu-id="e7e41-122">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="e7e41-122">None</span></span>

## <span data-ttu-id="e7e41-123">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e7e41-123">OUTPUTS</span></span>

### <span data-ttu-id="e7e41-124">Microsoft. Azure. Commands. Management. Storage. Models. PSUsage</span><span class="sxs-lookup"><span data-stu-id="e7e41-124">Microsoft.Azure.Commands.Management.Storage.Models.PSUsage</span></span>

## <span data-ttu-id="e7e41-125">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e7e41-125">NOTES</span></span>

## <span data-ttu-id="e7e41-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e7e41-126">RELATED LINKS</span></span>

[<span data-ttu-id="e7e41-127">Cmdlets do Azure Storage Manager</span><span class="sxs-lookup"><span data-stu-id="e7e41-127">Azure Storage Manager Cmdlets</span></span>](./AzureRM.Storage.md)


