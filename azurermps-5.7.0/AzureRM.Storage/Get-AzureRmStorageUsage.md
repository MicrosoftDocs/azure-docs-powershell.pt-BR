---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
ms.assetid: 11AAA319-DDBB-4156-9BE7-4DE8B80A904C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storage/get-azurermstorageusage
schema: 2.0.0
ms.openlocfilehash: 5d44fa0a3e0ead373a822ae91080df9bdc60cc50
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432867"
---
# <span data-ttu-id="1bb15-101">Get-AzureRmStorageUsage</span><span class="sxs-lookup"><span data-stu-id="1bb15-101">Get-AzureRmStorageUsage</span></span>

## <span data-ttu-id="1bb15-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1bb15-102">SYNOPSIS</span></span>
<span data-ttu-id="1bb15-103">Obtém o uso do recurso de armazenamento da assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="1bb15-103">Gets the Storage resource usage of the current subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1bb15-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1bb15-104">SYNTAX</span></span>

```
Get-AzureRmStorageUsage [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1bb15-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1bb15-105">DESCRIPTION</span></span>
<span data-ttu-id="1bb15-106">O cmdlet **Get-AzureRmStorageUsage** Obtém o uso do recurso do armazenamento do Azure para a assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="1bb15-106">The **Get-AzureRmStorageUsage** cmdlet gets the resource usage for Azure Storage for the current subscription.</span></span>

## <span data-ttu-id="1bb15-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1bb15-107">EXAMPLES</span></span>

### <span data-ttu-id="1bb15-108">Exemplo 1: obter o uso dos recursos de armazenamento</span><span class="sxs-lookup"><span data-stu-id="1bb15-108">Example 1: Get the storage resources usage</span></span>
```
PS C:\>Get-AzureRmStorageUsage
```

<span data-ttu-id="1bb15-109">Este comando obtém o uso dos recursos de armazenamento da assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="1bb15-109">This command gets the Storage resources usage of the current subscription.</span></span>

## <span data-ttu-id="1bb15-110">OS</span><span class="sxs-lookup"><span data-stu-id="1bb15-110">PARAMETERS</span></span>

### <span data-ttu-id="1bb15-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1bb15-111">-DefaultProfile</span></span>
<span data-ttu-id="1bb15-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1bb15-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1bb15-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1bb15-113">CommonParameters</span></span>
<span data-ttu-id="1bb15-114">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1bb15-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1bb15-115">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1bb15-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1bb15-116">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1bb15-116">INPUTS</span></span>

### <span data-ttu-id="1bb15-117">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="1bb15-117">None</span></span>
<span data-ttu-id="1bb15-118">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="1bb15-118">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="1bb15-119">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1bb15-119">OUTPUTS</span></span>

### <span data-ttu-id="1bb15-120">Microsoft. Azure. Commands. Management. Storage. Models. PSUsage</span><span class="sxs-lookup"><span data-stu-id="1bb15-120">Microsoft.Azure.Commands.Management.Storage.Models.PSUsage</span></span>

## <span data-ttu-id="1bb15-121">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1bb15-121">NOTES</span></span>

## <span data-ttu-id="1bb15-122">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1bb15-122">RELATED LINKS</span></span>

[<span data-ttu-id="1bb15-123">Cmdlets do Azure Storage Manager</span><span class="sxs-lookup"><span data-stu-id="1bb15-123">Azure Storage Manager Cmdlets</span></span>](./AzureRM.Storage.md)


