---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azprivatelinkresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateLinkResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateLinkResource.md
ms.openlocfilehash: 3ba277ccee3a07f71677628fdc0a985225cdf724
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93943303"
---
# <span data-ttu-id="1f3a7-101">Get-AzPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="1f3a7-101">Get-AzPrivateLinkResource</span></span>

## <span data-ttu-id="1f3a7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1f3a7-102">SYNOPSIS</span></span>
<span data-ttu-id="1f3a7-103">Obtém um recurso de link particular.</span><span class="sxs-lookup"><span data-stu-id="1f3a7-103">Gets a private link resource.</span></span>

## <span data-ttu-id="1f3a7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1f3a7-104">SYNTAX</span></span>

### <span data-ttu-id="1f3a7-105">ByPrivateLinkResourceId (padrão)</span><span class="sxs-lookup"><span data-stu-id="1f3a7-105">ByPrivateLinkResourceId (Default)</span></span>
```
Get-AzPrivateLinkResource -PrivateLinkResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1f3a7-106">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1f3a7-106">DESCRIPTION</span></span>
<span data-ttu-id="1f3a7-107">O cmdlet **Get-AzPrivateLinkResource** recupera todos os recursos de link que pertencem ao PrivateLinkResource.</span><span class="sxs-lookup"><span data-stu-id="1f3a7-107">The **Get-AzPrivateLinkResource** cmdlet retrieves all link resources belongs PrivateLinkResource.</span></span>

## <span data-ttu-id="1f3a7-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1f3a7-108">EXAMPLES</span></span>

### <span data-ttu-id="1f3a7-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="1f3a7-109">Example 1</span></span>
```
Get-AzPrivateLinkResource -PrivateLinkResourceId '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/TestResourceGroup/providers/Microsoft.Sql/servers/mySql'
```

<span data-ttu-id="1f3a7-110">Este exemplo lista todos os recursos de link privado nbelong para o SQL Server chamado mySql.</span><span class="sxs-lookup"><span data-stu-id="1f3a7-110">This example list all private link resources nbelong to sql server named mySql.</span></span>

## <span data-ttu-id="1f3a7-111">OS</span><span class="sxs-lookup"><span data-stu-id="1f3a7-111">PARAMETERS</span></span>

### <span data-ttu-id="1f3a7-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f3a7-112">-DefaultProfile</span></span>
<span data-ttu-id="1f3a7-113">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1f3a7-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1f3a7-114">-PrivateLinkResourceId</span><span class="sxs-lookup"><span data-stu-id="1f3a7-114">-PrivateLinkResourceId</span></span>
<span data-ttu-id="1f3a7-115">A ID do Gerenciador de recursos do Azure do recurso de link particular.</span><span class="sxs-lookup"><span data-stu-id="1f3a7-115">The Azure resource manager id of the private link resource.</span></span>

```yaml
Type: System.String
Parameter Sets: ByPrivateLinkResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f3a7-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f3a7-116">CommonParameters</span></span>
<span data-ttu-id="1f3a7-117">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1f3a7-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f3a7-118">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1f3a7-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f3a7-119">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1f3a7-119">INPUTS</span></span>

### <span data-ttu-id="1f3a7-120">System. String</span><span class="sxs-lookup"><span data-stu-id="1f3a7-120">System.String</span></span>

## <span data-ttu-id="1f3a7-121">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1f3a7-121">OUTPUTS</span></span>

### <span data-ttu-id="1f3a7-122">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="1f3a7-122">System.Boolean</span></span>

## <span data-ttu-id="1f3a7-123">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1f3a7-123">NOTES</span></span>

## <span data-ttu-id="1f3a7-124">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1f3a7-124">RELATED LINKS</span></span>
