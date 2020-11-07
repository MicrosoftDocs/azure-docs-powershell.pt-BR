---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/remove-aziothubroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/IotHub/IotHub/help/Remove-AzIotHubRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/IotHub/IotHub/help/Remove-AzIotHubRoute.md
ms.openlocfilehash: 1066c922e24f8a521ac7a52bab437812a7733021
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93775820"
---
# <span data-ttu-id="c03e6-101">Remove-AzIotHubRoute</span><span class="sxs-lookup"><span data-stu-id="c03e6-101">Remove-AzIotHubRoute</span></span>

## <span data-ttu-id="c03e6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c03e6-102">SYNOPSIS</span></span>
<span data-ttu-id="c03e6-103">Excluir uma rota no Hub IoT</span><span class="sxs-lookup"><span data-stu-id="c03e6-103">Delete a route in IoT Hub</span></span>

## <span data-ttu-id="c03e6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c03e6-104">SYNTAX</span></span>

### <span data-ttu-id="c03e6-105">ResourceSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="c03e6-105">ResourceSet (Default)</span></span>
```
Remove-AzIotHubRoute [-ResourceGroupName] <String> [-Name] <String> [-RouteName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c03e6-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="c03e6-106">InputObjectSet</span></span>
```
Remove-AzIotHubRoute [-InputObject] <PSIotHub> [-RouteName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c03e6-107">ResourceSet</span><span class="sxs-lookup"><span data-stu-id="c03e6-107">ResourceIdSet</span></span>
```
Remove-AzIotHubRoute [-ResourceId] <String> [-RouteName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c03e6-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c03e6-108">DESCRIPTION</span></span>
<span data-ttu-id="c03e6-109">Excluir rotas para um ponto de extremidade</span><span class="sxs-lookup"><span data-stu-id="c03e6-109">Delete a routes to an endpoint</span></span>

## <span data-ttu-id="c03e6-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c03e6-110">EXAMPLES</span></span>

### <span data-ttu-id="c03e6-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="c03e6-111">Example 1</span></span>
```
PS C:\> Remove-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -RouteName R1 -PassThru

True
```

<span data-ttu-id="c03e6-112">Excluir rota "R1" do Hub IoT "myiothub".</span><span class="sxs-lookup"><span data-stu-id="c03e6-112">Delete route "R1" from "myiothub" IoT Hub.</span></span>

## <span data-ttu-id="c03e6-113">OS</span><span class="sxs-lookup"><span data-stu-id="c03e6-113">PARAMETERS</span></span>

### <span data-ttu-id="c03e6-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c03e6-114">-DefaultProfile</span></span>
<span data-ttu-id="c03e6-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c03e6-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c03e6-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c03e6-116">-InputObject</span></span>
<span data-ttu-id="c03e6-117">Objeto IotHub</span><span class="sxs-lookup"><span data-stu-id="c03e6-117">IotHub Object</span></span>

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

### <span data-ttu-id="c03e6-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="c03e6-118">-Name</span></span>
<span data-ttu-id="c03e6-119">Nome do Hub IOT</span><span class="sxs-lookup"><span data-stu-id="c03e6-119">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="c03e6-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c03e6-120">-PassThru</span></span>
<span data-ttu-id="c03e6-121">Permite retornar o objeto booliano.</span><span class="sxs-lookup"><span data-stu-id="c03e6-121">Allows to return the boolean object.</span></span> <span data-ttu-id="c03e6-122">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="c03e6-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="c03e6-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c03e6-123">-ResourceGroupName</span></span>
<span data-ttu-id="c03e6-124">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="c03e6-124">Name of the Resource Group</span></span>

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

### <span data-ttu-id="c03e6-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c03e6-125">-ResourceId</span></span>
<span data-ttu-id="c03e6-126">ID do recurso IotHub</span><span class="sxs-lookup"><span data-stu-id="c03e6-126">IotHub Resource Id</span></span>

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

### <span data-ttu-id="c03e6-127">-RouteName</span><span class="sxs-lookup"><span data-stu-id="c03e6-127">-RouteName</span></span>
<span data-ttu-id="c03e6-128">Nome da rota</span><span class="sxs-lookup"><span data-stu-id="c03e6-128">Name of the Route</span></span>

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

### <span data-ttu-id="c03e6-129">-Confirme</span><span class="sxs-lookup"><span data-stu-id="c03e6-129">-Confirm</span></span>
<span data-ttu-id="c03e6-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c03e6-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c03e6-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c03e6-131">-WhatIf</span></span>
<span data-ttu-id="c03e6-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="c03e6-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c03e6-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c03e6-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c03e6-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c03e6-134">CommonParameters</span></span>
<span data-ttu-id="c03e6-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c03e6-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c03e6-136">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c03e6-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c03e6-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c03e6-137">INPUTS</span></span>

### <span data-ttu-id="c03e6-138">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="c03e6-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="c03e6-139">System. String</span><span class="sxs-lookup"><span data-stu-id="c03e6-139">System.String</span></span>

## <span data-ttu-id="c03e6-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c03e6-140">OUTPUTS</span></span>

### <span data-ttu-id="c03e6-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c03e6-141">System.Boolean</span></span>

## <span data-ttu-id="c03e6-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c03e6-142">NOTES</span></span>

## <span data-ttu-id="c03e6-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c03e6-143">RELATED LINKS</span></span>