---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Advisor.dll-Help.xml
Module Name: Az.Advisor
online version: https://docs.microsoft.com/en-us/powershell/module/az.advisor/set-azadvisorConfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Advisor/Advisor/help/Set-AzAdvisorConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Advisor/Advisor/help/Set-AzAdvisorConfiguration.md
ms.openlocfilehash: 4c3a3fd8f80bf1f8a18f65a8dc5c9d0bf26b6d9b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93595757"
---
# <span data-ttu-id="81274-101">Set-AzAdvisorConfiguration</span><span class="sxs-lookup"><span data-stu-id="81274-101">Set-AzAdvisorConfiguration</span></span>

## <span data-ttu-id="81274-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="81274-102">SYNOPSIS</span></span>
<span data-ttu-id="81274-103">Atualiza ou cria a configuração do Azure Advisor.</span><span class="sxs-lookup"><span data-stu-id="81274-103">Updates or creates the Azure Advisor Configuration.</span></span>

## <span data-ttu-id="81274-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="81274-104">SYNTAX</span></span>

### <span data-ttu-id="81274-105">InputObjectRgExcludeParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="81274-105">InputObjectRgExcludeParameterSet (Default)</span></span>
```
Set-AzAdvisorConfiguration [-Exclude] [[-ResourceGroupName] <String>]
 [[-InputObject] <PsAzureAdvisorConfigurationData>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="81274-106">InputObjectLowCpuExcludeParameterSet</span><span class="sxs-lookup"><span data-stu-id="81274-106">InputObjectLowCpuExcludeParameterSet</span></span> 
```
Set-AzAdvisorConfiguration [-Exclude] [-LowCpuThreshold] <Int32>
 [[-InputObject] <PsAzureAdvisorConfigurationData>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="81274-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="81274-107">DESCRIPTION</span></span>
<span data-ttu-id="81274-108">Usado para atualizar a configuração do Azure Advisor.</span><span class="sxs-lookup"><span data-stu-id="81274-108">Used to update the configuration of the Azure Advisor.</span></span> <span data-ttu-id="81274-109">Há dois tipos de configuração: configuração do nível da assinatura e configuração do nível do nível da Resource.</span><span class="sxs-lookup"><span data-stu-id="81274-109">Two types of Configuration are present: Subscription level configuration and ResourceGroup level configuration.</span></span> 

<span data-ttu-id="81274-110">Configuração de nível de assinatura: pode haver apenas uma configuração para esse tipo de assinatura.</span><span class="sxs-lookup"><span data-stu-id="81274-110">Subscription level configuration: There can be only one Configuration for this type for a subscription.</span></span> <span data-ttu-id="81274-111">As propriedades LowCpuThreshold e Exclude podem ser atualizadas usando este cmdlet.</span><span class="sxs-lookup"><span data-stu-id="81274-111">LowCpuThreshold and Exclude properties can be updated using this cmdlet.</span></span>
<span data-ttu-id="81274-112">Configuração do nível de um nível de subcódigo: pode haver apenas uma configuração para cada um dos seus Resources.</span><span class="sxs-lookup"><span data-stu-id="81274-112">ResourceGroup level configuration: There can be only one configuration for each ResourceGroup.</span></span> <span data-ttu-id="81274-113">Só é possível atualizar a propriedade Exclude usando este cmdlet.</span><span class="sxs-lookup"><span data-stu-id="81274-113">Only Exclude property can be updated using this cmdlet.</span></span>

## <span data-ttu-id="81274-114">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="81274-114">EXAMPLES</span></span>

###  <span data-ttu-id="81274-115">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="81274-115">Example 1</span></span>
```powershell
PS C:\> Set-AzAdvisorConfiguration -LowCpuThreshold 10
Id         : /subscriptions/{user_subscription}/resourceGroups/resourceGroupName1/providers/Microsoft.Advisor/configurations/{user_subscription}
Name       : {user_subscription}
Properties : additionalProperties : null
             exclude :  False
             lowCpuThreshold : 10

Type       : Microsoft.Advisor/Configurations
```

<span data-ttu-id="81274-116">Atualiza a configuração (lowCpuThreshold) para a configuração de nível de assinatura.</span><span class="sxs-lookup"><span data-stu-id="81274-116">Updates the configuration(lowCpuThreshold) for subscription level Configuration.</span></span>

### <span data-ttu-id="81274-117">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="81274-117">Example 2</span></span>
```powershell
PS C:\> Set-AzAdvisorConfiguration -LowCpuThreshold 15 -Exclude 
Id         : /subscriptions/{user_subscription}/resourceGroups/resourceGroupName1/providers/Microsoft.Advisor/configurations/{user_subscription}
Name       : {user_subscription}
Properties : additionalProperties : null
             exclude :  True
             lowCpuThreshold : 15

Type       : Microsoft.Advisor/Configurations
```

<span data-ttu-id="81274-118">Atualiza a configuração (lowCpuThreshold, Exclude) para a configuração de nível de assinatura e exclui da geração de recomendação.</span><span class="sxs-lookup"><span data-stu-id="81274-118">Updates the configuration(lowCpuThreshold, exclude) for subscription level Configuration and excludes from the recommendation generation.</span></span>

### <span data-ttu-id="81274-119">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="81274-119">Example 3</span></span>
```powershell
PS C:\> Set-AzAdvisorConfiguration -ResourceGroupName resourceGroupName1 -Exclude

Id         : /subscriptions/{user_subscription}/resourceGroups/resourceGroupName1/providers/Microsoft.Advisor/configurations/{user_subscription}-resourceGroupName1
Name       : {user_subscription}-resourceGroupName1
Properties : additionalProperties : null
             exclude :  True
             lowCpuThreshold : null

Type       : Microsoft.Advisor/Configurations
```

<span data-ttu-id="81274-120">Atualiza a configuração (exclusão) de resourceGroupName1 para ser excluída na geração de recomendação.</span><span class="sxs-lookup"><span data-stu-id="81274-120">Updates the configuration(exclude) for resourceGroupName1 to be excluded in the recommendation generation.</span></span>

### <span data-ttu-id="81274-121">Exemplo 4</span><span class="sxs-lookup"><span data-stu-id="81274-121">Example 4</span></span>
```powershell
PS C:\> Get-AzAdvisorConfiguration | Set-AzAdvisorConfiguration -LowCpuThreshold 20
Id         : /subscriptions/{user_subscription}/resourceGroups/resourceGroupName1/providers/Microsoft.Advisor/configurations/{user_subscription}
Name       : {user_subscription}
Properties : additionalProperties : null
             exclude :  False
             lowCpuThreshold : 20

Type       : Microsoft.Advisor/Configurations
```

<span data-ttu-id="81274-122">Atualiza a configuração para a recomendação fornecida passada do pipeline.</span><span class="sxs-lookup"><span data-stu-id="81274-122">Updates the configuration for the given recommendation passed on from the pipeline.</span></span>

## <span data-ttu-id="81274-123">OS</span><span class="sxs-lookup"><span data-stu-id="81274-123">PARAMETERS</span></span>

### <span data-ttu-id="81274-124">-Confirme</span><span class="sxs-lookup"><span data-stu-id="81274-124">-Confirm</span></span>
<span data-ttu-id="81274-125">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="81274-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="81274-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81274-126">-DefaultProfile</span></span>
<span data-ttu-id="81274-127">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="81274-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="81274-128">-Excluir</span><span class="sxs-lookup"><span data-stu-id="81274-128">-Exclude</span></span>
<span data-ttu-id="81274-129">Excluir da geração de recomendação.</span><span class="sxs-lookup"><span data-stu-id="81274-129">Exclude from the recommendation generation.</span></span> <span data-ttu-id="81274-130">Se não especificado, a propriedade Exclude será definida como false.</span><span class="sxs-lookup"><span data-stu-id="81274-130">If not specified exclude property will be set to false.</span></span>

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

### <span data-ttu-id="81274-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="81274-131">-InputObject</span></span>
<span data-ttu-id="81274-132">O tipo de objeto do PowerShell PsAzureAdvisorConfigurationData retornado por Get-AzAdvisorConfiguration chamada.</span><span class="sxs-lookup"><span data-stu-id="81274-132">The powershell object type PsAzureAdvisorConfigurationData returned by Get-AzAdvisorConfiguration call.</span></span>

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

### <span data-ttu-id="81274-133">-LowCpuThreshold</span><span class="sxs-lookup"><span data-stu-id="81274-133">-LowCpuThreshold</span></span>
<span data-ttu-id="81274-134">Valor para limite de CPU baixa.</span><span class="sxs-lookup"><span data-stu-id="81274-134">Value for Low Cpu threshold.</span></span>

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

### <span data-ttu-id="81274-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="81274-135">-ResourceGroupName</span></span>
<span data-ttu-id="81274-136">Nome do grupo de recursos para a configuração.</span><span class="sxs-lookup"><span data-stu-id="81274-136">Resource Group name for the configuration.</span></span>

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

### <span data-ttu-id="81274-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="81274-137">-WhatIf</span></span>
<span data-ttu-id="81274-138">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="81274-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="81274-139">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="81274-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="81274-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81274-140">CommonParameters</span></span>
<span data-ttu-id="81274-141">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="81274-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="81274-142">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="81274-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81274-143">SENSORES</span><span class="sxs-lookup"><span data-stu-id="81274-143">INPUTS</span></span>

### <span data-ttu-id="81274-144">Microsoft. Azure. Commands. Advisor. cmdlets. Models. PsAzureAdvisorConfigurationData</span><span class="sxs-lookup"><span data-stu-id="81274-144">Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorConfigurationData</span></span>

## <span data-ttu-id="81274-145">EXIBE</span><span class="sxs-lookup"><span data-stu-id="81274-145">OUTPUTS</span></span>

### <span data-ttu-id="81274-146">Microsoft. Azure. Commands. Advisor. cmdlets. Models. PsAzureAdvisorConfigurationData</span><span class="sxs-lookup"><span data-stu-id="81274-146">Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorConfigurationData</span></span>

## <span data-ttu-id="81274-147">INFORMA</span><span class="sxs-lookup"><span data-stu-id="81274-147">NOTES</span></span>

## <span data-ttu-id="81274-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="81274-148">RELATED LINKS</span></span>
