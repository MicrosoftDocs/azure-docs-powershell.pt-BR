---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azprivateendpointconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPrivateEndpointConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPrivateEndpointConnection.md
ms.openlocfilehash: b8625e5909ca1928b2e0e828b7ecb83f93252b27
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "93954765"
---
# <span data-ttu-id="283ea-101">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="283ea-101">Set-AzPrivateEndpointConnection</span></span>

## <span data-ttu-id="283ea-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="283ea-102">SYNOPSIS</span></span>
<span data-ttu-id="283ea-103">Atualiza um estado de conexão de ponto de extremidade privado no serviço de link particular.</span><span class="sxs-lookup"><span data-stu-id="283ea-103">Updates a private endpoint connection state on private link service.</span></span>

## <span data-ttu-id="283ea-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="283ea-104">SYNTAX</span></span>

### <span data-ttu-id="283ea-105">ByResourceId (padrão)</span><span class="sxs-lookup"><span data-stu-id="283ea-105">ByResourceId (Default)</span></span>
```
Set-AzPrivateEndpointConnection -ResourceId <String>
 -PrivateLinkServiceConnectionState <String> [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="283ea-106">ByResource</span><span class="sxs-lookup"><span data-stu-id="283ea-106">ByResource</span></span>
```
Set-AzPrivateEndpointConnection -Name <String> -ServiceName <String> -ResourceGroupName <String> [-PrivateLinkResourceType <String>]
 -PrivateLinkServiceConnectionState <String> [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="283ea-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="283ea-107">DESCRIPTION</span></span>
<span data-ttu-id="283ea-108">O cmdlet **set-AzPrivateEndpointConnection** atualiza um estado de conexão de ponto de extremidade privado em um serviço de link privado</span><span class="sxs-lookup"><span data-stu-id="283ea-108">The **Set-AzPrivateEndpointConnection** cmdlet updates a private endpoint connection state on a private link service</span></span>

## <span data-ttu-id="283ea-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="283ea-109">EXAMPLES</span></span>

### <span data-ttu-id="283ea-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="283ea-110">Example 1</span></span>
```
Set-AzPrivateEndpointConnection -Name TestPrivateEndpointConnection -ResourceGroupName TestResourceGroup -ServiceName TestPrivateLinkService -PrivateLinkServiceConnectionState "Approved"
```

<span data-ttu-id="283ea-111">Este exemplo atualiza um estado de conexão de ponto de extremidade particular para aprovado.</span><span class="sxs-lookup"><span data-stu-id="283ea-111">This example updates a private endpoint connection state to Approved.</span></span>

## <span data-ttu-id="283ea-112">OS</span><span class="sxs-lookup"><span data-stu-id="283ea-112">PARAMETERS</span></span>

### <span data-ttu-id="283ea-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="283ea-113">-DefaultProfile</span></span>
<span data-ttu-id="283ea-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="283ea-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="283ea-115">-Descrição</span><span class="sxs-lookup"><span data-stu-id="283ea-115">-Description</span></span>
<span data-ttu-id="283ea-116">O motivo da ação.</span><span class="sxs-lookup"><span data-stu-id="283ea-116">The reason of action.</span></span>

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

### <span data-ttu-id="283ea-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="283ea-117">-Name</span></span>
<span data-ttu-id="283ea-118">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="283ea-118">The resource name.</span></span>

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

### <span data-ttu-id="283ea-119">-PrivateLinkResourceType</span><span class="sxs-lookup"><span data-stu-id="283ea-119">-PrivateLinkResourceType</span></span>
<span data-ttu-id="283ea-120">O tipo de recurso de link particular.</span><span class="sxs-lookup"><span data-stu-id="283ea-120">The private link resource type.</span></span>

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

### <span data-ttu-id="283ea-121">-PrivateLinkServiceConnectionState</span><span class="sxs-lookup"><span data-stu-id="283ea-121">-PrivateLinkServiceConnectionState</span></span>
<span data-ttu-id="283ea-122">Aprovou ou rejeitou o recurso.</span><span class="sxs-lookup"><span data-stu-id="283ea-122">Approved or rejected the resource.</span></span>

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

### <span data-ttu-id="283ea-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="283ea-123">-ResourceGroupName</span></span>
<span data-ttu-id="283ea-124">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="283ea-124">The resource group name.</span></span>

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

### <span data-ttu-id="283ea-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="283ea-125">-ResourceId</span></span>
<span data-ttu-id="283ea-126">A ID do Gerenciador de recursos do Azure da conexão de ponto de extremidade particular.</span><span class="sxs-lookup"><span data-stu-id="283ea-126">The Azure resource manager id of the private endpoint connection.</span></span>

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

### <span data-ttu-id="283ea-127">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="283ea-127">-ServiceName</span></span>
<span data-ttu-id="283ea-128">O nome do serviço de link privado.</span><span class="sxs-lookup"><span data-stu-id="283ea-128">The private link service name.</span></span>

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

### <span data-ttu-id="283ea-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="283ea-129">CommonParameters</span></span>
<span data-ttu-id="283ea-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="283ea-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="283ea-131">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="283ea-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="283ea-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="283ea-132">INPUTS</span></span>

### <span data-ttu-id="283ea-133">System. String</span><span class="sxs-lookup"><span data-stu-id="283ea-133">System.String</span></span>

## <span data-ttu-id="283ea-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="283ea-134">OUTPUTS</span></span>

### <span data-ttu-id="283ea-135">Microsoft. Azure. Commands. Network. Models. PSPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="283ea-135">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span></span>

## <span data-ttu-id="283ea-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="283ea-136">NOTES</span></span>

## <span data-ttu-id="283ea-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="283ea-137">RELATED LINKS</span></span>

[<span data-ttu-id="283ea-138">Aprovar-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="283ea-138">Approve-AzPrivateEndpointConnection</span></span>](./Approve-AzPrivateEndpointConnection.md)

[<span data-ttu-id="283ea-139">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="283ea-139">Deny-AzPrivateEndpointConnection</span></span>](./Deny-AzPrivateEndpointConnection.md)

[<span data-ttu-id="283ea-140">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="283ea-140">Get-AzPrivateEndpointConnection</span></span>](./Get-AzPrivateEndpointConnection.md)

[<span data-ttu-id="283ea-141">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="283ea-141">Remove-AzPrivateEndpointConnection</span></span>](./Remove-AzPrivateEndpointConnection.md)