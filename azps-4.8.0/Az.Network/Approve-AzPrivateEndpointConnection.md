---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/approve-azprivateendpointconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Approve-AzPrivateEndpointConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Approve-AzPrivateEndpointConnection.md
ms.openlocfilehash: 8fe3058b122c88448403293ad4f109aa5d62b23f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94114406"
---
# <span data-ttu-id="90b0f-101">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="90b0f-101">Approve-AzPrivateEndpointConnection</span></span>

## <span data-ttu-id="90b0f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="90b0f-102">SYNOPSIS</span></span>
<span data-ttu-id="90b0f-103">Aprova uma conexão de ponto de extremidade particular.</span><span class="sxs-lookup"><span data-stu-id="90b0f-103">Approves a private endpoint connection.</span></span>

## <span data-ttu-id="90b0f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="90b0f-104">SYNTAX</span></span>

### <span data-ttu-id="90b0f-105">ByResourceId (padrão)</span><span class="sxs-lookup"><span data-stu-id="90b0f-105">ByResourceId (Default)</span></span>
```
Approve-AzPrivateEndpointConnection -ResourceId <String> [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="90b0f-106">ByResource</span><span class="sxs-lookup"><span data-stu-id="90b0f-106">ByResource</span></span>
```
Approve-AzPrivateEndpointConnection -Name <String> -ServiceName <String> -ResourceGroupName <String>
 [-PrivateLinkResourceType <string>][-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="90b0f-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="90b0f-107">DESCRIPTION</span></span>
<span data-ttu-id="90b0f-108">O cmdlet **Approve-AzPrivateEndpointConnection** aprova uma conexão de ponto de extremidade particular.</span><span class="sxs-lookup"><span data-stu-id="90b0f-108">The **Approve-AzPrivateEndpointConnection** cmdlet approves a private endpoint connection.</span></span>

## <span data-ttu-id="90b0f-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="90b0f-109">EXAMPLES</span></span>

### <span data-ttu-id="90b0f-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="90b0f-110">Example 1</span></span>
```
Approve-AzPrivateEndpointConnection -Name TestPrivateEndpointConnection -ResourceGroupName TestResourceGroup -ServiceName TestPrivateLinkService
```

<span data-ttu-id="90b0f-111">Este exemplo aprova uma conexão de ponto de extremidade particular.</span><span class="sxs-lookup"><span data-stu-id="90b0f-111">This example approves a private endpoint connection.</span></span>

## <span data-ttu-id="90b0f-112">OS</span><span class="sxs-lookup"><span data-stu-id="90b0f-112">PARAMETERS</span></span>

### <span data-ttu-id="90b0f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90b0f-113">-DefaultProfile</span></span>
<span data-ttu-id="90b0f-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="90b0f-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="90b0f-115">-Descrição</span><span class="sxs-lookup"><span data-stu-id="90b0f-115">-Description</span></span>
<span data-ttu-id="90b0f-116">O motivo da ação.</span><span class="sxs-lookup"><span data-stu-id="90b0f-116">The reason of action.</span></span>

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

### <span data-ttu-id="90b0f-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="90b0f-117">-Name</span></span>
<span data-ttu-id="90b0f-118">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="90b0f-118">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResource
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="90b0f-119">-PrivateLinkResourceType</span><span class="sxs-lookup"><span data-stu-id="90b0f-119">-PrivateLinkResourceType</span></span>
<span data-ttu-id="90b0f-120">O tipo de recurso de link particular.</span><span class="sxs-lookup"><span data-stu-id="90b0f-120">The private link resource type.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResource
Aliases:

Required: False
Position: Named
Default value: 'Microsoft.Network/privateLinkServices'
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="90b0f-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="90b0f-121">-ResourceGroupName</span></span>
<span data-ttu-id="90b0f-122">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="90b0f-122">The resource group name.</span></span>

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

### <span data-ttu-id="90b0f-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="90b0f-123">-ResourceId</span></span>
<span data-ttu-id="90b0f-124">A ID do Gerenciador de recursos do Azure da conexão de ponto de extremidade particular.</span><span class="sxs-lookup"><span data-stu-id="90b0f-124">The Azure resource manager id of the private endpoint connection.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="90b0f-125">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="90b0f-125">-ServiceName</span></span>
<span data-ttu-id="90b0f-126">O nome do serviço de link privado.</span><span class="sxs-lookup"><span data-stu-id="90b0f-126">The private link service name.</span></span>

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


### <span data-ttu-id="90b0f-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90b0f-127">CommonParameters</span></span>
<span data-ttu-id="90b0f-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="90b0f-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90b0f-129">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="90b0f-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90b0f-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="90b0f-130">INPUTS</span></span>

### <span data-ttu-id="90b0f-131">System. String</span><span class="sxs-lookup"><span data-stu-id="90b0f-131">System.String</span></span>

## <span data-ttu-id="90b0f-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="90b0f-132">OUTPUTS</span></span>

### <span data-ttu-id="90b0f-133">Microsoft. Azure. Commands. Network. Models. PSPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="90b0f-133">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span></span>

## <span data-ttu-id="90b0f-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="90b0f-134">NOTES</span></span>

## <span data-ttu-id="90b0f-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="90b0f-135">RELATED LINKS</span></span>

[<span data-ttu-id="90b0f-136">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="90b0f-136">Deny-AzPrivateEndpointConnection</span></span>](./Deny-AzPrivateEndpointConnection.md)

[<span data-ttu-id="90b0f-137">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="90b0f-137">Get-AzPrivateEndpointConnection</span></span>](./Get-AzPrivateEndpointConnection.md)

[<span data-ttu-id="90b0f-138">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="90b0f-138">Remove-AzPrivateEndpointConnection</span></span>](./Remove-AzPrivateEndpointConnection.md)

[<span data-ttu-id="90b0f-139">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="90b0f-139">Set-AzPrivateEndpointConnection</span></span>](./Set-AzPrivateEndpointConnection.md)