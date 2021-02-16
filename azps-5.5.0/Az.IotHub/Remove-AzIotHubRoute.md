---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/remove-aziothubroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubRoute.md
ms.openlocfilehash: b729aa9bab91f5a977d827de6bd83828166ba103
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113126"
---
# <span data-ttu-id="be1ad-101">Remove-AzIotHubRoute</span><span class="sxs-lookup"><span data-stu-id="be1ad-101">Remove-AzIotHubRoute</span></span>

## <span data-ttu-id="be1ad-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="be1ad-102">SYNOPSIS</span></span>
<span data-ttu-id="be1ad-103">Excluir uma rota no Hub de IoT</span><span class="sxs-lookup"><span data-stu-id="be1ad-103">Delete a route in IoT Hub</span></span>

## <span data-ttu-id="be1ad-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="be1ad-104">SYNTAX</span></span>

### <span data-ttu-id="be1ad-105">ResourceSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="be1ad-105">ResourceSet (Default)</span></span>
```
Remove-AzIotHubRoute [-ResourceGroupName] <String> [-Name] <String> [-RouteName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="be1ad-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="be1ad-106">InputObjectSet</span></span>
```
Remove-AzIotHubRoute [-InputObject] <PSIotHub> [-RouteName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="be1ad-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="be1ad-107">ResourceIdSet</span></span>
```
Remove-AzIotHubRoute [-ResourceId] <String> [-RouteName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="be1ad-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="be1ad-108">DESCRIPTION</span></span>
<span data-ttu-id="be1ad-109">Excluir rotas para um ponto de extremidade</span><span class="sxs-lookup"><span data-stu-id="be1ad-109">Delete a routes to an endpoint</span></span>

## <span data-ttu-id="be1ad-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="be1ad-110">EXAMPLES</span></span>

### <span data-ttu-id="be1ad-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="be1ad-111">Example 1</span></span>
```
PS C:\> Remove-AzIotHubRoute -ResourceGroupName "myresourcegroup" -Name "myiothub" -RouteName R1 -PassThru

True
```

<span data-ttu-id="be1ad-112">Exclua a rota "R1" do Hub de IoT do "myiothub".</span><span class="sxs-lookup"><span data-stu-id="be1ad-112">Delete route "R1" from "myiothub" IoT Hub.</span></span>

## <span data-ttu-id="be1ad-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="be1ad-113">PARAMETERS</span></span>

### <span data-ttu-id="be1ad-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be1ad-114">-DefaultProfile</span></span>
<span data-ttu-id="be1ad-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="be1ad-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="be1ad-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="be1ad-116">-InputObject</span></span>
<span data-ttu-id="be1ad-117">Objeto IotHub</span><span class="sxs-lookup"><span data-stu-id="be1ad-117">IotHub Object</span></span>

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

### <span data-ttu-id="be1ad-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="be1ad-118">-Name</span></span>
<span data-ttu-id="be1ad-119">Nome do Hub de Iot</span><span class="sxs-lookup"><span data-stu-id="be1ad-119">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="be1ad-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="be1ad-120">-PassThru</span></span>
<span data-ttu-id="be1ad-121">Permite retornar o objeto boolano.</span><span class="sxs-lookup"><span data-stu-id="be1ad-121">Allows to return the boolean object.</span></span> <span data-ttu-id="be1ad-122">Por padrão, esse cmdlet não gera saída.</span><span class="sxs-lookup"><span data-stu-id="be1ad-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="be1ad-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="be1ad-123">-ResourceGroupName</span></span>
<span data-ttu-id="be1ad-124">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="be1ad-124">Name of the Resource Group</span></span>

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

### <span data-ttu-id="be1ad-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="be1ad-125">-ResourceId</span></span>
<span data-ttu-id="be1ad-126">ID de Recurso do IotHub</span><span class="sxs-lookup"><span data-stu-id="be1ad-126">IotHub Resource Id</span></span>

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

### <span data-ttu-id="be1ad-127">-Nomeda Roteada</span><span class="sxs-lookup"><span data-stu-id="be1ad-127">-RouteName</span></span>
<span data-ttu-id="be1ad-128">Nome da Rota</span><span class="sxs-lookup"><span data-stu-id="be1ad-128">Name of the Route</span></span>

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

### <span data-ttu-id="be1ad-129">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="be1ad-129">-Confirm</span></span>
<span data-ttu-id="be1ad-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="be1ad-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="be1ad-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="be1ad-131">-WhatIf</span></span>
<span data-ttu-id="be1ad-132">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="be1ad-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="be1ad-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="be1ad-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="be1ad-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be1ad-134">CommonParameters</span></span>
<span data-ttu-id="be1ad-135">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="be1ad-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be1ad-136">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="be1ad-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be1ad-137">Entradas</span><span class="sxs-lookup"><span data-stu-id="be1ad-137">INPUTS</span></span>

### <span data-ttu-id="be1ad-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="be1ad-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="be1ad-139">System.String</span><span class="sxs-lookup"><span data-stu-id="be1ad-139">System.String</span></span>

## <span data-ttu-id="be1ad-140">Saídas</span><span class="sxs-lookup"><span data-stu-id="be1ad-140">OUTPUTS</span></span>

### <span data-ttu-id="be1ad-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="be1ad-141">System.Boolean</span></span>

## <span data-ttu-id="be1ad-142">Notas</span><span class="sxs-lookup"><span data-stu-id="be1ad-142">NOTES</span></span>

## <span data-ttu-id="be1ad-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="be1ad-143">RELATED LINKS</span></span>
