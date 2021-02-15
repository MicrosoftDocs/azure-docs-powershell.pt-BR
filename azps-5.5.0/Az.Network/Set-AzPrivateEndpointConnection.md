---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azprivateendpointconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPrivateEndpointConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPrivateEndpointConnection.md
ms.openlocfilehash: b8625e5909ca1928b2e0e828b7ecb83f93252b27
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115056"
---
# <span data-ttu-id="b2769-101">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="b2769-101">Set-AzPrivateEndpointConnection</span></span>

## <span data-ttu-id="b2769-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b2769-102">SYNOPSIS</span></span>
<span data-ttu-id="b2769-103">Atualiza um estado de conexão de ponto de extremidade particular no serviço de link particular.</span><span class="sxs-lookup"><span data-stu-id="b2769-103">Updates a private endpoint connection state on private link service.</span></span>

## <span data-ttu-id="b2769-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b2769-104">SYNTAX</span></span>

### <span data-ttu-id="b2769-105">ByResourceId (Padrão)</span><span class="sxs-lookup"><span data-stu-id="b2769-105">ByResourceId (Default)</span></span>
```
Set-AzPrivateEndpointConnection -ResourceId <String>
 -PrivateLinkServiceConnectionState <String> [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b2769-106">ByResource</span><span class="sxs-lookup"><span data-stu-id="b2769-106">ByResource</span></span>
```
Set-AzPrivateEndpointConnection -Name <String> -ServiceName <String> -ResourceGroupName <String> [-PrivateLinkResourceType <String>]
 -PrivateLinkServiceConnectionState <String> [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b2769-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="b2769-107">DESCRIPTION</span></span>
<span data-ttu-id="b2769-108">O cmdlet **Set-AzPrivateEndpointConnection** atualiza um estado de conexão de ponto de extremidade particular em um serviço de link particular</span><span class="sxs-lookup"><span data-stu-id="b2769-108">The **Set-AzPrivateEndpointConnection** cmdlet updates a private endpoint connection state on a private link service</span></span>

## <span data-ttu-id="b2769-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="b2769-109">EXAMPLES</span></span>

### <span data-ttu-id="b2769-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="b2769-110">Example 1</span></span>
```
Set-AzPrivateEndpointConnection -Name TestPrivateEndpointConnection -ResourceGroupName TestResourceGroup -ServiceName TestPrivateLinkService -PrivateLinkServiceConnectionState "Approved"
```

<span data-ttu-id="b2769-111">Este exemplo atualiza um estado de conexão de ponto de extremidade particular para Aprovado.</span><span class="sxs-lookup"><span data-stu-id="b2769-111">This example updates a private endpoint connection state to Approved.</span></span>

## <span data-ttu-id="b2769-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b2769-112">PARAMETERS</span></span>

### <span data-ttu-id="b2769-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2769-113">-DefaultProfile</span></span>
<span data-ttu-id="b2769-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b2769-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b2769-115">-Descrição</span><span class="sxs-lookup"><span data-stu-id="b2769-115">-Description</span></span>
<span data-ttu-id="b2769-116">O motivo da ação.</span><span class="sxs-lookup"><span data-stu-id="b2769-116">The reason of action.</span></span>

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

### <span data-ttu-id="b2769-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="b2769-117">-Name</span></span>
<span data-ttu-id="b2769-118">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="b2769-118">The resource name.</span></span>

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

### <span data-ttu-id="b2769-119">-PrivateLinkResourceType</span><span class="sxs-lookup"><span data-stu-id="b2769-119">-PrivateLinkResourceType</span></span>
<span data-ttu-id="b2769-120">O tipo de recurso de vínculo privado.</span><span class="sxs-lookup"><span data-stu-id="b2769-120">The private link resource type.</span></span>

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

### <span data-ttu-id="b2769-121">-PrivateLinkServiceConnectionState</span><span class="sxs-lookup"><span data-stu-id="b2769-121">-PrivateLinkServiceConnectionState</span></span>
<span data-ttu-id="b2769-122">Aprovado ou rejeitado o recurso.</span><span class="sxs-lookup"><span data-stu-id="b2769-122">Approved or rejected the resource.</span></span>

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

### <span data-ttu-id="b2769-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b2769-123">-ResourceGroupName</span></span>
<span data-ttu-id="b2769-124">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="b2769-124">The resource group name.</span></span>

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

### <span data-ttu-id="b2769-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b2769-125">-ResourceId</span></span>
<span data-ttu-id="b2769-126">A ID do gerenciador de recursos do Azure da conexão de ponto de extremidade particular.</span><span class="sxs-lookup"><span data-stu-id="b2769-126">The Azure resource manager id of the private endpoint connection.</span></span>

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

### <span data-ttu-id="b2769-127">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="b2769-127">-ServiceName</span></span>
<span data-ttu-id="b2769-128">O nome do serviço de link particular.</span><span class="sxs-lookup"><span data-stu-id="b2769-128">The private link service name.</span></span>

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

### <span data-ttu-id="b2769-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2769-129">CommonParameters</span></span>
<span data-ttu-id="b2769-130">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b2769-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2769-131">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b2769-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2769-132">Entradas</span><span class="sxs-lookup"><span data-stu-id="b2769-132">INPUTS</span></span>

### <span data-ttu-id="b2769-133">System.String</span><span class="sxs-lookup"><span data-stu-id="b2769-133">System.String</span></span>

## <span data-ttu-id="b2769-134">Saídas</span><span class="sxs-lookup"><span data-stu-id="b2769-134">OUTPUTS</span></span>

### <span data-ttu-id="b2769-135">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="b2769-135">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span></span>

## <span data-ttu-id="b2769-136">Notas</span><span class="sxs-lookup"><span data-stu-id="b2769-136">NOTES</span></span>

## <span data-ttu-id="b2769-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b2769-137">RELATED LINKS</span></span>

[<span data-ttu-id="b2769-138">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="b2769-138">Approve-AzPrivateEndpointConnection</span></span>](./Approve-AzPrivateEndpointConnection.md)

[<span data-ttu-id="b2769-139">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="b2769-139">Deny-AzPrivateEndpointConnection</span></span>](./Deny-AzPrivateEndpointConnection.md)

[<span data-ttu-id="b2769-140">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="b2769-140">Get-AzPrivateEndpointConnection</span></span>](./Get-AzPrivateEndpointConnection.md)

[<span data-ttu-id="b2769-141">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="b2769-141">Remove-AzPrivateEndpointConnection</span></span>](./Remove-AzPrivateEndpointConnection.md)