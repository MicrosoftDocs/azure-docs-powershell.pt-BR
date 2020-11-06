---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2IntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2IntegrationRuntime.md
ms.openlocfilehash: ce842abf58dabb0bdd518f02e7030f3fb2feabc1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93610817"
---
# <span data-ttu-id="79f11-101">Set-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="79f11-101">Set-AzureRmDataFactoryV2IntegrationRuntime</span></span>

## <span data-ttu-id="79f11-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="79f11-102">SYNOPSIS</span></span>
<span data-ttu-id="79f11-103">Atualiza um tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="79f11-103">Updates an integration runtime.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="79f11-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="79f11-104">SYNTAX</span></span>

### <span data-ttu-id="79f11-105">ByIntegrationRuntimeName (padrão)</span><span class="sxs-lookup"><span data-stu-id="79f11-105">ByIntegrationRuntimeName (Default)</span></span>
```
Set-AzureRmDataFactoryV2IntegrationRuntime [-Type <String>] [-Description <String>] [-Location <String>]
 [-NodeSize <String>] [-NodeCount <Int32>] [-CatalogServerEndpoint <String>]
 [-CatalogAdminCredential <PSCredential>] [-CatalogPricingTier <String>] [-VNetId <String>] [-Subnet <String>]
 [-MaxParallelExecutionsPerNode <Int32>] [-Force] [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="79f11-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="79f11-106">ByResourceId</span></span>
```
Set-AzureRmDataFactoryV2IntegrationRuntime [-Type <String>] [-Description <String>] [-Location <String>]
 [-NodeSize <String>] [-NodeCount <Int32>] [-CatalogServerEndpoint <String>]
 [-CatalogAdminCredential <PSCredential>] [-CatalogPricingTier <String>] [-VNetId <String>] [-Subnet <String>]
 [-MaxParallelExecutionsPerNode <Int32>] [-Force] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="79f11-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="79f11-107">ByIntegrationRuntimeObject</span></span>
```
Set-AzureRmDataFactoryV2IntegrationRuntime [-Type <String>] [-Description <String>] [-Location <String>]
 [-NodeSize <String>] [-NodeCount <Int32>] [-CatalogServerEndpoint <String>]
 [-CatalogAdminCredential <PSCredential>] [-CatalogPricingTier <String>] [-VNetId <String>] [-Subnet <String>]
 [-MaxParallelExecutionsPerNode <Int32>] [-Force] [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="79f11-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="79f11-108">DESCRIPTION</span></span>
<span data-ttu-id="79f11-109">O cmdlet Set-AzureRmDataFactoryV2IntegrationRuntime atualiza um tempo de execução de integração com parâmetros específicos.</span><span class="sxs-lookup"><span data-stu-id="79f11-109">The Set-AzureRmDataFactoryV2IntegrationRuntime cmdlet updates an integration runtime with specific parameters.</span></span>

## <span data-ttu-id="79f11-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="79f11-110">EXAMPLES</span></span>

### <span data-ttu-id="79f11-111">Exemplo 1: Descrição da atualização do tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="79f11-111">Example 1: Update integration runtime description.</span></span>
```
PS C:\> Set-AzureRmDataFactoryV2IntegrationRuntime -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir' `
                                            -Description 'New description'

    Id                : /subscriptions/b3ee3a7f-7614-4644-ad07-afa832620b4b/resourceGroups/rg-test-dfv2/providers/Microsoft.DataFactory/factories/test-df-eu2/integrationruntimes/test-selfhost-ir
    ResourceGroupName : rg-test-dfv2
    DataFactoryName   : test-df-eu2
    Name              : test-selfhost-ir
    Description       : New description
```

<span data-ttu-id="79f11-112">O cmdlet atualiza a descrição do tempo de execução de integração chamado ' test-selfhost-IV '.</span><span class="sxs-lookup"><span data-stu-id="79f11-112">The cmdlet updates the description of integration runtime named 'test-selfhost-ir'.</span></span>

## <span data-ttu-id="79f11-113">OS</span><span class="sxs-lookup"><span data-stu-id="79f11-113">PARAMETERS</span></span>

### <span data-ttu-id="79f11-114">-CatalogAdminCredential</span><span class="sxs-lookup"><span data-stu-id="79f11-114">-CatalogAdminCredential</span></span>
<span data-ttu-id="79f11-115">A credencial de administrador do banco de dados de catálogo do tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="79f11-115">The catalog database administrator credential of the integration runtime.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79f11-116">-CatalogPricingTier</span><span class="sxs-lookup"><span data-stu-id="79f11-116">-CatalogPricingTier</span></span>
<span data-ttu-id="79f11-117">O nível de preço do banco de dados do catálogo do tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="79f11-117">The catalog database pricing tier of the integration runtime.</span></span>

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

### <span data-ttu-id="79f11-118">-CatalogServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="79f11-118">-CatalogServerEndpoint</span></span>
<span data-ttu-id="79f11-119">O ponto de extremidade do servidor de banco de dados catálogo do tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="79f11-119">The catalog database server endpoint of the integration runtime.</span></span>

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

### <span data-ttu-id="79f11-120">-Confirme</span><span class="sxs-lookup"><span data-stu-id="79f11-120">-Confirm</span></span>
<span data-ttu-id="79f11-121">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="79f11-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="79f11-122">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="79f11-122">-DataFactoryName</span></span>
<span data-ttu-id="79f11-123">O nome do alocador de dados.</span><span class="sxs-lookup"><span data-stu-id="79f11-123">The data factory name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79f11-124">-Descrição</span><span class="sxs-lookup"><span data-stu-id="79f11-124">-Description</span></span>
<span data-ttu-id="79f11-125">A descrição do tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="79f11-125">The integration runtime description.</span></span>

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

### <span data-ttu-id="79f11-126">-Force</span><span class="sxs-lookup"><span data-stu-id="79f11-126">-Force</span></span>
<span data-ttu-id="79f11-127">Executa o cmdlet sem solicitar confirmação.</span><span class="sxs-lookup"><span data-stu-id="79f11-127">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="79f11-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="79f11-128">-InputObject</span></span>
<span data-ttu-id="79f11-129">O objeto de tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="79f11-129">The integration runtime object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime
Parameter Sets: ByIntegrationRuntimeObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="79f11-130">-Local</span><span class="sxs-lookup"><span data-stu-id="79f11-130">-Location</span></span>
<span data-ttu-id="79f11-131">O local do tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="79f11-131">The integration runtime location.</span></span>

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

### <span data-ttu-id="79f11-132">-MaxParallelExecutionsPerNode</span><span class="sxs-lookup"><span data-stu-id="79f11-132">-MaxParallelExecutionsPerNode</span></span>
<span data-ttu-id="79f11-133">Contagem máxima de execuções paralelas por nó para um tempo de execução de integração dedicada gerenciado.</span><span class="sxs-lookup"><span data-stu-id="79f11-133">Maximum parallel execution count per node for a managed dedicated integration runtime.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79f11-134">-Nome</span><span class="sxs-lookup"><span data-stu-id="79f11-134">-Name</span></span>
<span data-ttu-id="79f11-135">O nome do tempo de execução da integração.</span><span class="sxs-lookup"><span data-stu-id="79f11-135">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName
Aliases: IntegrationRuntimeName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79f11-136">-NodeCount</span><span class="sxs-lookup"><span data-stu-id="79f11-136">-NodeCount</span></span>
<span data-ttu-id="79f11-137">Contagem de nós de destino do tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="79f11-137">Target nodes count of the integration runtime.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79f11-138">-Nós</span><span class="sxs-lookup"><span data-stu-id="79f11-138">-NodeSize</span></span>
<span data-ttu-id="79f11-139">O tamanho do nó do tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="79f11-139">The integration runtime node size.</span></span>

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

### <span data-ttu-id="79f11-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="79f11-140">-ResourceGroupName</span></span>
<span data-ttu-id="79f11-141">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="79f11-141">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79f11-142">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="79f11-142">-ResourceId</span></span>
<span data-ttu-id="79f11-143">A ID do recurso do Azure.</span><span class="sxs-lookup"><span data-stu-id="79f11-143">The Azure resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases: Id

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79f11-144">-Subnet</span><span class="sxs-lookup"><span data-stu-id="79f11-144">-Subnet</span></span>
<span data-ttu-id="79f11-145">O nome da sub-rede na VNet.</span><span class="sxs-lookup"><span data-stu-id="79f11-145">The name of the subnet in the VNet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SubnetName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79f11-146">-Digite</span><span class="sxs-lookup"><span data-stu-id="79f11-146">-Type</span></span>
<span data-ttu-id="79f11-147">O tipo de tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="79f11-147">The integration runtime type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Managed, SelfHosted

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79f11-148">-VNetId</span><span class="sxs-lookup"><span data-stu-id="79f11-148">-VNetId</span></span>
<span data-ttu-id="79f11-149">A ID da VNet que o tempo de execução de integração une.</span><span class="sxs-lookup"><span data-stu-id="79f11-149">The ID of the VNet that the integration runtime joins.</span></span>

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

### <span data-ttu-id="79f11-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="79f11-150">-WhatIf</span></span>
<span data-ttu-id="79f11-151">Mostra o que acontece se o cmdlet for executado, mas não executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="79f11-151">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="79f11-152">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79f11-152">-DefaultProfile</span></span>
<span data-ttu-id="79f11-153">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="79f11-153">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79f11-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79f11-154">CommonParameters</span></span>
<span data-ttu-id="79f11-155">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="79f11-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79f11-156">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="79f11-156">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79f11-157">SENSORES</span><span class="sxs-lookup"><span data-stu-id="79f11-157">INPUTS</span></span>

### <span data-ttu-id="79f11-158">System. String</span><span class="sxs-lookup"><span data-stu-id="79f11-158">System.String</span></span>
<span data-ttu-id="79f11-159">Microsoft. Azure. Commands. DataFactoryV2. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="79f11-159">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="79f11-160">EXIBE</span><span class="sxs-lookup"><span data-stu-id="79f11-160">OUTPUTS</span></span>

### <span data-ttu-id="79f11-161">Microsoft. Azure. Commands. DataFactoryV2. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="79f11-161">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="79f11-162">INFORMA</span><span class="sxs-lookup"><span data-stu-id="79f11-162">NOTES</span></span>

## <span data-ttu-id="79f11-163">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="79f11-163">RELATED LINKS</span></span>

[<span data-ttu-id="79f11-164">Set-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="79f11-164">Set-AzureRmDataFactoryV2IntegrationRuntime</span></span>]()
