---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Advisor.dll-Help.xml
Module Name: Az.Advisor
online version: https://docs.microsoft.com/en-us/powershell/module/az.advisor/set-azadvisorConfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Advisor/Advisor/help/Set-AzAdvisorConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Advisor/Advisor/help/Set-AzAdvisorConfiguration.md
ms.openlocfilehash: bfd1677fa46a749b73206b02bb6585c4a529637f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114320"
---
# <span data-ttu-id="1f289-101">Set-AzAdvisorConfiguration</span><span class="sxs-lookup"><span data-stu-id="1f289-101">Set-AzAdvisorConfiguration</span></span>

## <span data-ttu-id="1f289-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1f289-102">SYNOPSIS</span></span>
<span data-ttu-id="1f289-103">Atualiza ou cria a Configuração do Azure Advisor.</span><span class="sxs-lookup"><span data-stu-id="1f289-103">Updates or creates the Azure Advisor Configuration.</span></span>

## <span data-ttu-id="1f289-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1f289-104">SYNTAX</span></span>

### <span data-ttu-id="1f289-105">InputObjectRgExcludeParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="1f289-105">InputObjectRgExcludeParameterSet (Default)</span></span>
```
Set-AzAdvisorConfiguration [-Exclude] [[-ResourceGroupName] <String>]
 [[-InputObject] <PsAzureAdvisorConfigurationData>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1f289-106">InputObjectLowCpuExcludeParameterSet</span><span class="sxs-lookup"><span data-stu-id="1f289-106">InputObjectLowCpuExcludeParameterSet</span></span> 
```
Set-AzAdvisorConfiguration [-Exclude] [-LowCpuThreshold] <Int32>
 [[-InputObject] <PsAzureAdvisorConfigurationData>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1f289-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="1f289-107">DESCRIPTION</span></span>
<span data-ttu-id="1f289-108">Usado para atualizar a configuração do Azure Advisor.</span><span class="sxs-lookup"><span data-stu-id="1f289-108">Used to update the configuration of the Azure Advisor.</span></span> <span data-ttu-id="1f289-109">Dois tipos de Configuração estão presentes: configuração de nível de assinatura e configuração de nível de Grupo de Recursos.</span><span class="sxs-lookup"><span data-stu-id="1f289-109">Two types of Configuration are present: Subscription level configuration and ResourceGroup level configuration.</span></span> 

<span data-ttu-id="1f289-110">Configuração de nível de assinatura: pode haver apenas uma configuração para esse tipo de assinatura.</span><span class="sxs-lookup"><span data-stu-id="1f289-110">Subscription level configuration: There can be only one Configuration for this type for a subscription.</span></span> <span data-ttu-id="1f289-111">As propriedades LowCpuThreshold e Exclude podem ser atualizadas usando este cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1f289-111">LowCpuThreshold and Exclude properties can be updated using this cmdlet.</span></span>
<span data-ttu-id="1f289-112">Configuração de nível de Grupo de Recursos: pode haver apenas uma configuração para cada Grupo de Recursos.</span><span class="sxs-lookup"><span data-stu-id="1f289-112">ResourceGroup level configuration: There can be only one configuration for each ResourceGroup.</span></span> <span data-ttu-id="1f289-113">Somente a propriedade Exclude pode ser atualizada usando este cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1f289-113">Only Exclude property can be updated using this cmdlet.</span></span>

## <span data-ttu-id="1f289-114">Exemplos</span><span class="sxs-lookup"><span data-stu-id="1f289-114">EXAMPLES</span></span>

###  <span data-ttu-id="1f289-115">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="1f289-115">Example 1</span></span>
```powershell
PS C:\> Set-AzAdvisorConfiguration -LowCpuThreshold 10
Id         : /subscriptions/{user_subscription}/resourceGroups/resourceGroupName1/providers/Microsoft.Advisor/configurations/{user_subscription}
Name       : {user_subscription}
Properties : additionalProperties : null
             exclude :  False
             lowCpuThreshold : 10

Type       : Microsoft.Advisor/Configurations
```

<span data-ttu-id="1f289-116">Atualiza a configuração(lowCpuThreshold) para configuração de nível de assinatura.</span><span class="sxs-lookup"><span data-stu-id="1f289-116">Updates the configuration(lowCpuThreshold) for subscription level Configuration.</span></span>

### <span data-ttu-id="1f289-117">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="1f289-117">Example 2</span></span>
```powershell
PS C:\> Set-AzAdvisorConfiguration -LowCpuThreshold 15 -Exclude 
Id         : /subscriptions/{user_subscription}/resourceGroups/resourceGroupName1/providers/Microsoft.Advisor/configurations/{user_subscription}
Name       : {user_subscription}
Properties : additionalProperties : null
             exclude :  True
             lowCpuThreshold : 15

Type       : Microsoft.Advisor/Configurations
```

<span data-ttu-id="1f289-118">Atualiza a configuração(lowCpuThreshold, exclude) para configuração de nível de assinatura e exclui da geração de recomendações.</span><span class="sxs-lookup"><span data-stu-id="1f289-118">Updates the configuration(lowCpuThreshold, exclude) for subscription level Configuration and excludes from the recommendation generation.</span></span>

### <span data-ttu-id="1f289-119">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="1f289-119">Example 3</span></span>
```powershell
PS C:\> Set-AzAdvisorConfiguration -ResourceGroupName resourceGroupName1 -Exclude

Id         : /subscriptions/{user_subscription}/resourceGroups/resourceGroupName1/providers/Microsoft.Advisor/configurations/{user_subscription}-resourceGroupName1
Name       : {user_subscription}-resourceGroupName1
Properties : additionalProperties : null
             exclude :  True
             lowCpuThreshold : null

Type       : Microsoft.Advisor/Configurations
```

<span data-ttu-id="1f289-120">Atualiza a configuração(exclusão) do resourceGroupName1 a ser excluído na geração de recomendações.</span><span class="sxs-lookup"><span data-stu-id="1f289-120">Updates the configuration(exclude) for resourceGroupName1 to be excluded in the recommendation generation.</span></span>

### <span data-ttu-id="1f289-121">Exemplo 4</span><span class="sxs-lookup"><span data-stu-id="1f289-121">Example 4</span></span>
```powershell
PS C:\> Get-AzAdvisorConfiguration | Set-AzAdvisorConfiguration -LowCpuThreshold 20
Id         : /subscriptions/{user_subscription}/resourceGroups/resourceGroupName1/providers/Microsoft.Advisor/configurations/{user_subscription}
Name       : {user_subscription}
Properties : additionalProperties : null
             exclude :  False
             lowCpuThreshold : 20

Type       : Microsoft.Advisor/Configurations
```

<span data-ttu-id="1f289-122">Atualiza a configuração para a determinada recomendação passada a partir do pipeline.</span><span class="sxs-lookup"><span data-stu-id="1f289-122">Updates the configuration for the given recommendation passed on from the pipeline.</span></span>

## <span data-ttu-id="1f289-123">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1f289-123">PARAMETERS</span></span>

### <span data-ttu-id="1f289-124">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="1f289-124">-Confirm</span></span>
<span data-ttu-id="1f289-125">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1f289-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1f289-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f289-126">-DefaultProfile</span></span>
<span data-ttu-id="1f289-127">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1f289-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1f289-128">-Excluir</span><span class="sxs-lookup"><span data-stu-id="1f289-128">-Exclude</span></span>
<span data-ttu-id="1f289-129">Exclua da geração de recomendações.</span><span class="sxs-lookup"><span data-stu-id="1f289-129">Exclude from the recommendation generation.</span></span> <span data-ttu-id="1f289-130">Se não especificado, a propriedade de exclusão será definida como falsa.</span><span class="sxs-lookup"><span data-stu-id="1f289-130">If not specified exclude property will be set to false.</span></span>

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

### <span data-ttu-id="1f289-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1f289-131">-InputObject</span></span>
<span data-ttu-id="1f289-132">O tipo de objeto do PowerShell PsAzureAdvisorConfigurationData retornado por Get-AzAdvisorConfiguration chamada.</span><span class="sxs-lookup"><span data-stu-id="1f289-132">The powershell object type PsAzureAdvisorConfigurationData returned by Get-AzAdvisorConfiguration call.</span></span>

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

### <span data-ttu-id="1f289-133">-LowCpuThreshold</span><span class="sxs-lookup"><span data-stu-id="1f289-133">-LowCpuThreshold</span></span>
<span data-ttu-id="1f289-134">Valor para limite baixo da Cpu.</span><span class="sxs-lookup"><span data-stu-id="1f289-134">Value for Low Cpu threshold.</span></span>

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

### <span data-ttu-id="1f289-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1f289-135">-ResourceGroupName</span></span>
<span data-ttu-id="1f289-136">Nome do Grupo de Recursos para a configuração.</span><span class="sxs-lookup"><span data-stu-id="1f289-136">Resource Group name for the configuration.</span></span>

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

### <span data-ttu-id="1f289-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1f289-137">-WhatIf</span></span>
<span data-ttu-id="1f289-138">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="1f289-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1f289-139">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="1f289-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1f289-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f289-140">CommonParameters</span></span>
<span data-ttu-id="1f289-141">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1f289-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="1f289-142">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1f289-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f289-143">Entradas</span><span class="sxs-lookup"><span data-stu-id="1f289-143">INPUTS</span></span>

### <span data-ttu-id="1f289-144">Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorConfigurationData</span><span class="sxs-lookup"><span data-stu-id="1f289-144">Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorConfigurationData</span></span>

## <span data-ttu-id="1f289-145">Saídas</span><span class="sxs-lookup"><span data-stu-id="1f289-145">OUTPUTS</span></span>

### <span data-ttu-id="1f289-146">Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorConfigurationData</span><span class="sxs-lookup"><span data-stu-id="1f289-146">Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorConfigurationData</span></span>

## <span data-ttu-id="1f289-147">Notas</span><span class="sxs-lookup"><span data-stu-id="1f289-147">NOTES</span></span>

## <span data-ttu-id="1f289-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1f289-148">RELATED LINKS</span></span>
