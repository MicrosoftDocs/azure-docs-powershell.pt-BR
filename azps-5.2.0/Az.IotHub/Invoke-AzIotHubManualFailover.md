---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/invoke-aziothubmanualfailover
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubManualFailover.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubManualFailover.md
ms.openlocfilehash: d32cad2dc435c468ca785da4f81416c7c5330bd8
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98261202"
---
# <span data-ttu-id="a3332-101">Invoke-AzIotHubManualFailover</span><span class="sxs-lookup"><span data-stu-id="a3332-101">Invoke-AzIotHubManualFailover</span></span>

## <span data-ttu-id="a3332-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a3332-102">SYNOPSIS</span></span>
<span data-ttu-id="a3332-103">Invocar o processo de failover para o Hub IoT para a região de recuperação de desastres em par geográfico.</span><span class="sxs-lookup"><span data-stu-id="a3332-103">Invoke failover process for the IoT Hub to the geo-paired disaster recovery region.</span></span>

## <span data-ttu-id="a3332-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a3332-104">SYNTAX</span></span>

### <span data-ttu-id="a3332-105">ResourceSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="a3332-105">ResourceSet (Default)</span></span>
```
Invoke-AzIotHubManualFailover [-ResourceGroupName] <String> [-Name] <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a3332-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="a3332-106">InputObjectSet</span></span>
```
Invoke-AzIotHubManualFailover [-InputObject] <PSIotHub> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a3332-107">ResourceSet</span><span class="sxs-lookup"><span data-stu-id="a3332-107">ResourceIdSet</span></span>
```
Invoke-AzIotHubManualFailover [-ResourceId] <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a3332-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a3332-108">DESCRIPTION</span></span>
<span data-ttu-id="a3332-109">Ele disparará o failover do seu hub IoT para o local secundário.</span><span class="sxs-lookup"><span data-stu-id="a3332-109">It will trigger the failover your IoT hub to the secondary location.</span></span> <span data-ttu-id="a3332-110">Esta ação causará perda de tempo e telemetria para a sua solução.</span><span class="sxs-lookup"><span data-stu-id="a3332-110">This action will cause down time and telemetry loss to your solution.</span></span> <span data-ttu-id="a3332-111">Esta é uma operação de longa duração que pode demorar vários minutos para ser concluída.</span><span class="sxs-lookup"><span data-stu-id="a3332-111">This is a long running operation and could take several minutes to finish.</span></span> <span data-ttu-id="a3332-112">Por favor, tome cuidado ao usá-lo.</span><span class="sxs-lookup"><span data-stu-id="a3332-112">Please exercise with caution when using it.</span></span>

## <span data-ttu-id="a3332-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a3332-113">EXAMPLES</span></span>

### <span data-ttu-id="a3332-114">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="a3332-114">Example 1</span></span>
```powershell
PS C:\> Invoke-AzIotHubManualFailover -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="a3332-115">Iniciando o processo de failover do Hub IoT "myiothub".</span><span class="sxs-lookup"><span data-stu-id="a3332-115">Initiating failover process of "myiothub" IoT Hub.</span></span>

### <span data-ttu-id="a3332-116">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="a3332-116">Example 2</span></span>
```powershell
PS C:\> Invoke-AzIotHubManualFailover -ResourceGroupName "myresourcegroup" -Name "myiothub" -AsJob
```

<span data-ttu-id="a3332-117">Iniciando o processo de failover do Hub IoT "myiothub" em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="a3332-117">Initiating failover process of "myiothub" IoT Hub in the background.</span></span>

## <span data-ttu-id="a3332-118">OS</span><span class="sxs-lookup"><span data-stu-id="a3332-118">PARAMETERS</span></span>

### <span data-ttu-id="a3332-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a3332-119">-AsJob</span></span>
<span data-ttu-id="a3332-120">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="a3332-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a3332-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3332-121">-DefaultProfile</span></span>
<span data-ttu-id="a3332-122">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a3332-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a3332-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a3332-123">-InputObject</span></span>
<span data-ttu-id="a3332-124">Objeto Hub IOT</span><span class="sxs-lookup"><span data-stu-id="a3332-124">Iot Hub Object</span></span>

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

### <span data-ttu-id="a3332-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="a3332-125">-Name</span></span>
<span data-ttu-id="a3332-126">Nome do Hub IOT</span><span class="sxs-lookup"><span data-stu-id="a3332-126">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="a3332-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a3332-127">-PassThru</span></span>
<span data-ttu-id="a3332-128">Permite retornar o objeto booliano.</span><span class="sxs-lookup"><span data-stu-id="a3332-128">Allows to return the boolean object.</span></span> <span data-ttu-id="a3332-129">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="a3332-129">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="a3332-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a3332-130">-ResourceGroupName</span></span>
<span data-ttu-id="a3332-131">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="a3332-131">Name of the Resource Group</span></span>

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

### <span data-ttu-id="a3332-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a3332-132">-ResourceId</span></span>
<span data-ttu-id="a3332-133">ID do recurso do Hub IOT</span><span class="sxs-lookup"><span data-stu-id="a3332-133">Iot Hub Resource Id</span></span>

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

### <span data-ttu-id="a3332-134">-Confirme</span><span class="sxs-lookup"><span data-stu-id="a3332-134">-Confirm</span></span>
<span data-ttu-id="a3332-135">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a3332-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a3332-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a3332-136">-WhatIf</span></span>
<span data-ttu-id="a3332-137">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="a3332-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a3332-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a3332-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a3332-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3332-139">CommonParameters</span></span>
<span data-ttu-id="a3332-140">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a3332-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3332-141">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a3332-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3332-142">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a3332-142">INPUTS</span></span>

### <span data-ttu-id="a3332-143">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="a3332-143">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="a3332-144">System. String</span><span class="sxs-lookup"><span data-stu-id="a3332-144">System.String</span></span>

## <span data-ttu-id="a3332-145">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a3332-145">OUTPUTS</span></span>

### <span data-ttu-id="a3332-146">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a3332-146">System.Boolean</span></span>

## <span data-ttu-id="a3332-147">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a3332-147">NOTES</span></span>

## <span data-ttu-id="a3332-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a3332-148">RELATED LINKS</span></span>
