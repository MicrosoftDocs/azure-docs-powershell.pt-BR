---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/set-azurermdatafactoryv2integrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2IntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2IntegrationRuntime.md
ms.openlocfilehash: 8b91e1a68fc731476240021889cc80c9c4848357
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429843"
---
# <span data-ttu-id="6a12a-101">Set-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="6a12a-101">Set-AzureRmDataFactoryV2IntegrationRuntime</span></span>

## <span data-ttu-id="6a12a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6a12a-102">SYNOPSIS</span></span>
<span data-ttu-id="6a12a-103">Atualiza um tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="6a12a-103">Updates an integration runtime.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6a12a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6a12a-104">SYNTAX</span></span>

### <span data-ttu-id="6a12a-105">ByIntegrationRuntimeName (padrão)</span><span class="sxs-lookup"><span data-stu-id="6a12a-105">ByIntegrationRuntimeName (Default)</span></span>
```
Set-AzureRmDataFactoryV2IntegrationRuntime [-Type <String>] [-Description <String>] [-Location <String>]
 [-NodeSize <String>] [-NodeCount <Int32>] [-CatalogServerEndpoint <String>]
 [-CatalogAdminCredential <PSCredential>] [-CatalogPricingTier <String>] [-VNetId <String>] [-Subnet <String>]
 [-SetupScriptContainerSasUri <String>] [-Edition <String>] [-MaxParallelExecutionsPerNode <Int32>]
 [-LicenseType <String>] [-AuthKey <SecureString>] [-Force] [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6a12a-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="6a12a-106">ByResourceId</span></span>
```
Set-AzureRmDataFactoryV2IntegrationRuntime [-Type <String>] [-Description <String>] [-Location <String>]
 [-NodeSize <String>] [-NodeCount <Int32>] [-CatalogServerEndpoint <String>]
 [-CatalogAdminCredential <PSCredential>] [-CatalogPricingTier <String>] [-VNetId <String>] [-Subnet <String>]
 [-SetupScriptContainerSasUri <String>] [-Edition <String>] [-MaxParallelExecutionsPerNode <Int32>]
 [-LicenseType <String>] [-AuthKey <SecureString>] [-Force] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6a12a-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="6a12a-107">ByIntegrationRuntimeObject</span></span>
```
Set-AzureRmDataFactoryV2IntegrationRuntime [-Type <String>] [-Description <String>] [-Location <String>]
 [-NodeSize <String>] [-NodeCount <Int32>] [-CatalogServerEndpoint <String>]
 [-CatalogAdminCredential <PSCredential>] [-CatalogPricingTier <String>] [-VNetId <String>] [-Subnet <String>]
 [-SetupScriptContainerSasUri <String>] [-Edition <String>] [-MaxParallelExecutionsPerNode <Int32>]
 [-LicenseType <String>] [-AuthKey <SecureString>] [-Force] [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6a12a-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6a12a-108">DESCRIPTION</span></span>
<span data-ttu-id="6a12a-109">O cmdlet Set-AzureRmDataFactoryV2IntegrationRuntime atualiza um tempo de execução de integração com parâmetros específicos.</span><span class="sxs-lookup"><span data-stu-id="6a12a-109">The Set-AzureRmDataFactoryV2IntegrationRuntime cmdlet updates an integration runtime with specific parameters.</span></span>

## <span data-ttu-id="6a12a-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6a12a-110">EXAMPLES</span></span>

### <span data-ttu-id="6a12a-111">Exemplo 1: Descrição da atualização do tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="6a12a-111">Example 1: Update integration runtime description.</span></span>
```
PS C:\> Set-AzureRmDataFactoryV2IntegrationRuntime -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir' `
                                            -Description 'New description'

    Id                : /subscriptions/b3ee3a7f-7614-4644-ad07-afa832620b4b/resourceGroups/rg-test-dfv2/providers/Microsoft.DataFactory/factories/test-df-eu2/integrationruntimes/test-selfhost-ir
    ResourceGroupName : rg-test-dfv2
    DataFactoryName   : test-df-eu2
    Name              : test-selfhost-ir
    Description       : New description
```

<span data-ttu-id="6a12a-112">O cmdlet atualiza a descrição do tempo de execução de integração chamado ' test-selfhost-IV '.</span><span class="sxs-lookup"><span data-stu-id="6a12a-112">The cmdlet updates the description of integration runtime named 'test-selfhost-ir'.</span></span>

## <span data-ttu-id="6a12a-113">OS</span><span class="sxs-lookup"><span data-stu-id="6a12a-113">PARAMETERS</span></span>

### <span data-ttu-id="6a12a-114">-AuthKey</span><span class="sxs-lookup"><span data-stu-id="6a12a-114">-AuthKey</span></span>
<span data-ttu-id="6a12a-115">A chave de autenticação do tempo de execução de integração de hospedagem interna.</span><span class="sxs-lookup"><span data-stu-id="6a12a-115">The authentication key of the self-hosted integration runtime.</span></span>

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a12a-116">-CatalogAdminCredential</span><span class="sxs-lookup"><span data-stu-id="6a12a-116">-CatalogAdminCredential</span></span>
<span data-ttu-id="6a12a-117">A credencial de administrador do banco de dados de catálogo do tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="6a12a-117">The catalog database administrator credential of the integration runtime.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a12a-118">-CatalogPricingTier</span><span class="sxs-lookup"><span data-stu-id="6a12a-118">-CatalogPricingTier</span></span>
<span data-ttu-id="6a12a-119">O nível de preço do banco de dados do catálogo do tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="6a12a-119">The catalog database pricing tier of the integration runtime.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a12a-120">-CatalogServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="6a12a-120">-CatalogServerEndpoint</span></span>
<span data-ttu-id="6a12a-121">O ponto de extremidade do servidor de banco de dados catálogo do tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="6a12a-121">The catalog database server endpoint of the integration runtime.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a12a-122">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="6a12a-122">-DataFactoryName</span></span>
<span data-ttu-id="6a12a-123">O nome do alocador de dados.</span><span class="sxs-lookup"><span data-stu-id="6a12a-123">The data factory name.</span></span>

```yaml
Type: String
Parameter Sets: ByIntegrationRuntimeName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6a12a-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a12a-124">-DefaultProfile</span></span>
<span data-ttu-id="6a12a-125">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6a12a-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6a12a-126">-Descrição</span><span class="sxs-lookup"><span data-stu-id="6a12a-126">-Description</span></span>
<span data-ttu-id="6a12a-127">A descrição do tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="6a12a-127">The integration runtime description.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a12a-128">-Edição</span><span class="sxs-lookup"><span data-stu-id="6a12a-128">-Edition</span></span>
<span data-ttu-id="6a12a-129">A edição para o tempo de execução de integração do SSIS que pode ser Standard ou Enterprise, o padrão é padrão se não for especificado.</span><span class="sxs-lookup"><span data-stu-id="6a12a-129">The edition for SSIS integration runtime which could be Standard or Enterprise, default is Standard if it is not specified.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Standard, Enterprise

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a12a-130">-Force</span><span class="sxs-lookup"><span data-stu-id="6a12a-130">-Force</span></span>
<span data-ttu-id="6a12a-131">Executa o cmdlet sem solicitar confirmação.</span><span class="sxs-lookup"><span data-stu-id="6a12a-131">Runs the cmdlet without prompting for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a12a-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6a12a-132">-InputObject</span></span>
<span data-ttu-id="6a12a-133">O objeto de tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="6a12a-133">The integration runtime object.</span></span>

```yaml
Type: PSIntegrationRuntime
Parameter Sets: ByIntegrationRuntimeObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6a12a-134">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="6a12a-134">-LicenseType</span></span>
<span data-ttu-id="6a12a-135">O tipo de licença que você deseja selecionar para o SSIS IV.</span><span class="sxs-lookup"><span data-stu-id="6a12a-135">The license type that you want to select for the SSIS IR.</span></span> <span data-ttu-id="6a12a-136">Há dois tipos: LicenseIncluded ou BasePrice.</span><span class="sxs-lookup"><span data-stu-id="6a12a-136">There are two types: LicenseIncluded or BasePrice.</span></span> <span data-ttu-id="6a12a-137">Se você estiver qualificado para o preço do Azure Hybrid use beneficie-se (AHUB), selecione BasePrice.</span><span class="sxs-lookup"><span data-stu-id="6a12a-137">If you are qualified for the Azure Hybrid Use Benefit (AHUB) pricing, please select BasePrice.</span></span> <span data-ttu-id="6a12a-138">Caso contrário, selecione LicenseIncluded.</span><span class="sxs-lookup"><span data-stu-id="6a12a-138">If not, please select LicenseIncluded.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: LicenseIncluded, BasePrice

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a12a-139">-Local</span><span class="sxs-lookup"><span data-stu-id="6a12a-139">-Location</span></span>
<span data-ttu-id="6a12a-140">O local do tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="6a12a-140">The integration runtime location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a12a-141">-MaxParallelExecutionsPerNode</span><span class="sxs-lookup"><span data-stu-id="6a12a-141">-MaxParallelExecutionsPerNode</span></span>
<span data-ttu-id="6a12a-142">Contagem máxima de execuções paralelas por nó para um tempo de execução de integração dedicada gerenciado.</span><span class="sxs-lookup"><span data-stu-id="6a12a-142">Maximum parallel execution count per node for a managed dedicated integration runtime.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a12a-143">-Nome</span><span class="sxs-lookup"><span data-stu-id="6a12a-143">-Name</span></span>
<span data-ttu-id="6a12a-144">O nome do tempo de execução da integração.</span><span class="sxs-lookup"><span data-stu-id="6a12a-144">The integration runtime name.</span></span>

```yaml
Type: String
Parameter Sets: ByIntegrationRuntimeName
Aliases: IntegrationRuntimeName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6a12a-145">-NodeCount</span><span class="sxs-lookup"><span data-stu-id="6a12a-145">-NodeCount</span></span>
<span data-ttu-id="6a12a-146">Contagem de nós de destino do tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="6a12a-146">Target nodes count of the integration runtime.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a12a-147">-Nós</span><span class="sxs-lookup"><span data-stu-id="6a12a-147">-NodeSize</span></span>
<span data-ttu-id="6a12a-148">O tamanho do nó do tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="6a12a-148">The integration runtime node size.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a12a-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6a12a-149">-ResourceGroupName</span></span>
<span data-ttu-id="6a12a-150">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="6a12a-150">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByIntegrationRuntimeName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6a12a-151">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6a12a-151">-ResourceId</span></span>
<span data-ttu-id="6a12a-152">A ID do recurso do Azure.</span><span class="sxs-lookup"><span data-stu-id="6a12a-152">The Azure resource ID.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases: Id

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6a12a-153">-SetupScriptContainerSasUri</span><span class="sxs-lookup"><span data-stu-id="6a12a-153">-SetupScriptContainerSasUri</span></span>
<span data-ttu-id="6a12a-154">O URI da SAS do contêiner de blob do Azure que contém o script de instalação personalizada.</span><span class="sxs-lookup"><span data-stu-id="6a12a-154">The SAS URI of the Azure blob container that contains the custom setup script.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a12a-155">-Subnet</span><span class="sxs-lookup"><span data-stu-id="6a12a-155">-Subnet</span></span>
<span data-ttu-id="6a12a-156">O nome da sub-rede na VNet.</span><span class="sxs-lookup"><span data-stu-id="6a12a-156">The name of the subnet in the VNet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SubnetName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a12a-157">-Digite</span><span class="sxs-lookup"><span data-stu-id="6a12a-157">-Type</span></span>
<span data-ttu-id="6a12a-158">O tipo de tempo de execução de integração.</span><span class="sxs-lookup"><span data-stu-id="6a12a-158">The integration runtime type.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Managed, SelfHosted

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a12a-159">-VNetId</span><span class="sxs-lookup"><span data-stu-id="6a12a-159">-VNetId</span></span>
<span data-ttu-id="6a12a-160">A ID da VNet que o tempo de execução de integração une.</span><span class="sxs-lookup"><span data-stu-id="6a12a-160">The ID of the VNet that the integration runtime joins.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a12a-161">-Confirme</span><span class="sxs-lookup"><span data-stu-id="6a12a-161">-Confirm</span></span>
<span data-ttu-id="6a12a-162">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6a12a-162">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6a12a-163">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6a12a-163">-WhatIf</span></span>
<span data-ttu-id="6a12a-164">Mostra o que acontece se o cmdlet for executado, mas não executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6a12a-164">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="6a12a-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a12a-165">CommonParameters</span></span>
<span data-ttu-id="6a12a-166">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6a12a-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a12a-167">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6a12a-167">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a12a-168">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6a12a-168">INPUTS</span></span>

### <span data-ttu-id="6a12a-169">System. String</span><span class="sxs-lookup"><span data-stu-id="6a12a-169">System.String</span></span>
<span data-ttu-id="6a12a-170">Microsoft. Azure. Commands. DataFactoryV2. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="6a12a-170">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="6a12a-171">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6a12a-171">OUTPUTS</span></span>

### <span data-ttu-id="6a12a-172">Microsoft. Azure. Commands. DataFactoryV2. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="6a12a-172">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="6a12a-173">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6a12a-173">NOTES</span></span>

## <span data-ttu-id="6a12a-174">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6a12a-174">RELATED LINKS</span></span>

[<span data-ttu-id="6a12a-175">Set-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="6a12a-175">Set-AzureRmDataFactoryV2IntegrationRuntime</span></span>]()
