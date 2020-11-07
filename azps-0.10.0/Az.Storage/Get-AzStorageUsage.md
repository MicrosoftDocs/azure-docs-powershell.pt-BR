---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 11AAA319-DDBB-4156-9BE7-4DE8B80A904C
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Get-AzStorageUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Get-AzStorageUsage.md
ms.openlocfilehash: edf78ad4022b29251d78e976ff7e5d66ae67bb69
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93776239"
---
# <span data-ttu-id="ab2d8-101">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="ab2d8-101">Get-AzStorageUsage</span></span>

## <span data-ttu-id="ab2d8-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ab2d8-102">SYNOPSIS</span></span>
<span data-ttu-id="ab2d8-103">Obtém o uso do recurso de armazenamento da assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="ab2d8-103">Gets the Storage resource usage of the current subscription.</span></span>

## <span data-ttu-id="ab2d8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ab2d8-104">SYNTAX</span></span>

```
Get-AzStorageUsage [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ab2d8-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ab2d8-105">DESCRIPTION</span></span>
<span data-ttu-id="ab2d8-106">O cmdlet **Get-AzStorageUsage** Obtém o uso do recurso do armazenamento do Azure para a assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="ab2d8-106">The **Get-AzStorageUsage** cmdlet gets the resource usage for Azure Storage for the current subscription.</span></span>

## <span data-ttu-id="ab2d8-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ab2d8-107">EXAMPLES</span></span>

### <span data-ttu-id="ab2d8-108">Exemplo 1: obter o uso dos recursos de armazenamento</span><span class="sxs-lookup"><span data-stu-id="ab2d8-108">Example 1: Get the storage resources usage</span></span>
```
PS C:\>Get-AzStorageUsage
```

<span data-ttu-id="ab2d8-109">Este comando obtém o uso dos recursos de armazenamento da assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="ab2d8-109">This command gets the Storage resources usage of the current subscription.</span></span>

## <span data-ttu-id="ab2d8-110">OS</span><span class="sxs-lookup"><span data-stu-id="ab2d8-110">PARAMETERS</span></span>

### <span data-ttu-id="ab2d8-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab2d8-111">-DefaultProfile</span></span>
<span data-ttu-id="ab2d8-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ab2d8-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ab2d8-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab2d8-113">CommonParameters</span></span>
<span data-ttu-id="ab2d8-114">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ab2d8-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab2d8-115">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ab2d8-115">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab2d8-116">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ab2d8-116">INPUTS</span></span>

### <span data-ttu-id="ab2d8-117">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="ab2d8-117">None</span></span>

## <span data-ttu-id="ab2d8-118">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ab2d8-118">OUTPUTS</span></span>

### <span data-ttu-id="ab2d8-119">Microsoft. Azure. Commands. Management. Storage. Models. PSUsage</span><span class="sxs-lookup"><span data-stu-id="ab2d8-119">Microsoft.Azure.Commands.Management.Storage.Models.PSUsage</span></span>

## <span data-ttu-id="ab2d8-120">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ab2d8-120">NOTES</span></span>

## <span data-ttu-id="ab2d8-121">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ab2d8-121">RELATED LINKS</span></span>

[<span data-ttu-id="ab2d8-122">Cmdlets do Azure Storage Manager</span><span class="sxs-lookup"><span data-stu-id="ab2d8-122">Azure Storage Manager Cmdlets</span></span>](./Az.Storage.md)


