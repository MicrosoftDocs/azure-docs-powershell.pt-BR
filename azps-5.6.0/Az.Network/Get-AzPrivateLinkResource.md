---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azprivatelinkresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateLinkResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateLinkResource.md
ms.openlocfilehash: 5c341677f5bc741f5848508f80b1a29e29c90b17
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101885661"
---
# <span data-ttu-id="bb1f0-101">Get-AzPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="bb1f0-101">Get-AzPrivateLinkResource</span></span>

## <span data-ttu-id="bb1f0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bb1f0-102">SYNOPSIS</span></span>
<span data-ttu-id="bb1f0-103">Obtém um recurso de link privado.</span><span class="sxs-lookup"><span data-stu-id="bb1f0-103">Gets a private link resource.</span></span>

## <span data-ttu-id="bb1f0-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="bb1f0-104">SYNTAX</span></span>

### <span data-ttu-id="bb1f0-105">ByPrivateLinkResourceId (Padrão)</span><span class="sxs-lookup"><span data-stu-id="bb1f0-105">ByPrivateLinkResourceId (Default)</span></span>
```
Get-AzPrivateLinkResource -PrivateLinkResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="bb1f0-106">ByResource</span><span class="sxs-lookup"><span data-stu-id="bb1f0-106">ByResource</span></span>
```
Get-AzPrivateLinkResource -ResourceGroupName <String> -ServiceName <String>
 [-DefaultProfile <IAzureContextContainer>] [-PrivateLinkResourceType <String>] [<CommonParameters>]
```

## <span data-ttu-id="bb1f0-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="bb1f0-107">DESCRIPTION</span></span>
<span data-ttu-id="bb1f0-108">O cmdlet **Get-AzPrivateLinkResource** recupera todos os recursos de link pertence a PrivateLinkResource.</span><span class="sxs-lookup"><span data-stu-id="bb1f0-108">The **Get-AzPrivateLinkResource** cmdlet retrieves all link resources belongs PrivateLinkResource.</span></span>

## <span data-ttu-id="bb1f0-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="bb1f0-109">EXAMPLES</span></span>

### <span data-ttu-id="bb1f0-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="bb1f0-110">Example 1</span></span>
```
Get-AzPrivateLinkResource -PrivateLinkResourceId '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/TestResourceGroup/providers/Microsoft.Sql/servers/mySql'
```

<span data-ttu-id="bb1f0-111">Este exemplo lista todos os recursos de link privado nbelong to sql server named mySql.</span><span class="sxs-lookup"><span data-stu-id="bb1f0-111">This example list all private link resources nbelong to sql server named mySql.</span></span>

## <span data-ttu-id="bb1f0-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="bb1f0-112">PARAMETERS</span></span>

### <span data-ttu-id="bb1f0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb1f0-113">-DefaultProfile</span></span>
<span data-ttu-id="bb1f0-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="bb1f0-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bb1f0-115">-PrivateLinkResourceId</span><span class="sxs-lookup"><span data-stu-id="bb1f0-115">-PrivateLinkResourceId</span></span>
<span data-ttu-id="bb1f0-116">A ID do gerenciador de recursos do Azure do recurso de link privado.</span><span class="sxs-lookup"><span data-stu-id="bb1f0-116">The Azure resource manager id of the private link resource.</span></span>

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

### <span data-ttu-id="bb1f0-117">-PrivateLinkResourceType</span><span class="sxs-lookup"><span data-stu-id="bb1f0-117">-PrivateLinkResourceType</span></span>
<span data-ttu-id="bb1f0-118">O tipo de recurso de link privado.</span><span class="sxs-lookup"><span data-stu-id="bb1f0-118">The private link resource type.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResource
Aliases:
Accepted values:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bb1f0-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bb1f0-119">-ResourceGroupName</span></span>
<span data-ttu-id="bb1f0-120">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="bb1f0-120">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bb1f0-121">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="bb1f0-121">-ServiceName</span></span>
<span data-ttu-id="bb1f0-122">O nome do serviço de link privado.</span><span class="sxs-lookup"><span data-stu-id="bb1f0-122">The private link service name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bb1f0-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb1f0-123">CommonParameters</span></span>
<span data-ttu-id="bb1f0-124">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bb1f0-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb1f0-125">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bb1f0-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb1f0-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="bb1f0-126">INPUTS</span></span>

### <span data-ttu-id="bb1f0-127">System.String</span><span class="sxs-lookup"><span data-stu-id="bb1f0-127">System.String</span></span>

## <span data-ttu-id="bb1f0-128">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="bb1f0-128">OUTPUTS</span></span>

### <span data-ttu-id="bb1f0-129">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="bb1f0-129">System.Boolean</span></span>

## <span data-ttu-id="bb1f0-130">NOTES</span><span class="sxs-lookup"><span data-stu-id="bb1f0-130">NOTES</span></span>

## <span data-ttu-id="bb1f0-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bb1f0-131">RELATED LINKS</span></span>
