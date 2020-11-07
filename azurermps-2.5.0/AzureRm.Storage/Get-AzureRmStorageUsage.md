---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
ms.assetid: 11AAA319-DDBB-4156-9BE7-4DE8B80A904C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storage/get-azurermstorageusage
schema: 2.0.0
ms.openlocfilehash: ae6524c46ed97563e7bf6c948f550a393d74f582
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93785597"
---
# <span data-ttu-id="85b78-101">Get-AzureRmStorageUsage</span><span class="sxs-lookup"><span data-stu-id="85b78-101">Get-AzureRmStorageUsage</span></span>

## <span data-ttu-id="85b78-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="85b78-102">SYNOPSIS</span></span>
<span data-ttu-id="85b78-103">Obtém o uso do recurso de armazenamento da assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="85b78-103">Gets the Storage resource usage of the current subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="85b78-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="85b78-104">SYNTAX</span></span>

```
Get-AzureRmStorageUsage [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="85b78-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="85b78-105">DESCRIPTION</span></span>
<span data-ttu-id="85b78-106">O cmdlet **Get-AzureRmStorageUsage** Obtém o uso do recurso do armazenamento do Azure para a assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="85b78-106">The **Get-AzureRmStorageUsage** cmdlet gets the resource usage for Azure Storage for the current subscription.</span></span>

## <span data-ttu-id="85b78-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="85b78-107">EXAMPLES</span></span>

### <span data-ttu-id="85b78-108">Exemplo 1: obter o uso dos recursos de armazenamento</span><span class="sxs-lookup"><span data-stu-id="85b78-108">Example 1: Get the storage resources usage</span></span>
```
PS C:\>Get-AzureRmStorageUsage
```

<span data-ttu-id="85b78-109">Este comando obtém o uso dos recursos de armazenamento da assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="85b78-109">This command gets the Storage resources usage of the current subscription.</span></span>

## <span data-ttu-id="85b78-110">OS</span><span class="sxs-lookup"><span data-stu-id="85b78-110">PARAMETERS</span></span>

### <span data-ttu-id="85b78-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85b78-111">-DefaultProfile</span></span>
<span data-ttu-id="85b78-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="85b78-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="85b78-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85b78-113">CommonParameters</span></span>
<span data-ttu-id="85b78-114">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="85b78-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85b78-115">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="85b78-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85b78-116">SENSORES</span><span class="sxs-lookup"><span data-stu-id="85b78-116">INPUTS</span></span>

### <span data-ttu-id="85b78-117">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="85b78-117">None</span></span>

## <span data-ttu-id="85b78-118">EXIBE</span><span class="sxs-lookup"><span data-stu-id="85b78-118">OUTPUTS</span></span>

### <span data-ttu-id="85b78-119">Microsoft. Azure. Commands. Management. Storage. Models. PSUsage</span><span class="sxs-lookup"><span data-stu-id="85b78-119">Microsoft.Azure.Commands.Management.Storage.Models.PSUsage</span></span>

## <span data-ttu-id="85b78-120">INFORMA</span><span class="sxs-lookup"><span data-stu-id="85b78-120">NOTES</span></span>

## <span data-ttu-id="85b78-121">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="85b78-121">RELATED LINKS</span></span>

[<span data-ttu-id="85b78-122">Cmdlets do Azure Storage Manager</span><span class="sxs-lookup"><span data-stu-id="85b78-122">Azure Storage Manager Cmdlets</span></span>](./AzureRM.Storage.md)


