---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/remove-aziothubroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubRoute.md
ms.openlocfilehash: b729aa9bab91f5a977d827de6bd83828166ba103
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98272813"
---
# <span data-ttu-id="bb21d-101">Remove-AzIotHubRoute</span><span class="sxs-lookup"><span data-stu-id="bb21d-101">Remove-AzIotHubRoute</span></span>

## <span data-ttu-id="bb21d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="bb21d-102">SYNOPSIS</span></span>
<span data-ttu-id="bb21d-103">Excluir uma rota no Hub IoT</span><span class="sxs-lookup"><span data-stu-id="bb21d-103">Delete a route in IoT Hub</span></span>

## <span data-ttu-id="bb21d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bb21d-104">SYNTAX</span></span>

### <span data-ttu-id="bb21d-105">ResourceSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="bb21d-105">ResourceSet (Default)</span></span>
```
Remove-AzIotHubRoute [-ResourceGroupName] <String> [-Name] <String> [-RouteName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bb21d-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="bb21d-106">InputObjectSet</span></span>
```
Remove-AzIotHubRoute [-InputObject] <PSIotHub> [-RouteName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bb21d-107">ResourceSet</span><span class="sxs-lookup"><span data-stu-id="bb21d-107">ResourceIdSet</span></span>
```
Remove-AzIotHubRoute [-ResourceId] <String> [-RouteName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bb21d-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="bb21d-108">DESCRIPTION</span></span>
<span data-ttu-id="bb21d-109">Excluir rotas para um ponto de extremidade</span><span class="sxs-lookup"><span data-stu-id="bb21d-109">Delete a routes to an endpoint</span></span>

## <span data-ttu-id="bb21d-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="bb21d-110">EXAMPLES</span></span>

### <span data-ttu-id="bb21d-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="bb21d-111">Example 1</span></span>
```
PS C:\> Remove-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -RouteName R1 -PassThru

True
```

<span data-ttu-id="bb21d-112">Excluir rota "R1" do Hub IoT "myiothub".</span><span class="sxs-lookup"><span data-stu-id="bb21d-112">Delete route "R1" from "myiothub" IoT Hub.</span></span>

## <span data-ttu-id="bb21d-113">OS</span><span class="sxs-lookup"><span data-stu-id="bb21d-113">PARAMETERS</span></span>

### <span data-ttu-id="bb21d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb21d-114">-DefaultProfile</span></span>
<span data-ttu-id="bb21d-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="bb21d-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bb21d-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bb21d-116">-InputObject</span></span>
<span data-ttu-id="bb21d-117">Objeto IotHub</span><span class="sxs-lookup"><span data-stu-id="bb21d-117">IotHub Object</span></span>

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

### <span data-ttu-id="bb21d-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="bb21d-118">-Name</span></span>
<span data-ttu-id="bb21d-119">Nome do Hub IOT</span><span class="sxs-lookup"><span data-stu-id="bb21d-119">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="bb21d-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bb21d-120">-PassThru</span></span>
<span data-ttu-id="bb21d-121">Permite retornar o objeto booliano.</span><span class="sxs-lookup"><span data-stu-id="bb21d-121">Allows to return the boolean object.</span></span> <span data-ttu-id="bb21d-122">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="bb21d-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="bb21d-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bb21d-123">-ResourceGroupName</span></span>
<span data-ttu-id="bb21d-124">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="bb21d-124">Name of the Resource Group</span></span>

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

### <span data-ttu-id="bb21d-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bb21d-125">-ResourceId</span></span>
<span data-ttu-id="bb21d-126">ID do recurso IotHub</span><span class="sxs-lookup"><span data-stu-id="bb21d-126">IotHub Resource Id</span></span>

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

### <span data-ttu-id="bb21d-127">-RouteName</span><span class="sxs-lookup"><span data-stu-id="bb21d-127">-RouteName</span></span>
<span data-ttu-id="bb21d-128">Nome da rota</span><span class="sxs-lookup"><span data-stu-id="bb21d-128">Name of the Route</span></span>

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

### <span data-ttu-id="bb21d-129">-Confirme</span><span class="sxs-lookup"><span data-stu-id="bb21d-129">-Confirm</span></span>
<span data-ttu-id="bb21d-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bb21d-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bb21d-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bb21d-131">-WhatIf</span></span>
<span data-ttu-id="bb21d-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="bb21d-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bb21d-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="bb21d-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bb21d-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb21d-134">CommonParameters</span></span>
<span data-ttu-id="bb21d-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bb21d-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb21d-136">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bb21d-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb21d-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="bb21d-137">INPUTS</span></span>

### <span data-ttu-id="bb21d-138">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="bb21d-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="bb21d-139">System. String</span><span class="sxs-lookup"><span data-stu-id="bb21d-139">System.String</span></span>

## <span data-ttu-id="bb21d-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="bb21d-140">OUTPUTS</span></span>

### <span data-ttu-id="bb21d-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="bb21d-141">System.Boolean</span></span>

## <span data-ttu-id="bb21d-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="bb21d-142">NOTES</span></span>

## <span data-ttu-id="bb21d-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bb21d-143">RELATED LINKS</span></span>
