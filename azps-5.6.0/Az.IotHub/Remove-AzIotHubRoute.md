---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/remove-aziothubroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubRoute.md
ms.openlocfilehash: 0ce0a651444bd30a1bf6c766083b0a8584c5cd71
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891021"
---
# <span data-ttu-id="7c881-101">Remove-AzIotHubRoute</span><span class="sxs-lookup"><span data-stu-id="7c881-101">Remove-AzIotHubRoute</span></span>

## <span data-ttu-id="7c881-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7c881-102">SYNOPSIS</span></span>
<span data-ttu-id="7c881-103">Excluir uma rota no Hub IoT</span><span class="sxs-lookup"><span data-stu-id="7c881-103">Delete a route in IoT Hub</span></span>

## <span data-ttu-id="7c881-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="7c881-104">SYNTAX</span></span>

### <span data-ttu-id="7c881-105">ResourceSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="7c881-105">ResourceSet (Default)</span></span>
```
Remove-AzIotHubRoute [-ResourceGroupName] <String> [-Name] <String> [-RouteName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7c881-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="7c881-106">InputObjectSet</span></span>
```
Remove-AzIotHubRoute [-InputObject] <PSIotHub> [-RouteName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7c881-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="7c881-107">ResourceIdSet</span></span>
```
Remove-AzIotHubRoute [-ResourceId] <String> [-RouteName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7c881-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="7c881-108">DESCRIPTION</span></span>
<span data-ttu-id="7c881-109">Excluir rotas para um ponto de extremidade</span><span class="sxs-lookup"><span data-stu-id="7c881-109">Delete a routes to an endpoint</span></span>

## <span data-ttu-id="7c881-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7c881-110">EXAMPLES</span></span>

### <span data-ttu-id="7c881-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="7c881-111">Example 1</span></span>
```
PS C:\> Remove-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -RouteName R1 -PassThru

True
```

<span data-ttu-id="7c881-112">Excluir rota "R1" do Hub de IoT "myiothub".</span><span class="sxs-lookup"><span data-stu-id="7c881-112">Delete route "R1" from "myiothub" IoT Hub.</span></span>

## <span data-ttu-id="7c881-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="7c881-113">PARAMETERS</span></span>

### <span data-ttu-id="7c881-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c881-114">-DefaultProfile</span></span>
<span data-ttu-id="7c881-115">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7c881-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7c881-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7c881-116">-InputObject</span></span>
<span data-ttu-id="7c881-117">Objeto IotHub</span><span class="sxs-lookup"><span data-stu-id="7c881-117">IotHub Object</span></span>

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

### <span data-ttu-id="7c881-118">-Name</span><span class="sxs-lookup"><span data-stu-id="7c881-118">-Name</span></span>
<span data-ttu-id="7c881-119">Nome do Hub de Iot</span><span class="sxs-lookup"><span data-stu-id="7c881-119">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="7c881-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7c881-120">-PassThru</span></span>
<span data-ttu-id="7c881-121">Permite retornar o objeto booleano.</span><span class="sxs-lookup"><span data-stu-id="7c881-121">Allows to return the boolean object.</span></span> <span data-ttu-id="7c881-122">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="7c881-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="7c881-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7c881-123">-ResourceGroupName</span></span>
<span data-ttu-id="7c881-124">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="7c881-124">Name of the Resource Group</span></span>

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

### <span data-ttu-id="7c881-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7c881-125">-ResourceId</span></span>
<span data-ttu-id="7c881-126">Id de Recurso IotHub</span><span class="sxs-lookup"><span data-stu-id="7c881-126">IotHub Resource Id</span></span>

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

### <span data-ttu-id="7c881-127">-RouteName</span><span class="sxs-lookup"><span data-stu-id="7c881-127">-RouteName</span></span>
<span data-ttu-id="7c881-128">Nome da rota</span><span class="sxs-lookup"><span data-stu-id="7c881-128">Name of the Route</span></span>

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

### <span data-ttu-id="7c881-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7c881-129">-Confirm</span></span>
<span data-ttu-id="7c881-130">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7c881-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7c881-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7c881-131">-WhatIf</span></span>
<span data-ttu-id="7c881-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="7c881-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7c881-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="7c881-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7c881-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c881-134">CommonParameters</span></span>
<span data-ttu-id="7c881-135">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7c881-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c881-136">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7c881-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c881-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7c881-137">INPUTS</span></span>

### <span data-ttu-id="7c881-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="7c881-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="7c881-139">System.String</span><span class="sxs-lookup"><span data-stu-id="7c881-139">System.String</span></span>

## <span data-ttu-id="7c881-140">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="7c881-140">OUTPUTS</span></span>

### <span data-ttu-id="7c881-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="7c881-141">System.Boolean</span></span>

## <span data-ttu-id="7c881-142">NOTES</span><span class="sxs-lookup"><span data-stu-id="7c881-142">NOTES</span></span>

## <span data-ttu-id="7c881-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7c881-143">RELATED LINKS</span></span>
