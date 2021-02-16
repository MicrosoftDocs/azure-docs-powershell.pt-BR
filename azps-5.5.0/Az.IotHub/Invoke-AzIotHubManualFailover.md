---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/invoke-aziothubmanualfailover
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubManualFailover.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubManualFailover.md
ms.openlocfilehash: d32cad2dc435c468ca785da4f81416c7c5330bd8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117612"
---
# <span data-ttu-id="91779-101">Invoke-AzIotHubManualFailover</span><span class="sxs-lookup"><span data-stu-id="91779-101">Invoke-AzIotHubManualFailover</span></span>

## <span data-ttu-id="91779-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="91779-102">SYNOPSIS</span></span>
<span data-ttu-id="91779-103">Invoke failover process for the IoT Hub to the geo-paired disaster recovery region.</span><span class="sxs-lookup"><span data-stu-id="91779-103">Invoke failover process for the IoT Hub to the geo-paired disaster recovery region.</span></span>

## <span data-ttu-id="91779-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="91779-104">SYNTAX</span></span>

### <span data-ttu-id="91779-105">ResourceSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="91779-105">ResourceSet (Default)</span></span>
```
Invoke-AzIotHubManualFailover [-ResourceGroupName] <String> [-Name] <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="91779-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="91779-106">InputObjectSet</span></span>
```
Invoke-AzIotHubManualFailover [-InputObject] <PSIotHub> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="91779-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="91779-107">ResourceIdSet</span></span>
```
Invoke-AzIotHubManualFailover [-ResourceId] <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="91779-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="91779-108">DESCRIPTION</span></span>
<span data-ttu-id="91779-109">Ele disparará o failover do hub de IoT para o local secundário.</span><span class="sxs-lookup"><span data-stu-id="91779-109">It will trigger the failover your IoT hub to the secondary location.</span></span> <span data-ttu-id="91779-110">Essa ação causará perda de tempo e telemetria na sua solução.</span><span class="sxs-lookup"><span data-stu-id="91779-110">This action will cause down time and telemetry loss to your solution.</span></span> <span data-ttu-id="91779-111">Esta é uma operação de longa execução e pode levar alguns minutos para ser terminada.</span><span class="sxs-lookup"><span data-stu-id="91779-111">This is a long running operation and could take several minutes to finish.</span></span> <span data-ttu-id="91779-112">Tenha cuidado ao usá-lo.</span><span class="sxs-lookup"><span data-stu-id="91779-112">Please exercise with caution when using it.</span></span>

## <span data-ttu-id="91779-113">Exemplos</span><span class="sxs-lookup"><span data-stu-id="91779-113">EXAMPLES</span></span>

### <span data-ttu-id="91779-114">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="91779-114">Example 1</span></span>
```powershell
PS C:\> Invoke-AzIotHubManualFailover -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="91779-115">Iniciando o processo de failover do Hub de IoT do "myiothub".</span><span class="sxs-lookup"><span data-stu-id="91779-115">Initiating failover process of "myiothub" IoT Hub.</span></span>

### <span data-ttu-id="91779-116">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="91779-116">Example 2</span></span>
```powershell
PS C:\> Invoke-AzIotHubManualFailover -ResourceGroupName "myresourcegroup" -Name "myiothub" -AsJob
```

<span data-ttu-id="91779-117">Iniciando o processo de failover do Hub IoT do "myiothub" em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="91779-117">Initiating failover process of "myiothub" IoT Hub in the background.</span></span>

## <span data-ttu-id="91779-118">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="91779-118">PARAMETERS</span></span>

### <span data-ttu-id="91779-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="91779-119">-AsJob</span></span>
<span data-ttu-id="91779-120">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="91779-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="91779-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91779-121">-DefaultProfile</span></span>
<span data-ttu-id="91779-122">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="91779-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="91779-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="91779-123">-InputObject</span></span>
<span data-ttu-id="91779-124">Objeto Hub Iot</span><span class="sxs-lookup"><span data-stu-id="91779-124">Iot Hub Object</span></span>

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

### <span data-ttu-id="91779-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="91779-125">-Name</span></span>
<span data-ttu-id="91779-126">Nome do Hub de Iot</span><span class="sxs-lookup"><span data-stu-id="91779-126">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="91779-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="91779-127">-PassThru</span></span>
<span data-ttu-id="91779-128">Permite retornar o objeto boolano.</span><span class="sxs-lookup"><span data-stu-id="91779-128">Allows to return the boolean object.</span></span> <span data-ttu-id="91779-129">Por padrão, esse cmdlet não gera saída.</span><span class="sxs-lookup"><span data-stu-id="91779-129">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="91779-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="91779-130">-ResourceGroupName</span></span>
<span data-ttu-id="91779-131">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="91779-131">Name of the Resource Group</span></span>

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

### <span data-ttu-id="91779-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="91779-132">-ResourceId</span></span>
<span data-ttu-id="91779-133">Id de Recurso do Hub Iot</span><span class="sxs-lookup"><span data-stu-id="91779-133">Iot Hub Resource Id</span></span>

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

### <span data-ttu-id="91779-134">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="91779-134">-Confirm</span></span>
<span data-ttu-id="91779-135">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="91779-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="91779-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="91779-136">-WhatIf</span></span>
<span data-ttu-id="91779-137">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="91779-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="91779-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="91779-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="91779-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91779-139">CommonParameters</span></span>
<span data-ttu-id="91779-140">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="91779-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91779-141">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="91779-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91779-142">Entradas</span><span class="sxs-lookup"><span data-stu-id="91779-142">INPUTS</span></span>

### <span data-ttu-id="91779-143">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="91779-143">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="91779-144">System.String</span><span class="sxs-lookup"><span data-stu-id="91779-144">System.String</span></span>

## <span data-ttu-id="91779-145">Saídas</span><span class="sxs-lookup"><span data-stu-id="91779-145">OUTPUTS</span></span>

### <span data-ttu-id="91779-146">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="91779-146">System.Boolean</span></span>

## <span data-ttu-id="91779-147">Notas</span><span class="sxs-lookup"><span data-stu-id="91779-147">NOTES</span></span>

## <span data-ttu-id="91779-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="91779-148">RELATED LINKS</span></span>
