---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/powershell/module/az.websites/new-azappserviceenvironment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzAppServiceEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzAppServiceEnvironment.md
ms.openlocfilehash: a922958ec2e15ea9cb4a3b0189f74dda6d71eab2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101893044"
---
# <span data-ttu-id="687ee-101">New-AzAppServiceEnvironment</span><span class="sxs-lookup"><span data-stu-id="687ee-101">New-AzAppServiceEnvironment</span></span>

## <span data-ttu-id="687ee-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="687ee-102">SYNOPSIS</span></span>
<span data-ttu-id="687ee-103">Cria um ambiente de serviço de aplicativo, incluindo a Tabela de Rota recomendada e o Grupo de Segurança de Rede</span><span class="sxs-lookup"><span data-stu-id="687ee-103">Creates an App Service Environment including the recommended Route Table and Network Security Group</span></span>

## <span data-ttu-id="687ee-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="687ee-104">SYNTAX</span></span>

### <span data-ttu-id="687ee-105">ASEv2SubnetNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="687ee-105">ASEv2SubnetNameParameterSet</span></span>
```
New-AzAppServiceEnvironment [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-Kind] <String>] -VirtualNetworkName <String> -SubnetName <String> -LoadBalancerMode <String>
 [-SkipRouteTable] [-SkipNetworkSecurityGroup] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="687ee-106">ASEv3SubnetNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="687ee-106">ASEv3SubnetNameParameterSet</span></span>
```
New-AzAppServiceEnvironment [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-Kind] <String>] -VirtualNetworkName <String> -SubnetName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="687ee-107">ASEv2SubnetIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="687ee-107">ASEv2SubnetIdParameterSet</span></span>
```
New-AzAppServiceEnvironment [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-Kind] <String>] -SubnetId <String> -LoadBalancerMode <String> [-SkipRouteTable] [-SkipNetworkSecurityGroup]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="687ee-108">ASEv3SubnetIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="687ee-108">ASEv3SubnetIdParameterSet</span></span>
```
New-AzAppServiceEnvironment [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-Kind] <String>] -SubnetId <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="687ee-109">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="687ee-109">DESCRIPTION</span></span>
<span data-ttu-id="687ee-110">O cmdlet **New-AzAppServiceEnvironment** cria um Ambiente de Serviço de Aplicativo.</span><span class="sxs-lookup"><span data-stu-id="687ee-110">The **New-AzAppServiceEnvironment** cmdlet creates an App Service Environment.</span></span>

## <span data-ttu-id="687ee-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="687ee-111">EXAMPLES</span></span>

### <span data-ttu-id="687ee-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="687ee-112">Example 1</span></span>
```powershell
PS C:\> New-AzAppServiceEnvironment -ResourceGroupName MyResourceGroup -Name MyAseV2 -Location WestEurope 
        -VirtualNetworkName MyVirtualNetwork -SubnetName AseSubnet -LoadBalancerMode Internal
```

<span data-ttu-id="687ee-113">Criar ambiente de serviço de aplicativo chamado MyAseV2, incluindo tabela de rota recomendada e grupo de segurança de rede</span><span class="sxs-lookup"><span data-stu-id="687ee-113">Create App Service Environment named MyAseV2 including recommended Route Table and Network Security Group</span></span>

### <span data-ttu-id="687ee-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="687ee-114">Example 2</span></span>
```powershell
PS C:\> New-AzAppServiceEnvironment -ResourceGroupName MyResourceGroup -Name MyAseV2 -Location WestEurope 
        -VirtualNetworkName MyVirtualNetwork -SubnetName AseSubnet -LoadBalancerMode Internal
        -SkipRouteTable -SkipNetworkSecurityGroup
```

<span data-ttu-id="687ee-115">Crie um ambiente de serviço de aplicativo chamado MyAseV2 sem a Tabela de Rota recomendada e o Grupo de Segurança de Rede.</span><span class="sxs-lookup"><span data-stu-id="687ee-115">Create App Service Environment named MyAseV2 without recommended Route Table and Network Security Group.</span></span>
<span data-ttu-id="687ee-116">Eles devem ser criado antes ou logo após o provisionamento do Ambiente de Serviço de Aplicativo para garantir uma instância funcional.</span><span class="sxs-lookup"><span data-stu-id="687ee-116">These should be create before or right after provisioning the App Service Environment to ensure a functional instance.</span></span>

## <span data-ttu-id="687ee-117">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="687ee-117">PARAMETERS</span></span>

### <span data-ttu-id="687ee-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="687ee-118">-AsJob</span></span>
<span data-ttu-id="687ee-119">Execute o cmdlet em segundo plano e retorne um Trabalho para controlar o progresso.</span><span class="sxs-lookup"><span data-stu-id="687ee-119">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="687ee-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="687ee-120">-DefaultProfile</span></span>
<span data-ttu-id="687ee-121">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="687ee-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="687ee-122">-Kind</span><span class="sxs-lookup"><span data-stu-id="687ee-122">-Kind</span></span>
<span data-ttu-id="687ee-123">A versão do ambiente de serviço de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="687ee-123">The version of the app service environment.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: ASEv2, ASEv3

Required: False
Position: 3
Default value: ASEv2
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="687ee-124">-LoadBalancerMode</span><span class="sxs-lookup"><span data-stu-id="687ee-124">-LoadBalancerMode</span></span>
<span data-ttu-id="687ee-125">Modo balanceador de carga do ambiente de serviço do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="687ee-125">Load balancer mode of the app service environment.</span></span>

```yaml
Type: System.String
Parameter Sets: ASEv2SubnetNameParameterSet, ASEv2SubnetIdParameterSet
Aliases:
Accepted values: Internal, External

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="687ee-126">-Location</span><span class="sxs-lookup"><span data-stu-id="687ee-126">-Location</span></span>
<span data-ttu-id="687ee-127">O local do ambiente de serviço de aplicativo, por exemplo: Europa Ocidental.</span><span class="sxs-lookup"><span data-stu-id="687ee-127">The Location of the app service environment eg: West Europe.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="687ee-128">-Name</span><span class="sxs-lookup"><span data-stu-id="687ee-128">-Name</span></span>
<span data-ttu-id="687ee-129">O nome do ambiente de serviço de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="687ee-129">The name of the app service environment.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="687ee-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="687ee-130">-PassThru</span></span>
<span data-ttu-id="687ee-131">Retornar o objeto do ambiente de serviço do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="687ee-131">Return the app service environment object.</span></span>

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

### <span data-ttu-id="687ee-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="687ee-132">-ResourceGroupName</span></span>
<span data-ttu-id="687ee-133">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="687ee-133">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="687ee-134">-SkipNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="687ee-134">-SkipNetworkSecurityGroup</span></span>
<span data-ttu-id="687ee-135">Não crie o grupo de segurança de rede recomendado como parte do ambiente de serviço de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="687ee-135">Do not create the recommended network security group as part of the app service environment.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ASEv2SubnetNameParameterSet, ASEv2SubnetIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="687ee-136">-SkipRouteTable</span><span class="sxs-lookup"><span data-stu-id="687ee-136">-SkipRouteTable</span></span>
<span data-ttu-id="687ee-137">Não crie a tabela de rota recomendada como parte do ambiente de serviço do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="687ee-137">Do not create the recommended route table as part of the app service environment.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ASEv2SubnetNameParameterSet, ASEv2SubnetIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="687ee-138">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="687ee-138">-SubnetId</span></span>
<span data-ttu-id="687ee-139">A id da sub-rede.</span><span class="sxs-lookup"><span data-stu-id="687ee-139">The subnet id.</span></span>

```yaml
Type: System.String
Parameter Sets: ASEv2SubnetIdParameterSet, ASEv3SubnetIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="687ee-140">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="687ee-140">-SubnetName</span></span>
<span data-ttu-id="687ee-141">O nome da sub-rede.</span><span class="sxs-lookup"><span data-stu-id="687ee-141">The subnet name.</span></span> <span data-ttu-id="687ee-142">Usado em combinação com -VirtualNetworkName e deve estar no mesmo grupo de recursos que o ASE.</span><span class="sxs-lookup"><span data-stu-id="687ee-142">Used in combination with -VirtualNetworkName and must be in same resource group as ASE.</span></span> <span data-ttu-id="687ee-143">Caso não seja, use -SubnetId</span><span class="sxs-lookup"><span data-stu-id="687ee-143">If not, use -SubnetId</span></span>

```yaml
Type: System.String
Parameter Sets: ASEv2SubnetNameParameterSet, ASEv3SubnetNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="687ee-144">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="687ee-144">-VirtualNetworkName</span></span>
<span data-ttu-id="687ee-145">O nome da vNet.</span><span class="sxs-lookup"><span data-stu-id="687ee-145">The vNet name.</span></span> <span data-ttu-id="687ee-146">Usado em combinação com -SubnetName e deve estar no mesmo grupo de recursos que o ASE.</span><span class="sxs-lookup"><span data-stu-id="687ee-146">Used in combination with -SubnetName and must be in same resource group as ASE.</span></span> <span data-ttu-id="687ee-147">Caso não seja, use -SubnetId</span><span class="sxs-lookup"><span data-stu-id="687ee-147">If not, use -SubnetId</span></span>

```yaml
Type: System.String
Parameter Sets: ASEv2SubnetNameParameterSet, ASEv3SubnetNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="687ee-148">-Confirm</span><span class="sxs-lookup"><span data-stu-id="687ee-148">-Confirm</span></span>
<span data-ttu-id="687ee-149">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="687ee-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="687ee-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="687ee-150">-WhatIf</span></span>
<span data-ttu-id="687ee-151">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="687ee-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="687ee-152">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="687ee-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="687ee-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="687ee-153">CommonParameters</span></span>
<span data-ttu-id="687ee-154">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="687ee-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="687ee-155">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="687ee-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="687ee-156">INPUTS</span><span class="sxs-lookup"><span data-stu-id="687ee-156">INPUTS</span></span>

### <span data-ttu-id="687ee-157">Nenhum</span><span class="sxs-lookup"><span data-stu-id="687ee-157">None</span></span>

## <span data-ttu-id="687ee-158">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="687ee-158">OUTPUTS</span></span>

### <span data-ttu-id="687ee-159">System.Object</span><span class="sxs-lookup"><span data-stu-id="687ee-159">System.Object</span></span>
## <span data-ttu-id="687ee-160">NOTES</span><span class="sxs-lookup"><span data-stu-id="687ee-160">NOTES</span></span>

## <span data-ttu-id="687ee-161">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="687ee-161">RELATED LINKS</span></span>

[<span data-ttu-id="687ee-162">Get-AzAppServiceEnvironment</span><span class="sxs-lookup"><span data-stu-id="687ee-162">Get-AzAppServiceEnvironment</span></span>](./Get-AzAppServiceEnvironment.md)

[<span data-ttu-id="687ee-163">New-AzAppServiceEnvironmentInboundServices</span><span class="sxs-lookup"><span data-stu-id="687ee-163">New-AzAppServiceEnvironmentInboundServices</span></span>](./New-AzAppServiceEnvironmentInboundServices.md)

[<span data-ttu-id="687ee-164">Remove-AzAppServiceEnvironment</span><span class="sxs-lookup"><span data-stu-id="687ee-164">Remove-AzAppServiceEnvironment</span></span>](./Remove-AzAppServiceEnvironment.md)
