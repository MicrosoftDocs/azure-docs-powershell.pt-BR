---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/set-azdatafactoryv2integrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2IntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2IntegrationRuntime.md
ms.openlocfilehash: e92d04e60132463b22741242f411f6af5d09c2b0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93771006"
---
# <span data-ttu-id="3b296-101">Set-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="3b296-101">Set-AzDataFactoryV2IntegrationRuntime</span></span>

## <span data-ttu-id="3b296-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3b296-102">SYNOPSIS</span></span>
<span data-ttu-id="3b296-103">Atualiza um tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="3b296-103">Updates an integration runtime.</span></span>

## <span data-ttu-id="3b296-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3b296-104">SYNTAX</span></span>

### <span data-ttu-id="3b296-105">ByIntegrationRuntimeName (padrão)</span><span class="sxs-lookup"><span data-stu-id="3b296-105">ByIntegrationRuntimeName (Default)</span></span>
```
Set-AzDataFactoryV2IntegrationRuntime [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Name] <String> [-Type <String>] [-Description <String>] [-Location <String>] [-NodeSize <String>]
 [-NodeCount <Int32>] [-CatalogServerEndpoint <String>] [-CatalogAdminCredential <PSCredential>]
 [-CatalogPricingTier <String>] [-VNetId <String>] [-Subnet <String>] [-SetupScriptContainerSasUri <String>]
 [-Edition <String>] [-MaxParallelExecutionsPerNode <Int32>] [-LicenseType <String>] [-AuthKey <SecureString>]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3b296-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="3b296-106">ByResourceId</span></span>
```
Set-AzDataFactoryV2IntegrationRuntime [-ResourceId] <String> [-Type <String>] [-Description <String>]
 [-Location <String>] [-NodeSize <String>] [-NodeCount <Int32>] [-CatalogServerEndpoint <String>]
 [-CatalogAdminCredential <PSCredential>] [-CatalogPricingTier <String>] [-VNetId <String>] [-Subnet <String>]
 [-SetupScriptContainerSasUri <String>] [-Edition <String>] [-MaxParallelExecutionsPerNode <Int32>]
 [-LicenseType <String>] [-AuthKey <SecureString>] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3b296-107">ByLinkedIntegrationRuntimeResourceId</span><span class="sxs-lookup"><span data-stu-id="3b296-107">ByLinkedIntegrationRuntimeResourceId</span></span>
```
Set-AzDataFactoryV2IntegrationRuntime [-ResourceId] <String> [-Type <String>] [-Description <String>]
 -SharedIntegrationRuntimeResourceId <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3b296-108">ByLinkedIntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="3b296-108">ByLinkedIntegrationRuntimeName</span></span>
```
Set-AzDataFactoryV2IntegrationRuntime [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Name] <String> [-Type <String>] [-Description <String>] -SharedIntegrationRuntimeResourceId <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3b296-109">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="3b296-109">ByIntegrationRuntimeObject</span></span>
```
Set-AzDataFactoryV2IntegrationRuntime [-InputObject] <PSIntegrationRuntime> [-Type <String>]
 [-Description <String>] [-Location <String>] [-NodeSize <String>] [-NodeCount <Int32>]
 [-CatalogServerEndpoint <String>] [-CatalogAdminCredential <PSCredential>] [-CatalogPricingTier <String>]
 [-VNetId <String>] [-Subnet <String>] [-SetupScriptContainerSasUri <String>] [-Edition <String>]
 [-MaxParallelExecutionsPerNode <Int32>] [-LicenseType <String>] [-AuthKey <SecureString>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3b296-110">ByLinkedIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="3b296-110">ByLinkedIntegrationRuntimeObject</span></span>
```
Set-AzDataFactoryV2IntegrationRuntime [-InputObject] <PSIntegrationRuntime> [-Type <String>]
 [-Description <String>] -SharedIntegrationRuntimeResourceId <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3b296-111">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3b296-111">DESCRIPTION</span></span>
<span data-ttu-id="3b296-112">O cmdlet Set-AzDataFactoryV2IntegrationRuntime atualiza um tempo de execução de integração com parâmetros específicos.</span><span class="sxs-lookup"><span data-stu-id="3b296-112">The Set-AzDataFactoryV2IntegrationRuntime cmdlet updates an integration runtime with specific parameters.</span></span>

## <span data-ttu-id="3b296-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3b296-113">EXAMPLES</span></span>

### <span data-ttu-id="3b296-114">Exemplo 1: Descrição da atualização do tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="3b296-114">Example 1: Update integration runtime description.</span></span>
```
PS C:\> Set-AzDataFactoryV2IntegrationRuntime -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir' `
                                            -Description 'New description'

    Id                : /subscriptions/b3ee3a7f-7614-4644-ad07-afa832620b4b/resourceGroups/rg-test-dfv2/providers/Microsoft.DataFactory/factories/test-df-eu2/integrationruntimes/test-selfhost-ir
    ResourceGroupName : rg-test-dfv2
    DataFactoryName   : test-df-eu2
    Name              : test-selfhost-ir
    Description       : New description
```

<span data-ttu-id="3b296-115">O cmdlet atualiza a descrição do tempo de execução de integração chamado ' test-selfhost-IV '.</span><span class="sxs-lookup"><span data-stu-id="3b296-115">The cmdlet updates the description of integration runtime named 'test-selfhost-ir'.</span></span>

### <span data-ttu-id="3b296-116">Exemplo 2: compartilhar o tempo de execução de integração de hospedagem automática.</span><span class="sxs-lookup"><span data-stu-id="3b296-116">Example 2: Share Self-hosted integration runtime.</span></span>
```
PS C:\> Set-AzDataFactoryV2IntegrationRuntime -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir' `
                                            -SharedIntegrationRuntimeResourceId '/subscriptions/b3ee3a7f-7614-4644-ad07-afa832620b4b/resourceGroups/rg-test-dfv2/providers/Microsoft.DataFactory/factories/test-df-eu2/integrationruntimes/test-selfhost-ir' -Type "SelfHosted"

    Id                : /subscriptions/b3ee3a7f-7614-4644-ad07-afa832620b4b/resourceGroups/rg-test-dfv2/providers/Microsoft.DataFactory/factories/test-df-eu2/integrationruntimes/test-selfhost-ir
    ResourceGroupName : rg-test-dfv2
    DataFactoryName   : test-df-eu2
    Name              : test-selfhost-ir
    Description       : New description
```

<span data-ttu-id="3b296-117">O cmdlet adiciona o ADF para usar o tempo de execução de integração compartilhada.</span><span class="sxs-lookup"><span data-stu-id="3b296-117">The cmdlet adds the ADF to use the shared integration runtime.</span></span> <span data-ttu-id="3b296-118">Ao usar `-SharedIntegrationRuntimeResourceId` o parâmetro, o `-Type` também deve ser incluído.</span><span class="sxs-lookup"><span data-stu-id="3b296-118">When using `-SharedIntegrationRuntimeResourceId` parameter the `-Type` must also be included.</span></span> <span data-ttu-id="3b296-119">Observe que a fábrica de dados precisa receber permissão para usar o tempo de execução de integração antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3b296-119">Note that the data factory need to be granted permission to use the integration runtime before running cmdlet.</span></span>

## <span data-ttu-id="3b296-120">OS</span><span class="sxs-lookup"><span data-stu-id="3b296-120">PARAMETERS</span></span>

### <span data-ttu-id="3b296-121">-AuthKey</span><span class="sxs-lookup"><span data-stu-id="3b296-121">-AuthKey</span></span>
<span data-ttu-id="3b296-122">A chave de autenticação do tempo de execução de integração de hospedagem interna.</span><span class="sxs-lookup"><span data-stu-id="3b296-122">The authentication key of the self-hosted integration runtime.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: ByIntegrationRuntimeName, ByResourceId, ByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b296-123">-CatalogAdminCredential</span><span class="sxs-lookup"><span data-stu-id="3b296-123">-CatalogAdminCredential</span></span>
<span data-ttu-id="3b296-124">A credencial de administrador do banco de dados de catálogo do tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="3b296-124">The catalog database administrator credential of the integration runtime.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: ByIntegrationRuntimeName, ByResourceId, ByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b296-125">-CatalogPricingTier</span><span class="sxs-lookup"><span data-stu-id="3b296-125">-CatalogPricingTier</span></span>
<span data-ttu-id="3b296-126">O nível de preço do banco de dados do catálogo do tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="3b296-126">The catalog database pricing tier of the integration runtime.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName, ByResourceId, ByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b296-127">-CatalogServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="3b296-127">-CatalogServerEndpoint</span></span>
<span data-ttu-id="3b296-128">O ponto de extremidade do servidor de banco de dados catálogo do tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="3b296-128">The catalog database server endpoint of the integration runtime.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName, ByResourceId, ByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b296-129">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="3b296-129">-DataFactoryName</span></span>
<span data-ttu-id="3b296-130">O nome do alocador de dados.</span><span class="sxs-lookup"><span data-stu-id="3b296-130">The data factory name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName, ByLinkedIntegrationRuntimeName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b296-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b296-131">-DefaultProfile</span></span>
<span data-ttu-id="3b296-132">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3b296-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3b296-133">-Descrição</span><span class="sxs-lookup"><span data-stu-id="3b296-133">-Description</span></span>
<span data-ttu-id="3b296-134">A descrição do tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="3b296-134">The integration runtime description.</span></span>

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

### <span data-ttu-id="3b296-135">-Edição</span><span class="sxs-lookup"><span data-stu-id="3b296-135">-Edition</span></span>
<span data-ttu-id="3b296-136">A edição para o tempo de execução de integração do SSIS que pode ser Standard ou Enterprise, o padrão é padrão se não for especificado.</span><span class="sxs-lookup"><span data-stu-id="3b296-136">The edition for SSIS integration runtime which could be Standard or Enterprise, default is Standard if it is not specified.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName, ByResourceId, ByIntegrationRuntimeObject
Aliases:
Accepted values: Standard, Enterprise

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b296-137">-Force</span><span class="sxs-lookup"><span data-stu-id="3b296-137">-Force</span></span>
<span data-ttu-id="3b296-138">Executa o cmdlet sem solicitar confirmação.</span><span class="sxs-lookup"><span data-stu-id="3b296-138">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="3b296-139">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3b296-139">-InputObject</span></span>
<span data-ttu-id="3b296-140">O objeto de tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="3b296-140">The integration runtime object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime
Parameter Sets: ByIntegrationRuntimeObject, ByLinkedIntegrationRuntimeObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3b296-141">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="3b296-141">-LicenseType</span></span>
<span data-ttu-id="3b296-142">O tipo de licença que você deseja selecionar para o SSIS IV.</span><span class="sxs-lookup"><span data-stu-id="3b296-142">The license type that you want to select for the SSIS IR.</span></span> <span data-ttu-id="3b296-143">Há dois tipos: LicenseIncluded ou BasePrice.</span><span class="sxs-lookup"><span data-stu-id="3b296-143">There are two types: LicenseIncluded or BasePrice.</span></span> <span data-ttu-id="3b296-144">Se você estiver qualificado para o preço do Azure Hybrid use beneficie-se (AHUB), selecione BasePrice.</span><span class="sxs-lookup"><span data-stu-id="3b296-144">If you are qualified for the Azure Hybrid Use Benefit (AHUB) pricing, please select BasePrice.</span></span> <span data-ttu-id="3b296-145">Caso contrário, selecione LicenseIncluded.</span><span class="sxs-lookup"><span data-stu-id="3b296-145">If not, please select LicenseIncluded.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName, ByResourceId, ByIntegrationRuntimeObject
Aliases:
Accepted values: LicenseIncluded, BasePrice

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b296-146">-Local</span><span class="sxs-lookup"><span data-stu-id="3b296-146">-Location</span></span>
<span data-ttu-id="3b296-147">O local do tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="3b296-147">The integration runtime location.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName, ByResourceId, ByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b296-148">-MaxParallelExecutionsPerNode</span><span class="sxs-lookup"><span data-stu-id="3b296-148">-MaxParallelExecutionsPerNode</span></span>
<span data-ttu-id="3b296-149">Contagem máxima de execuções paralelas por nó para um tempo de execução de integração dedicada gerenciado.</span><span class="sxs-lookup"><span data-stu-id="3b296-149">Maximum parallel execution count per node for a managed dedicated integration runtime.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: ByIntegrationRuntimeName, ByResourceId, ByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b296-150">-Nome</span><span class="sxs-lookup"><span data-stu-id="3b296-150">-Name</span></span>
<span data-ttu-id="3b296-151">O nome do tempo de execução da integração.</span><span class="sxs-lookup"><span data-stu-id="3b296-151">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName, ByLinkedIntegrationRuntimeName
Aliases: IntegrationRuntimeName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b296-152">-NodeCount</span><span class="sxs-lookup"><span data-stu-id="3b296-152">-NodeCount</span></span>
<span data-ttu-id="3b296-153">Contagem de nós de destino do tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="3b296-153">Target nodes count of the integration runtime.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: ByIntegrationRuntimeName, ByResourceId, ByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b296-154">-Nós</span><span class="sxs-lookup"><span data-stu-id="3b296-154">-NodeSize</span></span>
<span data-ttu-id="3b296-155">O tamanho do nó do tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="3b296-155">The integration runtime node size.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName, ByResourceId, ByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b296-156">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3b296-156">-ResourceGroupName</span></span>
<span data-ttu-id="3b296-157">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="3b296-157">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName, ByLinkedIntegrationRuntimeName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b296-158">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3b296-158">-ResourceId</span></span>
<span data-ttu-id="3b296-159">A ID do recurso do Azure.</span><span class="sxs-lookup"><span data-stu-id="3b296-159">The Azure resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId, ByLinkedIntegrationRuntimeResourceId
Aliases: Id

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b296-160">-SetupScriptContainerSasUri</span><span class="sxs-lookup"><span data-stu-id="3b296-160">-SetupScriptContainerSasUri</span></span>
<span data-ttu-id="3b296-161">O URI da SAS do contêiner de blob do Azure que contém o script de instalação personalizada.</span><span class="sxs-lookup"><span data-stu-id="3b296-161">The SAS URI of the Azure blob container that contains the custom setup script.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName, ByResourceId, ByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b296-162">-SharedIntegrationRuntimeResourceId</span><span class="sxs-lookup"><span data-stu-id="3b296-162">-SharedIntegrationRuntimeResourceId</span></span>
<span data-ttu-id="3b296-163">A ID do recurso do tempo de execução de integração de hospedagem automática compartilhada.</span><span class="sxs-lookup"><span data-stu-id="3b296-163">The resource id of the shared self-hosted integration runtime.</span></span>

```yaml
Type: System.String
Parameter Sets: ByLinkedIntegrationRuntimeResourceId, ByLinkedIntegrationRuntimeName, ByLinkedIntegrationRuntimeObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b296-164">-Subnet</span><span class="sxs-lookup"><span data-stu-id="3b296-164">-Subnet</span></span>
<span data-ttu-id="3b296-165">O nome da sub-rede na VNet.</span><span class="sxs-lookup"><span data-stu-id="3b296-165">The name of the subnet in the VNet.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName, ByResourceId, ByIntegrationRuntimeObject
Aliases: SubnetName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b296-166">-Digite</span><span class="sxs-lookup"><span data-stu-id="3b296-166">-Type</span></span>
<span data-ttu-id="3b296-167">O tipo de tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="3b296-167">The integration runtime type.</span></span>

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

### <span data-ttu-id="3b296-168">-VNetId</span><span class="sxs-lookup"><span data-stu-id="3b296-168">-VNetId</span></span>
<span data-ttu-id="3b296-169">A ID da VNet que o tempo de execução de integração une.</span><span class="sxs-lookup"><span data-stu-id="3b296-169">The ID of the VNet that the integration runtime joins.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName, ByResourceId, ByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b296-170">-Confirme</span><span class="sxs-lookup"><span data-stu-id="3b296-170">-Confirm</span></span>
<span data-ttu-id="3b296-171">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3b296-171">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3b296-172">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3b296-172">-WhatIf</span></span>
<span data-ttu-id="3b296-173">Mostra o que acontece se o cmdlet for executado, mas não executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3b296-173">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="3b296-174">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b296-174">CommonParameters</span></span>
<span data-ttu-id="3b296-175">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3b296-175">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b296-176">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3b296-176">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b296-177">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3b296-177">INPUTS</span></span>

### <span data-ttu-id="3b296-178">System. String</span><span class="sxs-lookup"><span data-stu-id="3b296-178">System.String</span></span>

### <span data-ttu-id="3b296-179">Microsoft. Azure. Commands. DataFactoryV2. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="3b296-179">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="3b296-180">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3b296-180">OUTPUTS</span></span>

### <span data-ttu-id="3b296-181">Microsoft. Azure. Commands. DataFactoryV2. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="3b296-181">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="3b296-182">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3b296-182">NOTES</span></span>

## <span data-ttu-id="3b296-183">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3b296-183">RELATED LINKS</span></span>

[<span data-ttu-id="3b296-184">Set-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="3b296-184">Set-AzDataFactoryV2IntegrationRuntime</span></span>]()
