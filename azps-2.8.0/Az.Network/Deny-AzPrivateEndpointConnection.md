---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/deny-azprivateendpointconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Deny-AzPrivateEndpointConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Deny-AzPrivateEndpointConnection.md
ms.openlocfilehash: 4a67914fd3709ef972adac8eba6b1b2fa211fbf6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93771817"
---
# <span data-ttu-id="98cbc-101">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="98cbc-101">Deny-AzPrivateEndpointConnection</span></span>

## <span data-ttu-id="98cbc-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="98cbc-102">SYNOPSIS</span></span>
<span data-ttu-id="98cbc-103">nega uma conexão de ponto de extremidade particular.</span><span class="sxs-lookup"><span data-stu-id="98cbc-103">denies a private endpoint connection.</span></span>

## <span data-ttu-id="98cbc-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="98cbc-104">SYNTAX</span></span>

### <span data-ttu-id="98cbc-105">ByResourceId (padrão)</span><span class="sxs-lookup"><span data-stu-id="98cbc-105">ByResourceId (Default)</span></span>
```
Deny-AzPrivateEndpointConnection -ResourceId <String> [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="98cbc-106">ByResource</span><span class="sxs-lookup"><span data-stu-id="98cbc-106">ByResource</span></span>
```
Deny-AzPrivateEndpointConnection -Name <String> -ServiceName <String> -ResourceGroupName <String>
 [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="98cbc-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="98cbc-107">DESCRIPTION</span></span>
<span data-ttu-id="98cbc-108">O cmdlet **Deny-AzPrivateEndpointConnection** nega uma conexão de ponto de extremidade particular.</span><span class="sxs-lookup"><span data-stu-id="98cbc-108">The **Deny-AzPrivateEndpointConnection** cmdlet denies a private endpoint connection.</span></span>

## <span data-ttu-id="98cbc-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="98cbc-109">EXAMPLES</span></span>

### <span data-ttu-id="98cbc-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="98cbc-110">Example 1</span></span>
```
Deny-AzPrivateEndpointConnection -Name TestPrivateEndpointConnection -ResourceGroupName TestResourceGroup -ServiceName TestPrivateLinkService
```

<span data-ttu-id="98cbc-111">Este exemplo nega uma conexão de ponto de extremidade particular.</span><span class="sxs-lookup"><span data-stu-id="98cbc-111">This example denies a private endpoint connection.</span></span>

## <span data-ttu-id="98cbc-112">OS</span><span class="sxs-lookup"><span data-stu-id="98cbc-112">PARAMETERS</span></span>

### <span data-ttu-id="98cbc-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98cbc-113">-DefaultProfile</span></span>
<span data-ttu-id="98cbc-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="98cbc-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="98cbc-115">-Descrição</span><span class="sxs-lookup"><span data-stu-id="98cbc-115">-Description</span></span>
<span data-ttu-id="98cbc-116">O motivo da ação.</span><span class="sxs-lookup"><span data-stu-id="98cbc-116">The reason of action.</span></span>

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

### <span data-ttu-id="98cbc-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="98cbc-117">-Name</span></span>
<span data-ttu-id="98cbc-118">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="98cbc-118">The resource name.</span></span>

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

### <span data-ttu-id="98cbc-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="98cbc-119">-ResourceGroupName</span></span>
<span data-ttu-id="98cbc-120">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="98cbc-120">The resource group name.</span></span>

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

### <span data-ttu-id="98cbc-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="98cbc-121">-ResourceId</span></span>
<span data-ttu-id="98cbc-122">A ID do Gerenciador de recursos do Azure da conexão de ponto de extremidade particular.</span><span class="sxs-lookup"><span data-stu-id="98cbc-122">The Azure resource manager id of the private endpoint connection.</span></span>

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

### <span data-ttu-id="98cbc-123">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="98cbc-123">-ServiceName</span></span>
<span data-ttu-id="98cbc-124">O nome do serviço de link privado.</span><span class="sxs-lookup"><span data-stu-id="98cbc-124">The private link service name.</span></span>

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

### <span data-ttu-id="98cbc-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98cbc-125">CommonParameters</span></span>
<span data-ttu-id="98cbc-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="98cbc-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98cbc-127">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="98cbc-127">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98cbc-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="98cbc-128">INPUTS</span></span>

### <span data-ttu-id="98cbc-129">System. String</span><span class="sxs-lookup"><span data-stu-id="98cbc-129">System.String</span></span>

## <span data-ttu-id="98cbc-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="98cbc-130">OUTPUTS</span></span>

### <span data-ttu-id="98cbc-131">Microsoft. Azure. Commands. Network. Models. PSPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="98cbc-131">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span></span>

## <span data-ttu-id="98cbc-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="98cbc-132">NOTES</span></span>

## <span data-ttu-id="98cbc-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="98cbc-133">RELATED LINKS</span></span>

[<span data-ttu-id="98cbc-134">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="98cbc-134">Get-AzPrivateEndpointConnection</span></span>](./Get-AzPrivateEndpointConnection.md)

[<span data-ttu-id="98cbc-135">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="98cbc-135">Deny-AzPrivateEndpointConnection</span></span>](./Deny-AzPrivateEndpointConnection.md)

[<span data-ttu-id="98cbc-136">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="98cbc-136">Remove-AzPrivateEndpointConnection</span></span>](./Remove-AzPrivateEndpointConnection.md)