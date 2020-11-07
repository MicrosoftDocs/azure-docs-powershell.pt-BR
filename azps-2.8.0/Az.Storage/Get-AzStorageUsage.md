---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 11AAA319-DDBB-4156-9BE7-4DE8B80A904C
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageUsage.md
ms.openlocfilehash: 7d61b7672050cd1efa3868a8a89208c790a684fe
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93774082"
---
# <span data-ttu-id="42077-101">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="42077-101">Get-AzStorageUsage</span></span>

## <span data-ttu-id="42077-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="42077-102">SYNOPSIS</span></span>
<span data-ttu-id="42077-103">Obtém o uso do recurso de armazenamento da assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="42077-103">Gets the Storage resource usage of the current subscription.</span></span>

## <span data-ttu-id="42077-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="42077-104">SYNTAX</span></span>

```
Get-AzStorageUsage -Location <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="42077-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="42077-105">DESCRIPTION</span></span>
<span data-ttu-id="42077-106">O cmdlet **Get-AzStorageUsage** Obtém o uso do recurso do armazenamento do Azure para a assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="42077-106">The **Get-AzStorageUsage** cmdlet gets the resource usage for Azure Storage for the current subscription.</span></span>

## <span data-ttu-id="42077-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="42077-107">EXAMPLES</span></span>

### <span data-ttu-id="42077-108">Exemplo 1: obter o uso dos recursos de armazenamento do local especificado</span><span class="sxs-lookup"><span data-stu-id="42077-108">Example 1: Get the storage resources usage of specified location</span></span>
```
PS C:\>Get-AzStorageUsage -Location 'West US'

LocalizedName : Storage Accounts
Name          : StorageAccounts
Unit          : Count
CurrentValue  : 18
Limit         : 250
```

<span data-ttu-id="42077-109">Esse comando obtém o uso dos recursos de armazenamento do local especificado na assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="42077-109">This command gets the Storage resources usage of specified location under the current subscription.</span></span>

## <span data-ttu-id="42077-110">OS</span><span class="sxs-lookup"><span data-stu-id="42077-110">PARAMETERS</span></span>

### <span data-ttu-id="42077-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42077-111">-DefaultProfile</span></span>
<span data-ttu-id="42077-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="42077-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="42077-113">-Local</span><span class="sxs-lookup"><span data-stu-id="42077-113">-Location</span></span>
<span data-ttu-id="42077-114">Indique para obter o uso de recursos de armazenamento no local especificado.</span><span class="sxs-lookup"><span data-stu-id="42077-114">Indicate to get Storage resources usage on the specified location.</span></span>
<span data-ttu-id="42077-115">Se não for especificado, receberá o uso de recursos de armazenamento em todos os locais sob a assinatura.</span><span class="sxs-lookup"><span data-stu-id="42077-115">If not specified, will get Storage resources usage on all locations under the subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42077-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42077-116">CommonParameters</span></span>
<span data-ttu-id="42077-117">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="42077-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42077-118">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="42077-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42077-119">SENSORES</span><span class="sxs-lookup"><span data-stu-id="42077-119">INPUTS</span></span>

### <span data-ttu-id="42077-120">System. String</span><span class="sxs-lookup"><span data-stu-id="42077-120">System.String</span></span>

## <span data-ttu-id="42077-121">EXIBE</span><span class="sxs-lookup"><span data-stu-id="42077-121">OUTPUTS</span></span>

### <span data-ttu-id="42077-122">Microsoft. Azure. Commands. Management. Storage. Models. PSUsage</span><span class="sxs-lookup"><span data-stu-id="42077-122">Microsoft.Azure.Commands.Management.Storage.Models.PSUsage</span></span>

## <span data-ttu-id="42077-123">INFORMA</span><span class="sxs-lookup"><span data-stu-id="42077-123">NOTES</span></span>

## <span data-ttu-id="42077-124">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="42077-124">RELATED LINKS</span></span>

[<span data-ttu-id="42077-125">Cmdlets do Azure Storage Manager</span><span class="sxs-lookup"><span data-stu-id="42077-125">Azure Storage Manager Cmdlets</span></span>](./Az.Storage.md)

