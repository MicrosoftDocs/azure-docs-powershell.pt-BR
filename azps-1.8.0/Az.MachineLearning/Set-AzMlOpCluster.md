---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearningCompute.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/set-azmlopcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Set-AzMlOpCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Set-AzMlOpCluster.md
ms.openlocfilehash: 833b3456cd39e4589ceaf37e0c86fd654c250ddc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93770415"
---
# <span data-ttu-id="9b2ac-101">Set-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="9b2ac-101">Set-AzMlOpCluster</span></span>

## <span data-ttu-id="9b2ac-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9b2ac-102">SYNOPSIS</span></span>
<span data-ttu-id="9b2ac-103">Define as propriedades de um cluster de operação.</span><span class="sxs-lookup"><span data-stu-id="9b2ac-103">Sets the properties of an operationalization cluster.</span></span>

## <span data-ttu-id="9b2ac-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9b2ac-104">SYNTAX</span></span>

### <span data-ttu-id="9b2ac-105">SetByIndividualParameters (padrão)</span><span class="sxs-lookup"><span data-stu-id="9b2ac-105">SetByIndividualParameters (Default)</span></span>
```
Set-AzMlOpCluster -ResourceGroupName <String> -Name <String> [-AgentCount <Int32>] [-SslStatus <String>]
 [-SslCertificate <String>] [-SslKey <String>] [-SslCName <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9b2ac-106">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="9b2ac-106">SetByInputObject</span></span>
```
Set-AzMlOpCluster -InputObject <PSOperationalizationCluster> [-AgentCount <Int32>] [-SslStatus <String>]
 [-SslCertificate <String>] [-SslKey <String>] [-SslCName <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9b2ac-107">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="9b2ac-107">SetByResourceId</span></span>
```
Set-AzMlOpCluster -ResourceId <String> [-AgentCount <Int32>] [-SslStatus <String>] [-SslCertificate <String>]
 [-SslKey <String>] [-SslCName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9b2ac-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9b2ac-108">DESCRIPTION</span></span>
<span data-ttu-id="9b2ac-109">Define todas as propriedades de um cluster de operação.</span><span class="sxs-lookup"><span data-stu-id="9b2ac-109">Sets all the properties of an operationalization cluster.</span></span> <span data-ttu-id="9b2ac-110">Como ele define todas as propriedades ao usar um objeto de cluster, um objeto de entrada totalmente válido deve ser passado.</span><span class="sxs-lookup"><span data-stu-id="9b2ac-110">Since it sets all the properties when using a cluster object a fully valid input object must be passed.</span></span> <span data-ttu-id="9b2ac-111">As propriedades somente leitura serão ignoradas.</span><span class="sxs-lookup"><span data-stu-id="9b2ac-111">Read-only properties will be ignored.</span></span> <span data-ttu-id="9b2ac-112">Somente algumas propriedades podem ser atualizadas no momento, conforme mostrado nos conjuntos de parâmetros.</span><span class="sxs-lookup"><span data-stu-id="9b2ac-112">Only some properties are currently updatable, as shown in the parameter sets.</span></span>

## <span data-ttu-id="9b2ac-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9b2ac-113">EXAMPLES</span></span>

### <span data-ttu-id="9b2ac-114">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="9b2ac-114">Example 1</span></span>
<span data-ttu-id="9b2ac-115">Atualize um cluster usando parâmetros individuais.</span><span class="sxs-lookup"><span data-stu-id="9b2ac-115">Update a cluster using individual parameters.</span></span>

```
PS C:\> Set-AzMlOpCluster -ResourceGroupName my-rg -ClusterName my-cluster -AgentCount 5
```

### <span data-ttu-id="9b2ac-116">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="9b2ac-116">Example 2</span></span>
<span data-ttu-id="9b2ac-117">Atualize um cluster usando um objeto de entrada.</span><span class="sxs-lookup"><span data-stu-id="9b2ac-117">Update a cluster using an input object.</span></span>

```
PS C:\> $cluster = Get-AzMlOpCluster -ResourceGroupName my-rg -ClusterName my-cluster
PS C:\> $cluster.ContainerService.AgentCount = 5
PS C:\> Set-AzMlOpCluster -InputObject $cluster
```

## <span data-ttu-id="9b2ac-118">OS</span><span class="sxs-lookup"><span data-stu-id="9b2ac-118">PARAMETERS</span></span>

### <span data-ttu-id="9b2ac-119">-AgentCount</span><span class="sxs-lookup"><span data-stu-id="9b2ac-119">-AgentCount</span></span>
<span data-ttu-id="9b2ac-120">O número de nós de agente no cluster ACS.</span><span class="sxs-lookup"><span data-stu-id="9b2ac-120">The number of agent nodes in the ACS cluster.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: SetByIndividualParameters, SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: SetByInputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b2ac-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b2ac-121">-DefaultProfile</span></span>
<span data-ttu-id="9b2ac-122">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9b2ac-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9b2ac-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9b2ac-123">-InputObject</span></span>
<span data-ttu-id="9b2ac-124">As propriedades do cluster de operação.</span><span class="sxs-lookup"><span data-stu-id="9b2ac-124">The operationalization cluster properties.</span></span>

```yaml
Type: Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster
Parameter Sets: SetByInputObject
Aliases: Cluster

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9b2ac-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="9b2ac-125">-Name</span></span>
<span data-ttu-id="9b2ac-126">O nome do cluster de operação.</span><span class="sxs-lookup"><span data-stu-id="9b2ac-126">The name of the operationalization cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIndividualParameters
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b2ac-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9b2ac-127">-ResourceGroupName</span></span>
<span data-ttu-id="9b2ac-128">O nome do grupo de recursos para o cluster de operação.</span><span class="sxs-lookup"><span data-stu-id="9b2ac-128">The name of the resource group for the operationalization cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIndividualParameters
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b2ac-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9b2ac-129">-ResourceId</span></span>
<span data-ttu-id="9b2ac-130">A ID de recurso do Azure para o cluster de operação.</span><span class="sxs-lookup"><span data-stu-id="9b2ac-130">The Azure resource id for the operationalization cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b2ac-131">-SslCertificate</span><span class="sxs-lookup"><span data-stu-id="9b2ac-131">-SslCertificate</span></span>
<span data-ttu-id="9b2ac-132">Os dados do certificado SSL no formato PEM.</span><span class="sxs-lookup"><span data-stu-id="9b2ac-132">The SSL certificate data in PEM format.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIndividualParameters, SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SetByInputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b2ac-133">-SslCName</span><span class="sxs-lookup"><span data-stu-id="9b2ac-133">-SslCName</span></span>
<span data-ttu-id="9b2ac-134">O CName do certificado SSL.</span><span class="sxs-lookup"><span data-stu-id="9b2ac-134">The CName for the SSL certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIndividualParameters, SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SetByInputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b2ac-135">-SslKey</span><span class="sxs-lookup"><span data-stu-id="9b2ac-135">-SslKey</span></span>
<span data-ttu-id="9b2ac-136">Os dados da chave SSL no formato PEM.</span><span class="sxs-lookup"><span data-stu-id="9b2ac-136">The SSL key data in PEM format.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIndividualParameters, SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SetByInputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b2ac-137">-SslStatus</span><span class="sxs-lookup"><span data-stu-id="9b2ac-137">-SslStatus</span></span>
<span data-ttu-id="9b2ac-138">Status da SSL.</span><span class="sxs-lookup"><span data-stu-id="9b2ac-138">SSL status.</span></span>
<span data-ttu-id="9b2ac-139">Os valores possíveis são ' Enabled ' e ' disabled '.</span><span class="sxs-lookup"><span data-stu-id="9b2ac-139">Possible values are 'Enabled' and 'Disabled'.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIndividualParameters, SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SetByInputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b2ac-140">-Confirme</span><span class="sxs-lookup"><span data-stu-id="9b2ac-140">-Confirm</span></span>
<span data-ttu-id="9b2ac-141">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9b2ac-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9b2ac-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9b2ac-142">-WhatIf</span></span>
<span data-ttu-id="9b2ac-143">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="9b2ac-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9b2ac-144">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="9b2ac-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9b2ac-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b2ac-145">CommonParameters</span></span>
<span data-ttu-id="9b2ac-146">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9b2ac-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b2ac-147">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9b2ac-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b2ac-148">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9b2ac-148">INPUTS</span></span>

### <span data-ttu-id="9b2ac-149">Microsoft. Azure. Commands. MachineLearningCompute. Models. PSOperationalizationCluster</span><span class="sxs-lookup"><span data-stu-id="9b2ac-149">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster</span></span>

### <span data-ttu-id="9b2ac-150">System. String</span><span class="sxs-lookup"><span data-stu-id="9b2ac-150">System.String</span></span>

### <span data-ttu-id="9b2ac-151">System. Nullable ' 1 [[System. Int32, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="9b2ac-151">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="9b2ac-152">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9b2ac-152">OUTPUTS</span></span>

### <span data-ttu-id="9b2ac-153">Microsoft. Azure. Commands. MachineLearningCompute. Models. PSOperationalizationCluster</span><span class="sxs-lookup"><span data-stu-id="9b2ac-153">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster</span></span>

## <span data-ttu-id="9b2ac-154">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9b2ac-154">NOTES</span></span>

## <span data-ttu-id="9b2ac-155">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9b2ac-155">RELATED LINKS</span></span>
