---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/set-aziothubdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubDeployment.md
ms.openlocfilehash: 1fac3ef0db0022bcb837392bf1c0b64e63c40401
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "93954982"
---
# <span data-ttu-id="175d6-101">Set-AzIotHubDeployment</span><span class="sxs-lookup"><span data-stu-id="175d6-101">Set-AzIotHubDeployment</span></span>

## <span data-ttu-id="175d6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="175d6-102">SYNOPSIS</span></span>
<span data-ttu-id="175d6-103">Atualize os campos mutáveis da implantação do IoT Edge.</span><span class="sxs-lookup"><span data-stu-id="175d6-103">Update the mutable fields of IoT Edge deployment.</span></span>

## <span data-ttu-id="175d6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="175d6-104">SYNTAX</span></span>

### <span data-ttu-id="175d6-105">ResourceSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="175d6-105">ResourceSet (Default)</span></span>
```
Set-AzIotHubDeployment [-ResourceGroupName] <String> [-IotHubName] <String> -Name <String> [-Priority <Int32>]
 [-TargetCondition <String>] [-Metric <Hashtable>] [-Label <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="175d6-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="175d6-106">InputObjectSet</span></span>
```
Set-AzIotHubDeployment [-InputObject] <PSIotHub> -Name <String> [-Priority <Int32>] [-TargetCondition <String>]
 [-Metric <Hashtable>] [-Label <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="175d6-107">ResourceSet</span><span class="sxs-lookup"><span data-stu-id="175d6-107">ResourceIdSet</span></span>
```
Set-AzIotHubDeployment [-ResourceId] <String> -Name <String> [-Priority <Int32>] [-TargetCondition <String>]
 [-Metric <Hashtable>] [-Label <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="175d6-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="175d6-108">DESCRIPTION</span></span>
<span data-ttu-id="175d6-109">Atualize as propriedades especificadas de uma implantação de borda IoT.</span><span class="sxs-lookup"><span data-stu-id="175d6-109">Update specified properties of an IoT Edge deployment.</span></span>
<span data-ttu-id="175d6-110">Observação: o conteúdo de configuração é imutável.</span><span class="sxs-lookup"><span data-stu-id="175d6-110">Note: Configuration content is immutable.</span></span> <span data-ttu-id="175d6-111">As propriedades de configuração que podem ser atualizadas são ' rótulos ', ' métricas ', ' prioridade ' e ' targetCondition '.</span><span class="sxs-lookup"><span data-stu-id="175d6-111">Configuration properties that can be updated are 'labels', 'metrics', 'priority' and 'targetCondition'.</span></span>
<span data-ttu-id="175d6-112">Consulte https://docs.microsoft.com/azure/iot-edge/module-deployment-monitoring  para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="175d6-112">See https://docs.microsoft.com/azure/iot-edge/module-deployment-monitoring  for more information.</span></span>

## <span data-ttu-id="175d6-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="175d6-113">EXAMPLES</span></span>

### <span data-ttu-id="175d6-114">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="175d6-114">Example 1</span></span>
```powershell
PS C:\> Set-AzIotHubDeployment -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "deploy1" -Priority 7 -TargetCondition "tags.building=3 and tags.environment='dev'"
```

<span data-ttu-id="175d6-115">Altere a prioridade da implantação de borda IoT e atualize sua condição de destino.</span><span class="sxs-lookup"><span data-stu-id="175d6-115">Alter the priority of IoT Edge deployment and update its target condition.</span></span>

## <span data-ttu-id="175d6-116">OS</span><span class="sxs-lookup"><span data-stu-id="175d6-116">PARAMETERS</span></span>

### <span data-ttu-id="175d6-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="175d6-117">-DefaultProfile</span></span>
<span data-ttu-id="175d6-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="175d6-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="175d6-119">-Force</span><span class="sxs-lookup"><span data-stu-id="175d6-119">-Force</span></span>
<span data-ttu-id="175d6-120">Permite que o objeto de implantação seja substituído mesmo se ele tiver sido atualizado desde a última vez que foi recuperado.</span><span class="sxs-lookup"><span data-stu-id="175d6-120">Allows deployment object to be replaced even if it was updated since it was retrieved last time.</span></span>

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

### <span data-ttu-id="175d6-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="175d6-121">-InputObject</span></span>
<span data-ttu-id="175d6-122">Objeto IotHub</span><span class="sxs-lookup"><span data-stu-id="175d6-122">IotHub object</span></span>

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

### <span data-ttu-id="175d6-123">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="175d6-123">-IotHubName</span></span>
<span data-ttu-id="175d6-124">Nome do Hub IOT</span><span class="sxs-lookup"><span data-stu-id="175d6-124">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="175d6-125">-Rótulo</span><span class="sxs-lookup"><span data-stu-id="175d6-125">-Label</span></span>
<span data-ttu-id="175d6-126">Mapa de rótulos a serem aplicados à implantação de destino.</span><span class="sxs-lookup"><span data-stu-id="175d6-126">Map of labels to be applied to target deployment.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="175d6-127">-Métrica</span><span class="sxs-lookup"><span data-stu-id="175d6-127">-Metric</span></span>
<span data-ttu-id="175d6-128">Coleção queries para definição de métricas de implantação de borda IoT.</span><span class="sxs-lookup"><span data-stu-id="175d6-128">Queries collection for IoT Edge deployment metrics definition.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="175d6-129">-Nome</span><span class="sxs-lookup"><span data-stu-id="175d6-129">-Name</span></span>
<span data-ttu-id="175d6-130">Identificador para a implantação.</span><span class="sxs-lookup"><span data-stu-id="175d6-130">Identifier for the deployment.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="175d6-131">-Priority</span><span class="sxs-lookup"><span data-stu-id="175d6-131">-Priority</span></span>
<span data-ttu-id="175d6-132">Peso da implantação em caso de regras concorrentes (WINS mais alto).</span><span class="sxs-lookup"><span data-stu-id="175d6-132">Weight of deployment in case of competing rules (highest wins).</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="175d6-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="175d6-133">-ResourceGroupName</span></span>
<span data-ttu-id="175d6-134">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="175d6-134">Name of the Resource Group</span></span>

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

### <span data-ttu-id="175d6-135">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="175d6-135">-ResourceId</span></span>
<span data-ttu-id="175d6-136">ID do recurso IotHub</span><span class="sxs-lookup"><span data-stu-id="175d6-136">IotHub Resource Id</span></span>

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

### <span data-ttu-id="175d6-137">-TargetCondition</span><span class="sxs-lookup"><span data-stu-id="175d6-137">-TargetCondition</span></span>
<span data-ttu-id="175d6-138">A condição de destino à qual a implantação de borda se aplica.</span><span class="sxs-lookup"><span data-stu-id="175d6-138">Target condition in which an Edge deployment applies to.</span></span>

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

### <span data-ttu-id="175d6-139">-Confirme</span><span class="sxs-lookup"><span data-stu-id="175d6-139">-Confirm</span></span>
<span data-ttu-id="175d6-140">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="175d6-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="175d6-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="175d6-141">-WhatIf</span></span>
<span data-ttu-id="175d6-142">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="175d6-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="175d6-143">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="175d6-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="175d6-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="175d6-144">CommonParameters</span></span>
<span data-ttu-id="175d6-145">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="175d6-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="175d6-146">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="175d6-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="175d6-147">SENSORES</span><span class="sxs-lookup"><span data-stu-id="175d6-147">INPUTS</span></span>

### <span data-ttu-id="175d6-148">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="175d6-148">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="175d6-149">System. String</span><span class="sxs-lookup"><span data-stu-id="175d6-149">System.String</span></span>

## <span data-ttu-id="175d6-150">EXIBE</span><span class="sxs-lookup"><span data-stu-id="175d6-150">OUTPUTS</span></span>

### <span data-ttu-id="175d6-151">Microsoft.Azure.Commands.Management.IotHub.Models.PSDEployment</span><span class="sxs-lookup"><span data-stu-id="175d6-151">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeployment</span></span>

## <span data-ttu-id="175d6-152">INFORMA</span><span class="sxs-lookup"><span data-stu-id="175d6-152">NOTES</span></span>

## <span data-ttu-id="175d6-153">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="175d6-153">RELATED LINKS</span></span>
