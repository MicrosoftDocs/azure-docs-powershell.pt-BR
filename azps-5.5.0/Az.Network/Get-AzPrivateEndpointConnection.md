---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azprivateendpointconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateEndpointConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateEndpointConnection.md
ms.openlocfilehash: 102ee966ae8ed213f1ed00395612061d1b39a3eb
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112899"
---
# <span data-ttu-id="49c87-101">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="49c87-101">Get-AzPrivateEndpointConnection</span></span>

## <span data-ttu-id="49c87-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="49c87-102">SYNOPSIS</span></span>
<span data-ttu-id="49c87-103">Obtém um recurso de conexão de ponto de extremidade particular.</span><span class="sxs-lookup"><span data-stu-id="49c87-103">Gets a private endpoint connection resource.</span></span>

## <span data-ttu-id="49c87-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="49c87-104">SYNTAX</span></span>

### <span data-ttu-id="49c87-105">ByResourceId (Padrão)</span><span class="sxs-lookup"><span data-stu-id="49c87-105">ByResourceId (Default)</span></span>
```
Get-AzPrivateEndpointConnection [-Description <String>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="49c87-106">ByPrivateLinkResourceId</span><span class="sxs-lookup"><span data-stu-id="49c87-106">ByPrivateLinkResourceId</span></span>
```
Get-AzPrivateEndpointConnection -PrivateLinkResourceId <String> [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="49c87-107">ByResource</span><span class="sxs-lookup"><span data-stu-id="49c87-107">ByResource</span></span>
```
Get-AzPrivateEndpointConnection [-Description <String>] [-Name <String>] -ResourceGroupName <String>
 -ServiceName <String> [-DefaultProfile <IAzureContextContainer>] [-PrivateLinkResourceType <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="49c87-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="49c87-108">DESCRIPTION</span></span>
<span data-ttu-id="49c87-109">O cmdlet **Get-AzPrivateEndpointConnection** recupera um recurso de conexão de ponto de extremidade particular.</span><span class="sxs-lookup"><span data-stu-id="49c87-109">The **Get-AzPrivateEndpointConnection** cmdlet retrieves a private endpoint connection resource.</span></span>

## <span data-ttu-id="49c87-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="49c87-110">EXAMPLES</span></span>

### <span data-ttu-id="49c87-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="49c87-111">Example 1</span></span>
```
Get-AzPrivateEndpointConnection -PrivateLinkResourceId '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/TestResourceGroup/providers/Microsoft.Sql/servers/mySql'
```

<span data-ttu-id="49c87-112">Este exemplo retorna uma lista de todas as conexões privadas do ponto de extremidade que pertencem ao sql server chamado Mysql.</span><span class="sxs-lookup"><span data-stu-id="49c87-112">This example return a list of all private endpoint connections belongs to sql server named Mysql.</span></span>

### <span data-ttu-id="49c87-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="49c87-113">Example 2</span></span>
```
Get-AzPrivateEndpointConnection -Name MyPrivateEndpointConnection1 -ResourceGroupName TestResourceGroup -ServiceName MyPrivateLinkService -PrivateLinkResourceType 'Microsoft.Network/privateLinkServices'
```

<span data-ttu-id="49c87-114">Este exemplo obter uma conexão de ponto de extremidade particular chamada MyPrivateEndpointConnection1 pertence ao serviço de link particular chamado MyPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="49c87-114">This example get a private endpoint connection named MyPrivateEndpointConnection1 belongs to private link service named MyPrivateLinkService</span></span>

## <span data-ttu-id="49c87-115">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="49c87-115">PARAMETERS</span></span>

### <span data-ttu-id="49c87-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49c87-116">-DefaultProfile</span></span>
<span data-ttu-id="49c87-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="49c87-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="49c87-118">-Descrição</span><span class="sxs-lookup"><span data-stu-id="49c87-118">-Description</span></span>
<span data-ttu-id="49c87-119">O motivo da ação.</span><span class="sxs-lookup"><span data-stu-id="49c87-119">The reason of action.</span></span>

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

### <span data-ttu-id="49c87-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="49c87-120">-Name</span></span>
<span data-ttu-id="49c87-121">O nome da conexão de ponto de extremidade particular.</span><span class="sxs-lookup"><span data-stu-id="49c87-121">The name of the private endpoint connection.</span></span>

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

### <span data-ttu-id="49c87-122">-PrivateLinkResourceId</span><span class="sxs-lookup"><span data-stu-id="49c87-122">-PrivateLinkResourceId</span></span>
<span data-ttu-id="49c87-123">A ID do gerenciador de recursos do Azure do recurso de link privado ao que a conexão de ponto de extremidade particular pertence.</span><span class="sxs-lookup"><span data-stu-id="49c87-123">The Azure resource manager id of the private link resource that private endpoint connection belongs to.</span></span>

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

### <span data-ttu-id="49c87-124">-PrivateLinkResourceType</span><span class="sxs-lookup"><span data-stu-id="49c87-124">-PrivateLinkResourceType</span></span>
<span data-ttu-id="49c87-125">O tipo de recurso de vínculo privado.</span><span class="sxs-lookup"><span data-stu-id="49c87-125">The private link resource type.</span></span>

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

### <span data-ttu-id="49c87-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="49c87-126">-ResourceGroupName</span></span>
<span data-ttu-id="49c87-127">O nome do grupo de recursos da conexão de ponto de extremidade particular.</span><span class="sxs-lookup"><span data-stu-id="49c87-127">The resource group name of the private endpoint connection.</span></span>

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

### <span data-ttu-id="49c87-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="49c87-128">-ResourceId</span></span>
<span data-ttu-id="49c87-129">A ID do gerenciador de recursos do Azure da conexão de ponto de extremidade particular.</span><span class="sxs-lookup"><span data-stu-id="49c87-129">The Azure resource manager id of the private endpoint connection.</span></span>

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

### <span data-ttu-id="49c87-130">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="49c87-130">-ServiceName</span></span>
<span data-ttu-id="49c87-131">O nome do serviço ao que a conexão de ponto de extremidade particular pertence.</span><span class="sxs-lookup"><span data-stu-id="49c87-131">The name of service that the private endpoint connection belong to.</span></span>

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

### <span data-ttu-id="49c87-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49c87-132">CommonParameters</span></span>
<span data-ttu-id="49c87-133">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="49c87-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49c87-134">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="49c87-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49c87-135">Entradas</span><span class="sxs-lookup"><span data-stu-id="49c87-135">INPUTS</span></span>

### <span data-ttu-id="49c87-136">System.String</span><span class="sxs-lookup"><span data-stu-id="49c87-136">System.String</span></span>

## <span data-ttu-id="49c87-137">Saídas</span><span class="sxs-lookup"><span data-stu-id="49c87-137">OUTPUTS</span></span>

### <span data-ttu-id="49c87-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="49c87-138">System.Boolean</span></span>

## <span data-ttu-id="49c87-139">Notas</span><span class="sxs-lookup"><span data-stu-id="49c87-139">NOTES</span></span>

## <span data-ttu-id="49c87-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="49c87-140">RELATED LINKS</span></span>

[<span data-ttu-id="49c87-141">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="49c87-141">Approve-AzPrivateEndpointConnection</span></span>](./Approve-AzPrivateEndpointConnection.md)

[<span data-ttu-id="49c87-142">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="49c87-142">Deny-AzPrivateEndpointConnection</span></span>](./Deny-AzPrivateEndpointConnection.md)

[<span data-ttu-id="49c87-143">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="49c87-143">Remove-AzPrivateEndpointConnection</span></span>](./Remove-AzPrivateEndpointConnection.md)

[<span data-ttu-id="49c87-144">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="49c87-144">Set-AzPrivateEndpointConnection</span></span>](./Set-AzPrivateEndpointConnection.md)
