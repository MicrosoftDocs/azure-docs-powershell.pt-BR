---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Advisor.dll-Help.xml
Module Name: Az.Advisor
online version: https://docs.microsoft.com/powershell/module/az.advisor/set-azadvisorConfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Advisor/Advisor/help/Set-AzAdvisorConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Advisor/Advisor/help/Set-AzAdvisorConfiguration.md
ms.openlocfilehash: 550b9d11cd2f5b0cadb13d76809faa2ac34dc426
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887260"
---
# <span data-ttu-id="77238-101">Set-AzAdvisorConfiguration</span><span class="sxs-lookup"><span data-stu-id="77238-101">Set-AzAdvisorConfiguration</span></span>

## <span data-ttu-id="77238-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="77238-102">SYNOPSIS</span></span>
<span data-ttu-id="77238-103">Atualiza ou cria a Configuração do Azure Advisor.</span><span class="sxs-lookup"><span data-stu-id="77238-103">Updates or creates the Azure Advisor Configuration.</span></span>

## <span data-ttu-id="77238-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="77238-104">SYNTAX</span></span>

### <span data-ttu-id="77238-105">InputObjectRgExcludeParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="77238-105">InputObjectRgExcludeParameterSet (Default)</span></span>
```
Set-AzAdvisorConfiguration [-Exclude] [[-ResourceGroupName] <String>]
 [[-InputObject] <PsAzureAdvisorConfigurationData>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="77238-106">InputObjectLowCpuExcludeParameterSet</span><span class="sxs-lookup"><span data-stu-id="77238-106">InputObjectLowCpuExcludeParameterSet</span></span> 
```
Set-AzAdvisorConfiguration [-Exclude] [-LowCpuThreshold] <Int32>
 [[-InputObject] <PsAzureAdvisorConfigurationData>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="77238-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="77238-107">DESCRIPTION</span></span>
<span data-ttu-id="77238-108">Usado para atualizar a configuração do Azure Advisor.</span><span class="sxs-lookup"><span data-stu-id="77238-108">Used to update the configuration of the Azure Advisor.</span></span> <span data-ttu-id="77238-109">Dois tipos de Configuração estão presentes: configuração de nível de assinatura e configuração de nível resourceGroup.</span><span class="sxs-lookup"><span data-stu-id="77238-109">Two types of Configuration are present: Subscription level configuration and ResourceGroup level configuration.</span></span> 

<span data-ttu-id="77238-110">Configuração de nível de assinatura: só pode haver uma Configuração para esse tipo para uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="77238-110">Subscription level configuration: There can be only one Configuration for this type for a subscription.</span></span> <span data-ttu-id="77238-111">As propriedades LowCpuThreshold e Exclude podem ser atualizadas usando este cmdlet.</span><span class="sxs-lookup"><span data-stu-id="77238-111">LowCpuThreshold and Exclude properties can be updated using this cmdlet.</span></span>
<span data-ttu-id="77238-112">Configuração de nível resourceGroup: só pode haver uma configuração para cada ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="77238-112">ResourceGroup level configuration: There can be only one configuration for each ResourceGroup.</span></span> <span data-ttu-id="77238-113">Somente a propriedade Exclude pode ser atualizada usando este cmdlet.</span><span class="sxs-lookup"><span data-stu-id="77238-113">Only Exclude property can be updated using this cmdlet.</span></span>

## <span data-ttu-id="77238-114">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="77238-114">EXAMPLES</span></span>

###  <span data-ttu-id="77238-115">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="77238-115">Example 1</span></span>
```powershell
PS C:\> Set-AzAdvisorConfiguration -LowCpuThreshold 10
Id         : /subscriptions/{user_subscription}/resourceGroups/resourceGroupName1/providers/Microsoft.Advisor/configurations/{user_subscription}
Name       : {user_subscription}
Properties : additionalProperties : null
             exclude :  False
             lowCpuThreshold : 10

Type       : Microsoft.Advisor/Configurations
```

<span data-ttu-id="77238-116">Atualiza a configuração(lowCpuThreshold) para configuração de nível de assinatura.</span><span class="sxs-lookup"><span data-stu-id="77238-116">Updates the configuration(lowCpuThreshold) for subscription level Configuration.</span></span>

### <span data-ttu-id="77238-117">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="77238-117">Example 2</span></span>
```powershell
PS C:\> Set-AzAdvisorConfiguration -LowCpuThreshold 15 -Exclude 
Id         : /subscriptions/{user_subscription}/resourceGroups/resourceGroupName1/providers/Microsoft.Advisor/configurations/{user_subscription}
Name       : {user_subscription}
Properties : additionalProperties : null
             exclude :  True
             lowCpuThreshold : 15

Type       : Microsoft.Advisor/Configurations
```

<span data-ttu-id="77238-118">Atualiza a configuração(lowCpuThreshold, exclude) para o nível de assinatura Configuração e exclui da geração de recomendações.</span><span class="sxs-lookup"><span data-stu-id="77238-118">Updates the configuration(lowCpuThreshold, exclude) for subscription level Configuration and excludes from the recommendation generation.</span></span>

### <span data-ttu-id="77238-119">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="77238-119">Example 3</span></span>
```powershell
PS C:\> Set-AzAdvisorConfiguration -ResourceGroupName resourceGroupName1 -Exclude

Id         : /subscriptions/{user_subscription}/resourceGroups/resourceGroupName1/providers/Microsoft.Advisor/configurations/{user_subscription}-resourceGroupName1
Name       : {user_subscription}-resourceGroupName1
Properties : additionalProperties : null
             exclude :  True
             lowCpuThreshold : null

Type       : Microsoft.Advisor/Configurations
```

<span data-ttu-id="77238-120">Atualiza a configuração(exclude) para resourceGroupName1 a ser excluído na geração de recomendações.</span><span class="sxs-lookup"><span data-stu-id="77238-120">Updates the configuration(exclude) for resourceGroupName1 to be excluded in the recommendation generation.</span></span>

### <span data-ttu-id="77238-121">Exemplo 4</span><span class="sxs-lookup"><span data-stu-id="77238-121">Example 4</span></span>
```powershell
PS C:\> Get-AzAdvisorConfiguration | Set-AzAdvisorConfiguration -LowCpuThreshold 20
Id         : /subscriptions/{user_subscription}/resourceGroups/resourceGroupName1/providers/Microsoft.Advisor/configurations/{user_subscription}
Name       : {user_subscription}
Properties : additionalProperties : null
             exclude :  False
             lowCpuThreshold : 20

Type       : Microsoft.Advisor/Configurations
```

<span data-ttu-id="77238-122">Atualiza a configuração para a recomendação dada passada do pipeline.</span><span class="sxs-lookup"><span data-stu-id="77238-122">Updates the configuration for the given recommendation passed on from the pipeline.</span></span>

## <span data-ttu-id="77238-123">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="77238-123">PARAMETERS</span></span>

### <span data-ttu-id="77238-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="77238-124">-Confirm</span></span>
<span data-ttu-id="77238-125">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="77238-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77238-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77238-126">-DefaultProfile</span></span>
<span data-ttu-id="77238-127">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="77238-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77238-128">-Exclude</span><span class="sxs-lookup"><span data-stu-id="77238-128">-Exclude</span></span>
<span data-ttu-id="77238-129">Excluir da geração de recomendações.</span><span class="sxs-lookup"><span data-stu-id="77238-129">Exclude from the recommendation generation.</span></span> <span data-ttu-id="77238-130">Se não for especificada, a propriedade exclude será definida como false.</span><span class="sxs-lookup"><span data-stu-id="77238-130">If not specified exclude property will be set to false.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77238-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="77238-131">-InputObject</span></span>
<span data-ttu-id="77238-132">O tipo de objeto powershell PsAzureAdvisorConfigurationData retornado por Get-AzAdvisorConfiguration chamada.</span><span class="sxs-lookup"><span data-stu-id="77238-132">The powershell object type PsAzureAdvisorConfigurationData returned by Get-AzAdvisorConfiguration call.</span></span>

```yaml
Type: PsAzureAdvisorConfigurationData
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="77238-133">-LowCpuThreshold</span><span class="sxs-lookup"><span data-stu-id="77238-133">-LowCpuThreshold</span></span>
<span data-ttu-id="77238-134">Valor para limite baixo da Cpu.</span><span class="sxs-lookup"><span data-stu-id="77238-134">Value for Low Cpu threshold.</span></span>

```yaml
Type: Int32
Parameter Sets: InputObjectLowCpuExcludeParameterSet
Aliases:
Accepted values: 0, 5, 10, 15, 20

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77238-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="77238-135">-ResourceGroupName</span></span>
<span data-ttu-id="77238-136">Nome do Grupo de Recursos para a configuração.</span><span class="sxs-lookup"><span data-stu-id="77238-136">Resource Group name for the configuration.</span></span>

```yaml
Type: String
Parameter Sets: InputObjectRgExcludeParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77238-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="77238-137">-WhatIf</span></span>
<span data-ttu-id="77238-138">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="77238-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="77238-139">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="77238-139">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77238-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77238-140">CommonParameters</span></span>
<span data-ttu-id="77238-141">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="77238-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="77238-142">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="77238-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77238-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="77238-143">INPUTS</span></span>

### <span data-ttu-id="77238-144">Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorConfigurationData</span><span class="sxs-lookup"><span data-stu-id="77238-144">Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorConfigurationData</span></span>

## <span data-ttu-id="77238-145">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="77238-145">OUTPUTS</span></span>

### <span data-ttu-id="77238-146">Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorConfigurationData</span><span class="sxs-lookup"><span data-stu-id="77238-146">Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorConfigurationData</span></span>

## <span data-ttu-id="77238-147">NOTES</span><span class="sxs-lookup"><span data-stu-id="77238-147">NOTES</span></span>

## <span data-ttu-id="77238-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="77238-148">RELATED LINKS</span></span>
