---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/invoke-aziothubmanualfailover
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubManualFailover.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubManualFailover.md
ms.openlocfilehash: f9372a246e16e719db60f52922a8a416f3de10c4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887737"
---
# <span data-ttu-id="ef50d-101">Invoke-AzIotHubManualFailover</span><span class="sxs-lookup"><span data-stu-id="ef50d-101">Invoke-AzIotHubManualFailover</span></span>

## <span data-ttu-id="ef50d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ef50d-102">SYNOPSIS</span></span>
<span data-ttu-id="ef50d-103">Invocar o processo de failover para o Hub de IoT para a região de recuperação de desastres geo emparelhada.</span><span class="sxs-lookup"><span data-stu-id="ef50d-103">Invoke failover process for the IoT Hub to the geo-paired disaster recovery region.</span></span>

## <span data-ttu-id="ef50d-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="ef50d-104">SYNTAX</span></span>

### <span data-ttu-id="ef50d-105">ResourceSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="ef50d-105">ResourceSet (Default)</span></span>
```
Invoke-AzIotHubManualFailover [-ResourceGroupName] <String> [-Name] <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ef50d-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="ef50d-106">InputObjectSet</span></span>
```
Invoke-AzIotHubManualFailover [-InputObject] <PSIotHub> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ef50d-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="ef50d-107">ResourceIdSet</span></span>
```
Invoke-AzIotHubManualFailover [-ResourceId] <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ef50d-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="ef50d-108">DESCRIPTION</span></span>
<span data-ttu-id="ef50d-109">Ele disparará o failover do hub de IoT para o local secundário.</span><span class="sxs-lookup"><span data-stu-id="ef50d-109">It will trigger the failover your IoT hub to the secondary location.</span></span> <span data-ttu-id="ef50d-110">Essa ação causará perda de tempo e telemetria para sua solução.</span><span class="sxs-lookup"><span data-stu-id="ef50d-110">This action will cause down time and telemetry loss to your solution.</span></span> <span data-ttu-id="ef50d-111">Esta é uma operação de longa duração e pode levar vários minutos para ser final.</span><span class="sxs-lookup"><span data-stu-id="ef50d-111">This is a long running operation and could take several minutes to finish.</span></span> <span data-ttu-id="ef50d-112">Tenha cuidado ao usá-lo.</span><span class="sxs-lookup"><span data-stu-id="ef50d-112">Please exercise with caution when using it.</span></span>

## <span data-ttu-id="ef50d-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ef50d-113">EXAMPLES</span></span>

### <span data-ttu-id="ef50d-114">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="ef50d-114">Example 1</span></span>
```powershell
PS C:\> Invoke-AzIotHubManualFailover -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="ef50d-115">Iniciando o processo de failover do Hub de IoT "myiothub".</span><span class="sxs-lookup"><span data-stu-id="ef50d-115">Initiating failover process of "myiothub" IoT Hub.</span></span>

### <span data-ttu-id="ef50d-116">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="ef50d-116">Example 2</span></span>
```powershell
PS C:\> Invoke-AzIotHubManualFailover -ResourceGroupName "myresourcegroup" -Name "myiothub" -AsJob
```

<span data-ttu-id="ef50d-117">Iniciando o processo de failover do Hub de IoT "myiothub" em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="ef50d-117">Initiating failover process of "myiothub" IoT Hub in the background.</span></span>

## <span data-ttu-id="ef50d-118">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="ef50d-118">PARAMETERS</span></span>

### <span data-ttu-id="ef50d-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ef50d-119">-AsJob</span></span>
<span data-ttu-id="ef50d-120">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="ef50d-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ef50d-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef50d-121">-DefaultProfile</span></span>
<span data-ttu-id="ef50d-122">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ef50d-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ef50d-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ef50d-123">-InputObject</span></span>
<span data-ttu-id="ef50d-124">Objeto Iot Hub</span><span class="sxs-lookup"><span data-stu-id="ef50d-124">Iot Hub Object</span></span>

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

### <span data-ttu-id="ef50d-125">-Name</span><span class="sxs-lookup"><span data-stu-id="ef50d-125">-Name</span></span>
<span data-ttu-id="ef50d-126">Nome do Hub de Iot</span><span class="sxs-lookup"><span data-stu-id="ef50d-126">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="ef50d-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ef50d-127">-PassThru</span></span>
<span data-ttu-id="ef50d-128">Permite retornar o objeto booleano.</span><span class="sxs-lookup"><span data-stu-id="ef50d-128">Allows to return the boolean object.</span></span> <span data-ttu-id="ef50d-129">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="ef50d-129">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="ef50d-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ef50d-130">-ResourceGroupName</span></span>
<span data-ttu-id="ef50d-131">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="ef50d-131">Name of the Resource Group</span></span>

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

### <span data-ttu-id="ef50d-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ef50d-132">-ResourceId</span></span>
<span data-ttu-id="ef50d-133">Id do Recurso de Hub de Iot</span><span class="sxs-lookup"><span data-stu-id="ef50d-133">Iot Hub Resource Id</span></span>

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

### <span data-ttu-id="ef50d-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ef50d-134">-Confirm</span></span>
<span data-ttu-id="ef50d-135">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ef50d-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ef50d-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ef50d-136">-WhatIf</span></span>
<span data-ttu-id="ef50d-137">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="ef50d-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ef50d-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ef50d-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ef50d-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef50d-139">CommonParameters</span></span>
<span data-ttu-id="ef50d-140">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ef50d-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef50d-141">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ef50d-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef50d-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ef50d-142">INPUTS</span></span>

### <span data-ttu-id="ef50d-143">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="ef50d-143">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="ef50d-144">System.String</span><span class="sxs-lookup"><span data-stu-id="ef50d-144">System.String</span></span>

## <span data-ttu-id="ef50d-145">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="ef50d-145">OUTPUTS</span></span>

### <span data-ttu-id="ef50d-146">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="ef50d-146">System.Boolean</span></span>

## <span data-ttu-id="ef50d-147">NOTES</span><span class="sxs-lookup"><span data-stu-id="ef50d-147">NOTES</span></span>

## <span data-ttu-id="ef50d-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ef50d-148">RELATED LINKS</span></span>
