---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azprivateendpointconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateEndpointConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateEndpointConnection.md
ms.openlocfilehash: 30b156a7adc972d06e514dd3d8d27c40f41194df
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93943308"
---
# <span data-ttu-id="8348c-101">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="8348c-101">Get-AzPrivateEndpointConnection</span></span>

## <span data-ttu-id="8348c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8348c-102">SYNOPSIS</span></span>
<span data-ttu-id="8348c-103">Obtém um recurso de conexão de ponto de extremidade particular.</span><span class="sxs-lookup"><span data-stu-id="8348c-103">Gets a private endpoint connection resource.</span></span>

## <span data-ttu-id="8348c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8348c-104">SYNTAX</span></span>

### <span data-ttu-id="8348c-105">ByPrivateLinkResourceId (padrão)</span><span class="sxs-lookup"><span data-stu-id="8348c-105">ByPrivateLinkResourceId (Default)</span></span>
```
Get-AzPrivateEndpointConnection -PrivateLinkResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8348c-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="8348c-106">ByResourceId</span></span>
```
Get-AzPrivateEndpointConnection -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8348c-107">ByResource</span><span class="sxs-lookup"><span data-stu-id="8348c-107">ByResource</span></span>
```
Get-AzPrivateEndpointConnection -ServiceName <String> -ResourceGroupName <String>
[-Name <String>] [-PrivateLinkResourceType <String>] [-Description <String>]
[-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8348c-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8348c-108">DESCRIPTION</span></span>
<span data-ttu-id="8348c-109">O cmdlet **Get-AzPrivateEndpointConnection** recupera um recurso de conexão de ponto de extremidade particular.</span><span class="sxs-lookup"><span data-stu-id="8348c-109">The **Get-AzPrivateEndpointConnection** cmdlet retrieves a private endpoint connection resource.</span></span>

## <span data-ttu-id="8348c-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8348c-110">EXAMPLES</span></span>

### <span data-ttu-id="8348c-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="8348c-111">Example 1</span></span>
```
Get-AzPrivateEndpointConnection -PrivateLinkResourceId '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/TestResourceGroup/providers/Microsoft.Sql/servers/mySql'
```

<span data-ttu-id="8348c-112">Este exemplo retorna uma lista de todas as conexões de ponto de extremidade privadas pertencentes ao SQL Server chamado mysql.</span><span class="sxs-lookup"><span data-stu-id="8348c-112">This example return a list of all private endpoint connections belongs to sql server named Mysql.</span></span>

### <span data-ttu-id="8348c-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="8348c-113">Example 2</span></span>
```
Get-AzPrivateEndpointConnection -Name MyPrivateEndpointConnection1 -ResourceGroupName TestResourceGroup -ServiceName MyPrivateLinkService -PrivateLinkResourceType 'Microsoft.Network/privateLinkServices'
```

<span data-ttu-id="8348c-114">Este exemplo obtém uma conexão de ponto de extremidade privada chamada MyPrivateEndpointConnection1 pertence ao serviço de link privado chamado MyPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="8348c-114">This example get a private endpoint connection named MyPrivateEndpointConnection1 belongs to private link service named MyPrivateLinkService</span></span>

## <span data-ttu-id="8348c-115">OS</span><span class="sxs-lookup"><span data-stu-id="8348c-115">PARAMETERS</span></span>

### <span data-ttu-id="8348c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8348c-116">-DefaultProfile</span></span>
<span data-ttu-id="8348c-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8348c-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8348c-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="8348c-118">-Name</span></span>
<span data-ttu-id="8348c-119">O nome da conexão de ponto de extremidade particular.</span><span class="sxs-lookup"><span data-stu-id="8348c-119">The name of the private endpoint connection.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResource
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8348c-120">-PrivateLinkResourceId</span><span class="sxs-lookup"><span data-stu-id="8348c-120">-PrivateLinkResourceId</span></span>
<span data-ttu-id="8348c-121">A ID do recurso de link privado do recurso de link privado do Azure Resource Manager ao qual a conexão de ponto de extremidade privada pertence.</span><span class="sxs-lookup"><span data-stu-id="8348c-121">The Azure resource manager id of the private link resource that private endpoint connection belongs to.</span></span>

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

### <span data-ttu-id="8348c-122">-PrivateLinkResourceType</span><span class="sxs-lookup"><span data-stu-id="8348c-122">-PrivateLinkResourceType</span></span>
<span data-ttu-id="8348c-123">O tipo de recurso de link particular.</span><span class="sxs-lookup"><span data-stu-id="8348c-123">The private link resource type.</span></span>

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

### <span data-ttu-id="8348c-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8348c-124">-ResourceGroupName</span></span>
<span data-ttu-id="8348c-125">O nome do grupo de recursos da conexão de ponto de extremidade particular.</span><span class="sxs-lookup"><span data-stu-id="8348c-125">The resource group name of the private endpoint connection.</span></span>

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

### <span data-ttu-id="8348c-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8348c-126">-ResourceId</span></span>
<span data-ttu-id="8348c-127">A ID do Gerenciador de recursos do Azure da conexão de ponto de extremidade particular.</span><span class="sxs-lookup"><span data-stu-id="8348c-127">The Azure resource manager id of the private endpoint connection.</span></span>

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

### <span data-ttu-id="8348c-128">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="8348c-128">-ServiceName</span></span>
<span data-ttu-id="8348c-129">O nome do serviço ao qual pertence a conexão de ponto de extremidade privada.</span><span class="sxs-lookup"><span data-stu-id="8348c-129">The name of service that the private endpoint connection belong to.</span></span>

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

### <span data-ttu-id="8348c-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8348c-130">CommonParameters</span></span>
<span data-ttu-id="8348c-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8348c-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8348c-132">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8348c-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8348c-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8348c-133">INPUTS</span></span>

### <span data-ttu-id="8348c-134">System. String</span><span class="sxs-lookup"><span data-stu-id="8348c-134">System.String</span></span>

## <span data-ttu-id="8348c-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8348c-135">OUTPUTS</span></span>

### <span data-ttu-id="8348c-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="8348c-136">System.Boolean</span></span>

## <span data-ttu-id="8348c-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8348c-137">NOTES</span></span>

## <span data-ttu-id="8348c-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8348c-138">RELATED LINKS</span></span>

[<span data-ttu-id="8348c-139">Aprovar-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="8348c-139">Approve-AzPrivateEndpointConnection</span></span>](./Approve-AzPrivateEndpointConnection.md)

[<span data-ttu-id="8348c-140">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="8348c-140">Deny-AzPrivateEndpointConnection</span></span>](./Deny-AzPrivateEndpointConnection.md)

[<span data-ttu-id="8348c-141">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="8348c-141">Remove-AzPrivateEndpointConnection</span></span>](./Remove-AzPrivateEndpointConnection.md)

[<span data-ttu-id="8348c-142">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="8348c-142">Set-AzPrivateEndpointConnection</span></span>](./Set-AzPrivateEndpointConnection.md)
