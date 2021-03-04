---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/set-azprivateendpointconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPrivateEndpointConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPrivateEndpointConnection.md
ms.openlocfilehash: 7684072abbef4af8344cc07aa4bef6cab88ad3ed
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888821"
---
# <span data-ttu-id="7405e-101">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="7405e-101">Set-AzPrivateEndpointConnection</span></span>

## <span data-ttu-id="7405e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7405e-102">SYNOPSIS</span></span>
<span data-ttu-id="7405e-103">Atualiza um estado de conexão de ponto de extremidade privado no serviço de link privado.</span><span class="sxs-lookup"><span data-stu-id="7405e-103">Updates a private endpoint connection state on private link service.</span></span>

## <span data-ttu-id="7405e-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="7405e-104">SYNTAX</span></span>

### <span data-ttu-id="7405e-105">ByResourceId (Padrão)</span><span class="sxs-lookup"><span data-stu-id="7405e-105">ByResourceId (Default)</span></span>
```
Set-AzPrivateEndpointConnection -ResourceId <String>
 -PrivateLinkServiceConnectionState <String> [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7405e-106">ByResource</span><span class="sxs-lookup"><span data-stu-id="7405e-106">ByResource</span></span>
```
Set-AzPrivateEndpointConnection -Name <String> -ServiceName <String> -ResourceGroupName <String> [-PrivateLinkResourceType <String>]
 -PrivateLinkServiceConnectionState <String> [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7405e-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="7405e-107">DESCRIPTION</span></span>
<span data-ttu-id="7405e-108">O cmdlet **Set-AzPrivateEndpointConnection** atualiza um estado de conexão de ponto de extremidade privado em um serviço de link privado</span><span class="sxs-lookup"><span data-stu-id="7405e-108">The **Set-AzPrivateEndpointConnection** cmdlet updates a private endpoint connection state on a private link service</span></span>

## <span data-ttu-id="7405e-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7405e-109">EXAMPLES</span></span>

### <span data-ttu-id="7405e-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="7405e-110">Example 1</span></span>
```
Set-AzPrivateEndpointConnection -Name TestPrivateEndpointConnection -ResourceGroupName TestResourceGroup -ServiceName TestPrivateLinkService -PrivateLinkServiceConnectionState "Approved"
```

<span data-ttu-id="7405e-111">Este exemplo atualiza um estado de conexão de ponto de extremidade privado para Aprovado.</span><span class="sxs-lookup"><span data-stu-id="7405e-111">This example updates a private endpoint connection state to Approved.</span></span>

## <span data-ttu-id="7405e-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="7405e-112">PARAMETERS</span></span>

### <span data-ttu-id="7405e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7405e-113">-DefaultProfile</span></span>
<span data-ttu-id="7405e-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7405e-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7405e-115">-Description</span><span class="sxs-lookup"><span data-stu-id="7405e-115">-Description</span></span>
<span data-ttu-id="7405e-116">O motivo da ação.</span><span class="sxs-lookup"><span data-stu-id="7405e-116">The reason of action.</span></span>

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

### <span data-ttu-id="7405e-117">-Name</span><span class="sxs-lookup"><span data-stu-id="7405e-117">-Name</span></span>
<span data-ttu-id="7405e-118">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="7405e-118">The resource name.</span></span>

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

### <span data-ttu-id="7405e-119">-PrivateLinkResourceType</span><span class="sxs-lookup"><span data-stu-id="7405e-119">-PrivateLinkResourceType</span></span>
<span data-ttu-id="7405e-120">O tipo de recurso de link privado.</span><span class="sxs-lookup"><span data-stu-id="7405e-120">The private link resource type.</span></span>

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

### <span data-ttu-id="7405e-121">-PrivateLinkServiceConnectionState</span><span class="sxs-lookup"><span data-stu-id="7405e-121">-PrivateLinkServiceConnectionState</span></span>
<span data-ttu-id="7405e-122">Aprovado ou rejeitado pelo recurso.</span><span class="sxs-lookup"><span data-stu-id="7405e-122">Approved or rejected the resource.</span></span>

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

### <span data-ttu-id="7405e-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7405e-123">-ResourceGroupName</span></span>
<span data-ttu-id="7405e-124">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="7405e-124">The resource group name.</span></span>

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

### <span data-ttu-id="7405e-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7405e-125">-ResourceId</span></span>
<span data-ttu-id="7405e-126">A ID do gerenciador de recursos do Azure da conexão de ponto de extremidade privada.</span><span class="sxs-lookup"><span data-stu-id="7405e-126">The Azure resource manager id of the private endpoint connection.</span></span>

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

### <span data-ttu-id="7405e-127">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="7405e-127">-ServiceName</span></span>
<span data-ttu-id="7405e-128">O nome do serviço de link privado.</span><span class="sxs-lookup"><span data-stu-id="7405e-128">The private link service name.</span></span>

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

### <span data-ttu-id="7405e-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7405e-129">CommonParameters</span></span>
<span data-ttu-id="7405e-130">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7405e-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7405e-131">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7405e-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7405e-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7405e-132">INPUTS</span></span>

### <span data-ttu-id="7405e-133">System.String</span><span class="sxs-lookup"><span data-stu-id="7405e-133">System.String</span></span>

## <span data-ttu-id="7405e-134">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="7405e-134">OUTPUTS</span></span>

### <span data-ttu-id="7405e-135">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="7405e-135">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span></span>

## <span data-ttu-id="7405e-136">NOTES</span><span class="sxs-lookup"><span data-stu-id="7405e-136">NOTES</span></span>

## <span data-ttu-id="7405e-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7405e-137">RELATED LINKS</span></span>

[<span data-ttu-id="7405e-138">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="7405e-138">Approve-AzPrivateEndpointConnection</span></span>](./Approve-AzPrivateEndpointConnection.md)

[<span data-ttu-id="7405e-139">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="7405e-139">Deny-AzPrivateEndpointConnection</span></span>](./Deny-AzPrivateEndpointConnection.md)

[<span data-ttu-id="7405e-140">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="7405e-140">Get-AzPrivateEndpointConnection</span></span>](./Get-AzPrivateEndpointConnection.md)

[<span data-ttu-id="7405e-141">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="7405e-141">Remove-AzPrivateEndpointConnection</span></span>](./Remove-AzPrivateEndpointConnection.md)