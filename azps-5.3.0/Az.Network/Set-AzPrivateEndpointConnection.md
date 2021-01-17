---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azprivateendpointconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPrivateEndpointConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPrivateEndpointConnection.md
ms.openlocfilehash: b8625e5909ca1928b2e0e828b7ecb83f93252b27
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98433387"
---
# <span data-ttu-id="a7397-101">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="a7397-101">Set-AzPrivateEndpointConnection</span></span>

## <span data-ttu-id="a7397-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a7397-102">SYNOPSIS</span></span>
<span data-ttu-id="a7397-103">Atualiza um estado de conexão de ponto de extremidade privado no serviço de link particular.</span><span class="sxs-lookup"><span data-stu-id="a7397-103">Updates a private endpoint connection state on private link service.</span></span>

## <span data-ttu-id="a7397-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a7397-104">SYNTAX</span></span>

### <span data-ttu-id="a7397-105">ByResourceId (padrão)</span><span class="sxs-lookup"><span data-stu-id="a7397-105">ByResourceId (Default)</span></span>
```
Set-AzPrivateEndpointConnection -ResourceId <String>
 -PrivateLinkServiceConnectionState <String> [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a7397-106">ByResource</span><span class="sxs-lookup"><span data-stu-id="a7397-106">ByResource</span></span>
```
Set-AzPrivateEndpointConnection -Name <String> -ServiceName <String> -ResourceGroupName <String> [-PrivateLinkResourceType <String>]
 -PrivateLinkServiceConnectionState <String> [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a7397-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a7397-107">DESCRIPTION</span></span>
<span data-ttu-id="a7397-108">O cmdlet **set-AzPrivateEndpointConnection** atualiza um estado de conexão de ponto de extremidade privado em um serviço de link privado</span><span class="sxs-lookup"><span data-stu-id="a7397-108">The **Set-AzPrivateEndpointConnection** cmdlet updates a private endpoint connection state on a private link service</span></span>

## <span data-ttu-id="a7397-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a7397-109">EXAMPLES</span></span>

### <span data-ttu-id="a7397-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="a7397-110">Example 1</span></span>
```
Set-AzPrivateEndpointConnection -Name TestPrivateEndpointConnection -ResourceGroupName TestResourceGroup -ServiceName TestPrivateLinkService -PrivateLinkServiceConnectionState "Approved"
```

<span data-ttu-id="a7397-111">Este exemplo atualiza um estado de conexão de ponto de extremidade particular para aprovado.</span><span class="sxs-lookup"><span data-stu-id="a7397-111">This example updates a private endpoint connection state to Approved.</span></span>

## <span data-ttu-id="a7397-112">OS</span><span class="sxs-lookup"><span data-stu-id="a7397-112">PARAMETERS</span></span>

### <span data-ttu-id="a7397-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7397-113">-DefaultProfile</span></span>
<span data-ttu-id="a7397-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a7397-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a7397-115">-Descrição</span><span class="sxs-lookup"><span data-stu-id="a7397-115">-Description</span></span>
<span data-ttu-id="a7397-116">O motivo da ação.</span><span class="sxs-lookup"><span data-stu-id="a7397-116">The reason of action.</span></span>

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

### <span data-ttu-id="a7397-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="a7397-117">-Name</span></span>
<span data-ttu-id="a7397-118">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="a7397-118">The resource name.</span></span>

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

### <span data-ttu-id="a7397-119">-PrivateLinkResourceType</span><span class="sxs-lookup"><span data-stu-id="a7397-119">-PrivateLinkResourceType</span></span>
<span data-ttu-id="a7397-120">O tipo de recurso de link particular.</span><span class="sxs-lookup"><span data-stu-id="a7397-120">The private link resource type.</span></span>

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

### <span data-ttu-id="a7397-121">-PrivateLinkServiceConnectionState</span><span class="sxs-lookup"><span data-stu-id="a7397-121">-PrivateLinkServiceConnectionState</span></span>
<span data-ttu-id="a7397-122">Aprovou ou rejeitou o recurso.</span><span class="sxs-lookup"><span data-stu-id="a7397-122">Approved or rejected the resource.</span></span>

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

### <span data-ttu-id="a7397-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a7397-123">-ResourceGroupName</span></span>
<span data-ttu-id="a7397-124">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="a7397-124">The resource group name.</span></span>

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

### <span data-ttu-id="a7397-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a7397-125">-ResourceId</span></span>
<span data-ttu-id="a7397-126">A ID do Gerenciador de recursos do Azure da conexão de ponto de extremidade particular.</span><span class="sxs-lookup"><span data-stu-id="a7397-126">The Azure resource manager id of the private endpoint connection.</span></span>

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

### <span data-ttu-id="a7397-127">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="a7397-127">-ServiceName</span></span>
<span data-ttu-id="a7397-128">O nome do serviço de link privado.</span><span class="sxs-lookup"><span data-stu-id="a7397-128">The private link service name.</span></span>

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

### <span data-ttu-id="a7397-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7397-129">CommonParameters</span></span>
<span data-ttu-id="a7397-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a7397-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7397-131">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a7397-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7397-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a7397-132">INPUTS</span></span>

### <span data-ttu-id="a7397-133">System. String</span><span class="sxs-lookup"><span data-stu-id="a7397-133">System.String</span></span>

## <span data-ttu-id="a7397-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a7397-134">OUTPUTS</span></span>

### <span data-ttu-id="a7397-135">Microsoft. Azure. Commands. Network. Models. PSPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="a7397-135">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span></span>

## <span data-ttu-id="a7397-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a7397-136">NOTES</span></span>

## <span data-ttu-id="a7397-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a7397-137">RELATED LINKS</span></span>

[<span data-ttu-id="a7397-138">Aprovar-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="a7397-138">Approve-AzPrivateEndpointConnection</span></span>](./Approve-AzPrivateEndpointConnection.md)

[<span data-ttu-id="a7397-139">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="a7397-139">Deny-AzPrivateEndpointConnection</span></span>](./Deny-AzPrivateEndpointConnection.md)

[<span data-ttu-id="a7397-140">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="a7397-140">Get-AzPrivateEndpointConnection</span></span>](./Get-AzPrivateEndpointConnection.md)

[<span data-ttu-id="a7397-141">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="a7397-141">Remove-AzPrivateEndpointConnection</span></span>](./Remove-AzPrivateEndpointConnection.md)