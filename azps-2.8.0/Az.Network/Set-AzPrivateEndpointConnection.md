---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azprivateendpointconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPrivateEndpointConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPrivateEndpointConnection.md
ms.openlocfilehash: 588402480cbd626a747208705ec59fd10c572075
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93772757"
---
# <span data-ttu-id="dd1ff-101">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="dd1ff-101">Set-AzPrivateEndpointConnection</span></span>

## <span data-ttu-id="dd1ff-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="dd1ff-102">SYNOPSIS</span></span>
<span data-ttu-id="dd1ff-103">Atualiza um estado de conexão de ponto de extremidade privado no serviço de link particular.</span><span class="sxs-lookup"><span data-stu-id="dd1ff-103">Updates a private endpoint connection state on private link service.</span></span>

## <span data-ttu-id="dd1ff-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="dd1ff-104">SYNTAX</span></span>

```
Set-AzPrivateEndpointConnection -Name <String> -ServiceName <String> -ResourceGroupName <String>
 -PrivateLinkServiceConnectionState <String> [-Description <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="dd1ff-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="dd1ff-105">DESCRIPTION</span></span>
<span data-ttu-id="dd1ff-106">O cmdlet **set-AzPrivateEndpointConnection** atualiza um estado de conexão de ponto de extremidade privado em um serviço de link privado</span><span class="sxs-lookup"><span data-stu-id="dd1ff-106">The **Set-AzPrivateEndpointConnection** cmdlet updates a private endpoint connection state on a private link service</span></span>

## <span data-ttu-id="dd1ff-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="dd1ff-107">EXAMPLES</span></span>

### <span data-ttu-id="dd1ff-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="dd1ff-108">Example 1</span></span>
```
Set-AzPrivateEndpointConnection -Name TestPrivateEndpointConnection -ResourceGroupName TestResourceGroup -ServiceName TestPrivateLinkService -PrivateLinkServiceConnectionState "Approved"
```

<span data-ttu-id="dd1ff-109">Este exemplo atualiza um estado de conexão de ponto de extremidade particular para aprovado.</span><span class="sxs-lookup"><span data-stu-id="dd1ff-109">This example updates a private endpoint connection state to Approved.</span></span>

## <span data-ttu-id="dd1ff-110">OS</span><span class="sxs-lookup"><span data-stu-id="dd1ff-110">PARAMETERS</span></span>

### <span data-ttu-id="dd1ff-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd1ff-111">-DefaultProfile</span></span>
<span data-ttu-id="dd1ff-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="dd1ff-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dd1ff-113">-Descrição</span><span class="sxs-lookup"><span data-stu-id="dd1ff-113">-Description</span></span>
<span data-ttu-id="dd1ff-114">O motivo da ação.</span><span class="sxs-lookup"><span data-stu-id="dd1ff-114">The reason of action.</span></span>

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

### <span data-ttu-id="dd1ff-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="dd1ff-115">-Name</span></span>
<span data-ttu-id="dd1ff-116">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="dd1ff-116">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dd1ff-117">-PrivateLinkServiceConnectionState</span><span class="sxs-lookup"><span data-stu-id="dd1ff-117">-PrivateLinkServiceConnectionState</span></span>
<span data-ttu-id="dd1ff-118">Aprovou ou rejeitou o recurso.</span><span class="sxs-lookup"><span data-stu-id="dd1ff-118">Approved or rejected the resource.</span></span>

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

### <span data-ttu-id="dd1ff-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dd1ff-119">-ResourceGroupName</span></span>
<span data-ttu-id="dd1ff-120">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="dd1ff-120">The resource group name.</span></span>

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

### <span data-ttu-id="dd1ff-121">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="dd1ff-121">-ServiceName</span></span>
<span data-ttu-id="dd1ff-122">O nome do serviço de link privado.</span><span class="sxs-lookup"><span data-stu-id="dd1ff-122">The private link service name.</span></span>

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

### <span data-ttu-id="dd1ff-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd1ff-123">CommonParameters</span></span>
<span data-ttu-id="dd1ff-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dd1ff-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd1ff-125">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="dd1ff-125">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd1ff-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="dd1ff-126">INPUTS</span></span>

### <span data-ttu-id="dd1ff-127">System. String</span><span class="sxs-lookup"><span data-stu-id="dd1ff-127">System.String</span></span>

## <span data-ttu-id="dd1ff-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="dd1ff-128">OUTPUTS</span></span>

### <span data-ttu-id="dd1ff-129">Microsoft. Azure. Commands. Network. Models. PSPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="dd1ff-129">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span></span>

## <span data-ttu-id="dd1ff-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="dd1ff-130">NOTES</span></span>

## <span data-ttu-id="dd1ff-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="dd1ff-131">RELATED LINKS</span></span>
