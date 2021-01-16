---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azprivatelinkresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateLinkResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateLinkResource.md
ms.openlocfilehash: 7517509c64c66506444c3ed627338a0f9546a00b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98263204"
---
# <span data-ttu-id="23147-101">Get-AzPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="23147-101">Get-AzPrivateLinkResource</span></span>

## <span data-ttu-id="23147-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="23147-102">SYNOPSIS</span></span>
<span data-ttu-id="23147-103">Obtém um recurso de link particular.</span><span class="sxs-lookup"><span data-stu-id="23147-103">Gets a private link resource.</span></span>

## <span data-ttu-id="23147-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="23147-104">SYNTAX</span></span>

### <span data-ttu-id="23147-105">ByPrivateLinkResourceId (padrão)</span><span class="sxs-lookup"><span data-stu-id="23147-105">ByPrivateLinkResourceId (Default)</span></span>
```
Get-AzPrivateLinkResource -PrivateLinkResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="23147-106">ByResource</span><span class="sxs-lookup"><span data-stu-id="23147-106">ByResource</span></span>
```
Get-AzPrivateLinkResource -ResourceGroupName <String> -ServiceName <String>
 [-DefaultProfile <IAzureContextContainer>] [-PrivateLinkResourceType <String>] [<CommonParameters>]
```

## <span data-ttu-id="23147-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="23147-107">DESCRIPTION</span></span>
<span data-ttu-id="23147-108">O cmdlet **Get-AzPrivateLinkResource** recupera todos os recursos de link que pertencem ao PrivateLinkResource.</span><span class="sxs-lookup"><span data-stu-id="23147-108">The **Get-AzPrivateLinkResource** cmdlet retrieves all link resources belongs PrivateLinkResource.</span></span>

## <span data-ttu-id="23147-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="23147-109">EXAMPLES</span></span>

### <span data-ttu-id="23147-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="23147-110">Example 1</span></span>
```
Get-AzPrivateLinkResource -PrivateLinkResourceId '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/TestResourceGroup/providers/Microsoft.Sql/servers/mySql'
```

<span data-ttu-id="23147-111">Este exemplo lista todos os recursos de link privado nbelong para o SQL Server chamado mySql.</span><span class="sxs-lookup"><span data-stu-id="23147-111">This example list all private link resources nbelong to sql server named mySql.</span></span>

## <span data-ttu-id="23147-112">OS</span><span class="sxs-lookup"><span data-stu-id="23147-112">PARAMETERS</span></span>

### <span data-ttu-id="23147-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23147-113">-DefaultProfile</span></span>
<span data-ttu-id="23147-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="23147-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="23147-115">-PrivateLinkResourceId</span><span class="sxs-lookup"><span data-stu-id="23147-115">-PrivateLinkResourceId</span></span>
<span data-ttu-id="23147-116">A ID do Gerenciador de recursos do Azure do recurso de link particular.</span><span class="sxs-lookup"><span data-stu-id="23147-116">The Azure resource manager id of the private link resource.</span></span>

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

### <span data-ttu-id="23147-117">-PrivateLinkResourceType</span><span class="sxs-lookup"><span data-stu-id="23147-117">-PrivateLinkResourceType</span></span>
<span data-ttu-id="23147-118">O tipo de recurso de link particular.</span><span class="sxs-lookup"><span data-stu-id="23147-118">The private link resource type.</span></span>

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

### <span data-ttu-id="23147-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="23147-119">-ResourceGroupName</span></span>
<span data-ttu-id="23147-120">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="23147-120">The resource group name.</span></span>

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

### <span data-ttu-id="23147-121">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="23147-121">-ServiceName</span></span>
<span data-ttu-id="23147-122">O nome do serviço de link privado.</span><span class="sxs-lookup"><span data-stu-id="23147-122">The private link service name.</span></span>

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

### <span data-ttu-id="23147-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23147-123">CommonParameters</span></span>
<span data-ttu-id="23147-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="23147-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23147-125">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="23147-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23147-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="23147-126">INPUTS</span></span>

### <span data-ttu-id="23147-127">System. String</span><span class="sxs-lookup"><span data-stu-id="23147-127">System.String</span></span>

## <span data-ttu-id="23147-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="23147-128">OUTPUTS</span></span>

### <span data-ttu-id="23147-129">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="23147-129">System.Boolean</span></span>

## <span data-ttu-id="23147-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="23147-130">NOTES</span></span>

## <span data-ttu-id="23147-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="23147-131">RELATED LINKS</span></span>
