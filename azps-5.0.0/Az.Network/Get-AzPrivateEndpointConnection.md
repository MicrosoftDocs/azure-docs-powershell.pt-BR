---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azprivateendpointconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateEndpointConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateEndpointConnection.md
ms.openlocfilehash: 102ee966ae8ed213f1ed00395612061d1b39a3eb
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94282222"
---
# <span data-ttu-id="77f4f-101">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="77f4f-101">Get-AzPrivateEndpointConnection</span></span>

## <span data-ttu-id="77f4f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="77f4f-102">SYNOPSIS</span></span>
<span data-ttu-id="77f4f-103">Obtém um recurso de conexão de ponto de extremidade particular.</span><span class="sxs-lookup"><span data-stu-id="77f4f-103">Gets a private endpoint connection resource.</span></span>

## <span data-ttu-id="77f4f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="77f4f-104">SYNTAX</span></span>

### <span data-ttu-id="77f4f-105">ByResourceId (padrão)</span><span class="sxs-lookup"><span data-stu-id="77f4f-105">ByResourceId (Default)</span></span>
```
Get-AzPrivateEndpointConnection [-Description <String>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="77f4f-106">ByPrivateLinkResourceId</span><span class="sxs-lookup"><span data-stu-id="77f4f-106">ByPrivateLinkResourceId</span></span>
```
Get-AzPrivateEndpointConnection -PrivateLinkResourceId <String> [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="77f4f-107">ByResource</span><span class="sxs-lookup"><span data-stu-id="77f4f-107">ByResource</span></span>
```
Get-AzPrivateEndpointConnection [-Description <String>] [-Name <String>] -ResourceGroupName <String>
 -ServiceName <String> [-DefaultProfile <IAzureContextContainer>] [-PrivateLinkResourceType <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="77f4f-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="77f4f-108">DESCRIPTION</span></span>
<span data-ttu-id="77f4f-109">O cmdlet **Get-AzPrivateEndpointConnection** recupera um recurso de conexão de ponto de extremidade particular.</span><span class="sxs-lookup"><span data-stu-id="77f4f-109">The **Get-AzPrivateEndpointConnection** cmdlet retrieves a private endpoint connection resource.</span></span>

## <span data-ttu-id="77f4f-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="77f4f-110">EXAMPLES</span></span>

### <span data-ttu-id="77f4f-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="77f4f-111">Example 1</span></span>
```
Get-AzPrivateEndpointConnection -PrivateLinkResourceId '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/TestResourceGroup/providers/Microsoft.Sql/servers/mySql'
```

<span data-ttu-id="77f4f-112">Este exemplo retorna uma lista de todas as conexões de ponto de extremidade privadas pertencentes ao SQL Server chamado mysql.</span><span class="sxs-lookup"><span data-stu-id="77f4f-112">This example return a list of all private endpoint connections belongs to sql server named Mysql.</span></span>

### <span data-ttu-id="77f4f-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="77f4f-113">Example 2</span></span>
```
Get-AzPrivateEndpointConnection -Name MyPrivateEndpointConnection1 -ResourceGroupName TestResourceGroup -ServiceName MyPrivateLinkService -PrivateLinkResourceType 'Microsoft.Network/privateLinkServices'
```

<span data-ttu-id="77f4f-114">Este exemplo obtém uma conexão de ponto de extremidade privada chamada MyPrivateEndpointConnection1 pertence ao serviço de link privado chamado MyPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="77f4f-114">This example get a private endpoint connection named MyPrivateEndpointConnection1 belongs to private link service named MyPrivateLinkService</span></span>

## <span data-ttu-id="77f4f-115">OS</span><span class="sxs-lookup"><span data-stu-id="77f4f-115">PARAMETERS</span></span>

### <span data-ttu-id="77f4f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77f4f-116">-DefaultProfile</span></span>
<span data-ttu-id="77f4f-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="77f4f-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="77f4f-118">-Descrição</span><span class="sxs-lookup"><span data-stu-id="77f4f-118">-Description</span></span>
<span data-ttu-id="77f4f-119">O motivo da ação.</span><span class="sxs-lookup"><span data-stu-id="77f4f-119">The reason of action.</span></span>

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

### <span data-ttu-id="77f4f-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="77f4f-120">-Name</span></span>
<span data-ttu-id="77f4f-121">O nome da conexão de ponto de extremidade particular.</span><span class="sxs-lookup"><span data-stu-id="77f4f-121">The name of the private endpoint connection.</span></span>

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

### <span data-ttu-id="77f4f-122">-PrivateLinkResourceId</span><span class="sxs-lookup"><span data-stu-id="77f4f-122">-PrivateLinkResourceId</span></span>
<span data-ttu-id="77f4f-123">A ID do recurso de link privado do recurso de link privado do Azure Resource Manager ao qual a conexão de ponto de extremidade privada pertence.</span><span class="sxs-lookup"><span data-stu-id="77f4f-123">The Azure resource manager id of the private link resource that private endpoint connection belongs to.</span></span>

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

### <span data-ttu-id="77f4f-124">-PrivateLinkResourceType</span><span class="sxs-lookup"><span data-stu-id="77f4f-124">-PrivateLinkResourceType</span></span>
<span data-ttu-id="77f4f-125">O tipo de recurso de link particular.</span><span class="sxs-lookup"><span data-stu-id="77f4f-125">The private link resource type.</span></span>

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

### <span data-ttu-id="77f4f-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="77f4f-126">-ResourceGroupName</span></span>
<span data-ttu-id="77f4f-127">O nome do grupo de recursos da conexão de ponto de extremidade particular.</span><span class="sxs-lookup"><span data-stu-id="77f4f-127">The resource group name of the private endpoint connection.</span></span>

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

### <span data-ttu-id="77f4f-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="77f4f-128">-ResourceId</span></span>
<span data-ttu-id="77f4f-129">A ID do Gerenciador de recursos do Azure da conexão de ponto de extremidade particular.</span><span class="sxs-lookup"><span data-stu-id="77f4f-129">The Azure resource manager id of the private endpoint connection.</span></span>

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

### <span data-ttu-id="77f4f-130">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="77f4f-130">-ServiceName</span></span>
<span data-ttu-id="77f4f-131">O nome do serviço ao qual pertence a conexão de ponto de extremidade privada.</span><span class="sxs-lookup"><span data-stu-id="77f4f-131">The name of service that the private endpoint connection belong to.</span></span>

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

### <span data-ttu-id="77f4f-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77f4f-132">CommonParameters</span></span>
<span data-ttu-id="77f4f-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="77f4f-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77f4f-134">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="77f4f-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77f4f-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="77f4f-135">INPUTS</span></span>

### <span data-ttu-id="77f4f-136">System. String</span><span class="sxs-lookup"><span data-stu-id="77f4f-136">System.String</span></span>

## <span data-ttu-id="77f4f-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="77f4f-137">OUTPUTS</span></span>

### <span data-ttu-id="77f4f-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="77f4f-138">System.Boolean</span></span>

## <span data-ttu-id="77f4f-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="77f4f-139">NOTES</span></span>

## <span data-ttu-id="77f4f-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="77f4f-140">RELATED LINKS</span></span>

[<span data-ttu-id="77f4f-141">Aprovar-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="77f4f-141">Approve-AzPrivateEndpointConnection</span></span>](./Approve-AzPrivateEndpointConnection.md)

[<span data-ttu-id="77f4f-142">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="77f4f-142">Deny-AzPrivateEndpointConnection</span></span>](./Deny-AzPrivateEndpointConnection.md)

[<span data-ttu-id="77f4f-143">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="77f4f-143">Remove-AzPrivateEndpointConnection</span></span>](./Remove-AzPrivateEndpointConnection.md)

[<span data-ttu-id="77f4f-144">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="77f4f-144">Set-AzPrivateEndpointConnection</span></span>](./Set-AzPrivateEndpointConnection.md)
