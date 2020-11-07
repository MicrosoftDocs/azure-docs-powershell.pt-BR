---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/remove-aziothubroutingendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/IotHub/IotHub/help/Remove-AzIotHubRoutingEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/IotHub/IotHub/help/Remove-AzIotHubRoutingEndpoint.md
ms.openlocfilehash: 781959d3e8738af8c3520cf99762dfa5714a23c6
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93775817"
---
# <span data-ttu-id="a0bdb-101">Remove-AzIotHubRoutingEndpoint</span><span class="sxs-lookup"><span data-stu-id="a0bdb-101">Remove-AzIotHubRoutingEndpoint</span></span>

## <span data-ttu-id="a0bdb-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a0bdb-102">SYNOPSIS</span></span>
<span data-ttu-id="a0bdb-103">Excluir um ponto de extremidade para o seu hub IoT</span><span class="sxs-lookup"><span data-stu-id="a0bdb-103">Delete an endpoint for your IoT Hub</span></span>

## <span data-ttu-id="a0bdb-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a0bdb-104">SYNTAX</span></span>

### <span data-ttu-id="a0bdb-105">ResourceSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="a0bdb-105">ResourceSet (Default)</span></span>
```
Remove-AzIotHubRoutingEndpoint [-ResourceGroupName] <String> [-Name] <String> [-EndpointName <String>]
 [-EndpointType <PSEndpointType>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a0bdb-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="a0bdb-106">InputObjectSet</span></span>
```
Remove-AzIotHubRoutingEndpoint [-InputObject] <PSIotHub> [-EndpointName <String>]
 [-EndpointType <PSEndpointType>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a0bdb-107">ResourceSet</span><span class="sxs-lookup"><span data-stu-id="a0bdb-107">ResourceIdSet</span></span>
```
Remove-AzIotHubRoutingEndpoint [-ResourceId] <String> [-EndpointName <String>] [-EndpointType <PSEndpointType>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a0bdb-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a0bdb-108">DESCRIPTION</span></span>
<span data-ttu-id="a0bdb-109">Excluir um ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="a0bdb-109">Delete an endpoint.</span></span> <span data-ttu-id="a0bdb-110">Lembre-se de excluir qualquer rota que use esse ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="a0bdb-110">Remember to delete any routes that use this endpoint.</span></span>

## <span data-ttu-id="a0bdb-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a0bdb-111">EXAMPLES</span></span>

### <span data-ttu-id="a0bdb-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="a0bdb-112">Example 1</span></span>
```
PS C:\> Remove-AzIotHubRoutingEndpoint -ResourceGroupName "myresourcegroup" -Name "myiothub" -EndpointName E2 -PassThru

True
```

<span data-ttu-id="a0bdb-113">Exclua o ponto de extremidade "E2" do Hub IoT "myiothub".</span><span class="sxs-lookup"><span data-stu-id="a0bdb-113">Delete endpoint "E2" from "myiothub" IoT Hub.</span></span>

## <span data-ttu-id="a0bdb-114">OS</span><span class="sxs-lookup"><span data-stu-id="a0bdb-114">PARAMETERS</span></span>

### <span data-ttu-id="a0bdb-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0bdb-115">-DefaultProfile</span></span>
<span data-ttu-id="a0bdb-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a0bdb-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a0bdb-117">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="a0bdb-117">-EndpointName</span></span>
<span data-ttu-id="a0bdb-118">Nome do ponto de extremidade de roteamento</span><span class="sxs-lookup"><span data-stu-id="a0bdb-118">Name of the Routing Endpoint</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0bdb-119">-EndpointType</span><span class="sxs-lookup"><span data-stu-id="a0bdb-119">-EndpointType</span></span>
<span data-ttu-id="a0bdb-120">Tipo de ponto de extremidade de roteamento</span><span class="sxs-lookup"><span data-stu-id="a0bdb-120">Type of the Routing Endpoint</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSEndpointType
Parameter Sets: (All)
Aliases:
Accepted values: EventHub, ServiceBusQueue, ServiceBusTopic, AzureStorageContainer

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0bdb-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a0bdb-121">-InputObject</span></span>
<span data-ttu-id="a0bdb-122">Objeto IotHub</span><span class="sxs-lookup"><span data-stu-id="a0bdb-122">IotHub Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub
Parameter Sets: InputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a0bdb-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="a0bdb-123">-Name</span></span>
<span data-ttu-id="a0bdb-124">Nome do Hub IOT</span><span class="sxs-lookup"><span data-stu-id="a0bdb-124">Name of the Iot Hub</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0bdb-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a0bdb-125">-PassThru</span></span>
<span data-ttu-id="a0bdb-126">Permite retornar o objeto booliano.</span><span class="sxs-lookup"><span data-stu-id="a0bdb-126">Allows to return the boolean object.</span></span> <span data-ttu-id="a0bdb-127">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="a0bdb-127">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0bdb-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a0bdb-128">-ResourceGroupName</span></span>
<span data-ttu-id="a0bdb-129">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="a0bdb-129">Name of the Resource Group</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0bdb-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a0bdb-130">-ResourceId</span></span>
<span data-ttu-id="a0bdb-131">ID do recurso IotHub</span><span class="sxs-lookup"><span data-stu-id="a0bdb-131">IotHub Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a0bdb-132">-Confirme</span><span class="sxs-lookup"><span data-stu-id="a0bdb-132">-Confirm</span></span>
<span data-ttu-id="a0bdb-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a0bdb-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0bdb-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a0bdb-134">-WhatIf</span></span>
<span data-ttu-id="a0bdb-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="a0bdb-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a0bdb-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a0bdb-136">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0bdb-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0bdb-137">CommonParameters</span></span>
<span data-ttu-id="a0bdb-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a0bdb-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0bdb-139">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a0bdb-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0bdb-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a0bdb-140">INPUTS</span></span>

### <span data-ttu-id="a0bdb-141">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="a0bdb-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="a0bdb-142">System. String</span><span class="sxs-lookup"><span data-stu-id="a0bdb-142">System.String</span></span>

## <span data-ttu-id="a0bdb-143">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a0bdb-143">OUTPUTS</span></span>

### <span data-ttu-id="a0bdb-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a0bdb-144">System.Boolean</span></span>

## <span data-ttu-id="a0bdb-145">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a0bdb-145">NOTES</span></span>

## <span data-ttu-id="a0bdb-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a0bdb-146">RELATED LINKS</span></span>
