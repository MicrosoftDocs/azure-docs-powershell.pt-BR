---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azprivateendpointconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateEndpointConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateEndpointConnection.md
ms.openlocfilehash: d2df4f7f5ed073d357daa1113a8e0c7477a05cce
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101885663"
---
# <span data-ttu-id="0c289-101">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="0c289-101">Get-AzPrivateEndpointConnection</span></span>

## <span data-ttu-id="0c289-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0c289-102">SYNOPSIS</span></span>
<span data-ttu-id="0c289-103">Obtém um recurso de conexão de ponto de extremidade privado.</span><span class="sxs-lookup"><span data-stu-id="0c289-103">Gets a private endpoint connection resource.</span></span>

## <span data-ttu-id="0c289-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="0c289-104">SYNTAX</span></span>

### <span data-ttu-id="0c289-105">ByResourceId (Padrão)</span><span class="sxs-lookup"><span data-stu-id="0c289-105">ByResourceId (Default)</span></span>
```
Get-AzPrivateEndpointConnection [-Description <String>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0c289-106">ByPrivateLinkResourceId</span><span class="sxs-lookup"><span data-stu-id="0c289-106">ByPrivateLinkResourceId</span></span>
```
Get-AzPrivateEndpointConnection -PrivateLinkResourceId <String> [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0c289-107">ByResource</span><span class="sxs-lookup"><span data-stu-id="0c289-107">ByResource</span></span>
```
Get-AzPrivateEndpointConnection [-Description <String>] [-Name <String>] -ResourceGroupName <String>
 -ServiceName <String> [-DefaultProfile <IAzureContextContainer>] [-PrivateLinkResourceType <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="0c289-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="0c289-108">DESCRIPTION</span></span>
<span data-ttu-id="0c289-109">O cmdlet **Get-AzPrivateEndpointConnection** recupera um recurso de conexão de ponto de extremidade privado.</span><span class="sxs-lookup"><span data-stu-id="0c289-109">The **Get-AzPrivateEndpointConnection** cmdlet retrieves a private endpoint connection resource.</span></span>

## <span data-ttu-id="0c289-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0c289-110">EXAMPLES</span></span>

### <span data-ttu-id="0c289-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="0c289-111">Example 1</span></span>
```
Get-AzPrivateEndpointConnection -PrivateLinkResourceId '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/TestResourceGroup/providers/Microsoft.Sql/servers/mySql'
```

<span data-ttu-id="0c289-112">Este exemplo retorna uma lista de todas as conexões de ponto de extremidade privadas que pertencem ao sql server chamado Mysql.</span><span class="sxs-lookup"><span data-stu-id="0c289-112">This example return a list of all private endpoint connections belongs to sql server named Mysql.</span></span>

### <span data-ttu-id="0c289-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="0c289-113">Example 2</span></span>
```
Get-AzPrivateEndpointConnection -Name MyPrivateEndpointConnection1 -ResourceGroupName TestResourceGroup -ServiceName MyPrivateLinkService -PrivateLinkResourceType 'Microsoft.Network/privateLinkServices'
```

<span data-ttu-id="0c289-114">Este exemplo obter uma conexão de ponto de extremidade privada chamada MyPrivateEndpointConnection1 pertence a um serviço de link privado chamado MyPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="0c289-114">This example get a private endpoint connection named MyPrivateEndpointConnection1 belongs to private link service named MyPrivateLinkService</span></span>

## <span data-ttu-id="0c289-115">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="0c289-115">PARAMETERS</span></span>

### <span data-ttu-id="0c289-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c289-116">-DefaultProfile</span></span>
<span data-ttu-id="0c289-117">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0c289-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0c289-118">-Description</span><span class="sxs-lookup"><span data-stu-id="0c289-118">-Description</span></span>
<span data-ttu-id="0c289-119">O motivo da ação.</span><span class="sxs-lookup"><span data-stu-id="0c289-119">The reason of action.</span></span>

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

### <span data-ttu-id="0c289-120">-Name</span><span class="sxs-lookup"><span data-stu-id="0c289-120">-Name</span></span>
<span data-ttu-id="0c289-121">O nome da conexão de ponto de extremidade privada.</span><span class="sxs-lookup"><span data-stu-id="0c289-121">The name of the private endpoint connection.</span></span>

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

### <span data-ttu-id="0c289-122">-PrivateLinkResourceId</span><span class="sxs-lookup"><span data-stu-id="0c289-122">-PrivateLinkResourceId</span></span>
<span data-ttu-id="0c289-123">A ID do gerenciador de recursos do Azure do recurso de link privado que a conexão de ponto de extremidade privada pertence.</span><span class="sxs-lookup"><span data-stu-id="0c289-123">The Azure resource manager id of the private link resource that private endpoint connection belongs to.</span></span>

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

### <span data-ttu-id="0c289-124">-PrivateLinkResourceType</span><span class="sxs-lookup"><span data-stu-id="0c289-124">-PrivateLinkResourceType</span></span>
<span data-ttu-id="0c289-125">O tipo de recurso de link privado.</span><span class="sxs-lookup"><span data-stu-id="0c289-125">The private link resource type.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResource
Aliases:
Accepted values: 

Required: False
Position: Named
Default value: 'Microsoft.Network/privateLinkServices'
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0c289-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0c289-126">-ResourceGroupName</span></span>
<span data-ttu-id="0c289-127">O nome do grupo de recursos da conexão de ponto de extremidade privada.</span><span class="sxs-lookup"><span data-stu-id="0c289-127">The resource group name of the private endpoint connection.</span></span>

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

### <span data-ttu-id="0c289-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0c289-128">-ResourceId</span></span>
<span data-ttu-id="0c289-129">A ID do gerenciador de recursos do Azure da conexão de ponto de extremidade privada.</span><span class="sxs-lookup"><span data-stu-id="0c289-129">The Azure resource manager id of the private endpoint connection.</span></span>

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

### <span data-ttu-id="0c289-130">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="0c289-130">-ServiceName</span></span>
<span data-ttu-id="0c289-131">O nome do serviço ao que a conexão de ponto de extremidade privada pertence.</span><span class="sxs-lookup"><span data-stu-id="0c289-131">The name of service that the private endpoint connection belong to.</span></span>

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

### <span data-ttu-id="0c289-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c289-132">CommonParameters</span></span>
<span data-ttu-id="0c289-133">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0c289-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c289-134">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0c289-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c289-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0c289-135">INPUTS</span></span>

### <span data-ttu-id="0c289-136">System.String</span><span class="sxs-lookup"><span data-stu-id="0c289-136">System.String</span></span>

## <span data-ttu-id="0c289-137">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="0c289-137">OUTPUTS</span></span>

### <span data-ttu-id="0c289-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="0c289-138">System.Boolean</span></span>

## <span data-ttu-id="0c289-139">NOTES</span><span class="sxs-lookup"><span data-stu-id="0c289-139">NOTES</span></span>

## <span data-ttu-id="0c289-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0c289-140">RELATED LINKS</span></span>

[<span data-ttu-id="0c289-141">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="0c289-141">Approve-AzPrivateEndpointConnection</span></span>](./Approve-AzPrivateEndpointConnection.md)

[<span data-ttu-id="0c289-142">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="0c289-142">Deny-AzPrivateEndpointConnection</span></span>](./Deny-AzPrivateEndpointConnection.md)

[<span data-ttu-id="0c289-143">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="0c289-143">Remove-AzPrivateEndpointConnection</span></span>](./Remove-AzPrivateEndpointConnection.md)

[<span data-ttu-id="0c289-144">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="0c289-144">Set-AzPrivateEndpointConnection</span></span>](./Set-AzPrivateEndpointConnection.md)
