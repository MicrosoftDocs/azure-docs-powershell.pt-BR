---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Add-AzWebAppAccessRestrictionRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Add-AzWebAppAccessRestrictionRule.md
ms.openlocfilehash: b28cb8ac408ff281930eac68bf2b97d288150dd6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113897"
---
# <span data-ttu-id="5b16e-101">Add-AzWebAppAccessRestrictionRule</span><span class="sxs-lookup"><span data-stu-id="5b16e-101">Add-AzWebAppAccessRestrictionRule</span></span>

## <span data-ttu-id="5b16e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5b16e-102">SYNOPSIS</span></span>
<span data-ttu-id="5b16e-103">Adiciona uma regra de Restiction do Access a um Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="5b16e-103">Adds an Access Restiction rule to an Azure Web App.</span></span>

## <span data-ttu-id="5b16e-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5b16e-104">SYNTAX</span></span>

### <span data-ttu-id="5b16e-105">IpAddressParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="5b16e-105">IpAddressParameterSet (Default)</span></span>
```
Add-AzWebAppAccessRestrictionRule [-ResourceGroupName] <String> [-WebAppName] <String> [-Name <String>]
 [-Description <String>] -Priority <UInt32> [-Action <String>] [-SlotName <String>] [-TargetScmSite]
 -IpAddress <String> [-PassThru] [-HttpHeader <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5b16e-106">ServiceTagParameterSet</span><span class="sxs-lookup"><span data-stu-id="5b16e-106">ServiceTagParameterSet</span></span>
```
Add-AzWebAppAccessRestrictionRule [-ResourceGroupName] <String> [-WebAppName] <String> [-Name <String>]
 [-Description <String>] -Priority <UInt32> [-Action <String>] [-SlotName <String>] [-TargetScmSite]
 [-PassThru] -ServiceTag <String> [-HttpHeader <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5b16e-107">SubnetNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="5b16e-107">SubnetNameParameterSet</span></span>
```
Add-AzWebAppAccessRestrictionRule [-ResourceGroupName] <String> [-WebAppName] <String> [-Name <String>]
 [-Description <String>] -Priority <UInt32> [-Action <String>] [-SlotName <String>] [-TargetScmSite]
 -SubnetName <String> -VirtualNetworkName <String> [-IgnoreMissingServiceEndpoint] [-PassThru]
 [-HttpHeader <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5b16e-108">SubnetIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5b16e-108">SubnetIdParameterSet</span></span>
```
Add-AzWebAppAccessRestrictionRule [-ResourceGroupName] <String> [-WebAppName] <String> [-Name <String>]
 [-Description <String>] -Priority <UInt32> [-Action <String>] [-SlotName <String>] [-TargetScmSite]
 -SubnetId <String> [-IgnoreMissingServiceEndpoint] [-PassThru] [-HttpHeader <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5b16e-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="5b16e-109">DESCRIPTION</span></span>
<span data-ttu-id="5b16e-110">O cmdlet **Add-AzWebAppAccessRestrictionRule** adiciona uma regra de Restrição do Access a um Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="5b16e-110">The **Add-AzWebAppAccessRestrictionRule** cmdlet adds an Access Restriction rule to an Azure Web App.</span></span>

## <span data-ttu-id="5b16e-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="5b16e-111">EXAMPLES</span></span>

### <span data-ttu-id="5b16e-112">Exemplo 1: Adicionar a regra de Restrição de Acesso IpAddress a um Aplicativo Web</span><span class="sxs-lookup"><span data-stu-id="5b16e-112">Example 1: Add IpAddress Access Restriction rule to a Web App</span></span>
```
PS C:\>Add-AzWebAppAccessRestrictionRule -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite" 
-Name IpRule -Priority 200 -Action Allow -IpAddress 10.10.0.0/8
```

<span data-ttu-id="5b16e-113">Esse comando adiciona uma regra de restrição de acesso com prioridade 200 e intervalo ip a um Web App chamado ContosoSite que pertence ao grupo de recursos Default-Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="5b16e-113">This command adds an access restriction rule with priority 200 and ip range to a Web App named ContosoSite that belongs to the resource group Default-Web-WestUS.</span></span>

### <span data-ttu-id="5b16e-114">Exemplo 2: Adicionar a regra de Restrição de Acesso do Ponto de Extremidade do Serviço de Sub-rede a um Aplicativo Web</span><span class="sxs-lookup"><span data-stu-id="5b16e-114">Example 2: Add Subnet Service Endpoint Access Restriction rule to a Web App</span></span>
```
PS C:\>Add-AzWebAppAccessRestrictionRule -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite" 
-Name SubnetRule -Priority 300 -Action Allow -SubnetName appgw-subnet -VirtualNetworkName corp-vnet
```

<span data-ttu-id="5b16e-115">Este comando adiciona uma regra de restrição de acesso com prioridade 300 e com a sub-rede appgw-subnet na corp-vnet a um Web App chamado ContosoSite que pertence ao grupo de recursos Default-Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="5b16e-115">This command adds an access restriction rule with priority 300 and with subnet appgw-subnet in corp-vnet to a Web App named ContosoSite that belongs to the resource group Default-Web-WestUS.</span></span>

### <span data-ttu-id="5b16e-116">Exemplo 3: Adicionar regra de Restrição de Acesso ServiceTag a um Aplicativo Web</span><span class="sxs-lookup"><span data-stu-id="5b16e-116">Example 3: Add ServiceTag Access Restriction rule to a Web App</span></span>
```
PS C:\>Add-AzWebAppAccessRestrictionRule -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite" 
-Name ServiceTagRule -Priority 200 -Action Allow -ServiceTag AzureFrontDoor.Backend
```

<span data-ttu-id="5b16e-117">Esse comando adiciona uma regra de restrição de acesso com prioridade 200 e uma Marca de Serviço que representa o escopo ip do Azure Front Door a um Web App chamado ContosoSite que pertence ao grupo de recursos Default-Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="5b16e-117">This command adds an access restriction rule with priority 200 and a Service Tag representing the ip scope of Azure Front Door to a Web App named ContosoSite that belongs to the resource group Default-Web-WestUS.</span></span>

### <span data-ttu-id="5b16e-118">Exemplo 4: Adicionar regra de Restrição de Acesso de vários endereços a um Web App</span><span class="sxs-lookup"><span data-stu-id="5b16e-118">Example 4: Add multi-address Access Restriction rule to a Web App</span></span>
```
PS C:\>Add-AzWebAppAccessRestrictionRule -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite" 
-Name MultipleIpRule -Priority 200 -Action Allow -IpAddress "10.10.0.0/8,192.168.0.0/16"
```

<span data-ttu-id="5b16e-119">Esse comando adiciona uma regra de restrição de acesso com prioridade 200 e dois intervalos ip a um Web App chamado ContosoSite que pertence ao grupo de recursos Default-Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="5b16e-119">This command adds an access restriction rule with priority 200 and two ip ranges to a Web App named ContosoSite that belongs to the resource group Default-Web-WestUS.</span></span>

### <span data-ttu-id="5b16e-120">Exemplo 5: Adicionar regra de Restrição de Acesso com cabeçalho http a um Aplicativo Web</span><span class="sxs-lookup"><span data-stu-id="5b16e-120">Example 5: Add Access Restriction rule with http header to a Web App</span></span>
```
PS C:\>Add-AzWebAppAccessRestrictionRule -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite" 
-Name MultipleIpRule -Priority 400 -Action Allow -ServiceTag AzureFrontDoor.Backend
-HttpHeader @{'x-forwarded-host' = 'www.contoso.com', 'app.contoso.com'; 'x-azure-fdid' = '355deb06-47c4-4ba4-9641-c7d7a98b913e'}
```

<span data-ttu-id="5b16e-121">Este comando adiciona uma regra de restrição de acesso com prioridade 400 para a Marca de Serviço AzureFrontDoor.Backend e restringe ainda mais o acesso somente a cabeçalhos http de determinados valores a um Web App chamado ContosoSite que pertence ao grupo de recursos Default-Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="5b16e-121">This command adds an access restriction rule with priority 400 for Service Tag AzureFrontDoor.Backend and further restricts access only to http headers of certain values to a Web App named ContosoSite that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="5b16e-122">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5b16e-122">PARAMETERS</span></span>

### <span data-ttu-id="5b16e-123">-Ação</span><span class="sxs-lookup"><span data-stu-id="5b16e-123">-Action</span></span>
<span data-ttu-id="5b16e-124">Regra Permitir ou Negar.</span><span class="sxs-lookup"><span data-stu-id="5b16e-124">Allow or Deny rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Allow, Deny

Required: False
Position: Named
Default value: Allow
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b16e-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b16e-125">-DefaultProfile</span></span>
<span data-ttu-id="5b16e-126">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="5b16e-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5b16e-127">-Descrição</span><span class="sxs-lookup"><span data-stu-id="5b16e-127">-Description</span></span>
<span data-ttu-id="5b16e-128">Descrição da Restrição do Access.</span><span class="sxs-lookup"><span data-stu-id="5b16e-128">Access Restriction description.</span></span>

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

### <span data-ttu-id="5b16e-129">-httpHeader</span><span class="sxs-lookup"><span data-stu-id="5b16e-129">-HttpHeader</span></span>
<span data-ttu-id="5b16e-130">Restrições de cabeçalho http.</span><span class="sxs-lookup"><span data-stu-id="5b16e-130">Http header restrictions.</span></span> <span data-ttu-id="5b16e-131">Exemplo: -httpHeader @{'x-azure-fdid' = '7acacb02-47ea-4cd4-b568-5e880e72582e'; 'x-forwarded-host' = 'www.contoso.com', 'app.contoso.com'}</span><span class="sxs-lookup"><span data-stu-id="5b16e-131">Example: -HttpHeader @{'x-azure-fdid' = '7acacb02-47ea-4cd4-b568-5e880e72582e'; 'x-forwarded-host' = 'www.contoso.com', 'app.contoso.com'}</span></span>

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

### <span data-ttu-id="5b16e-132">-IgnoreMissingServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="5b16e-132">-IgnoreMissingServiceEndpoint</span></span>
<span data-ttu-id="5b16e-133">Especifique se o registro do Ponto de Extremidade de Serviço na Sub-rede deve ser validado.</span><span class="sxs-lookup"><span data-stu-id="5b16e-133">Specify if Service Endpoint registration at Subnet should be validated.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SubnetNameParameterSet, SubnetIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b16e-134">-IpAddress</span><span class="sxs-lookup"><span data-stu-id="5b16e-134">-IpAddress</span></span>
<span data-ttu-id="5b16e-135">Ip Address v4 ou v6 CIDR range.</span><span class="sxs-lookup"><span data-stu-id="5b16e-135">Ip Address v4 or v6 CIDR range.</span></span> <span data-ttu-id="5b16e-136">Por exemplo: 192.168.0.0/24</span><span class="sxs-lookup"><span data-stu-id="5b16e-136">E.g.: 192.168.0.0/24</span></span>

```yaml
Type: System.String
Parameter Sets: IpAddressParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b16e-137">-Nome</span><span class="sxs-lookup"><span data-stu-id="5b16e-137">-Name</span></span>
<span data-ttu-id="5b16e-138">Nome da Regra</span><span class="sxs-lookup"><span data-stu-id="5b16e-138">Rule Name</span></span>

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

### <span data-ttu-id="5b16e-139">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5b16e-139">-PassThru</span></span>
<span data-ttu-id="5b16e-140">Retornar o objeto de configuração de restrição de acesso.</span><span class="sxs-lookup"><span data-stu-id="5b16e-140">Return the access restriction config object.</span></span>

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

### <span data-ttu-id="5b16e-141">-Prioridade</span><span class="sxs-lookup"><span data-stu-id="5b16e-141">-Priority</span></span>
<span data-ttu-id="5b16e-142">Prioridade da Restrição do Access.</span><span class="sxs-lookup"><span data-stu-id="5b16e-142">Access Restriction priority.</span></span> <span data-ttu-id="5b16e-143">Por exemplo: 500.</span><span class="sxs-lookup"><span data-stu-id="5b16e-143">E.g.: 500.</span></span>

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b16e-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5b16e-144">-ResourceGroupName</span></span>
<span data-ttu-id="5b16e-145">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="5b16e-145">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5b16e-146">-ServiceTag</span><span class="sxs-lookup"><span data-stu-id="5b16e-146">-ServiceTag</span></span>
<span data-ttu-id="5b16e-147">Nome da marca de serviço</span><span class="sxs-lookup"><span data-stu-id="5b16e-147">Name of Service Tag</span></span>

```yaml
Type: System.String
Parameter Sets: ServiceTagParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b16e-148">-SlotName</span><span class="sxs-lookup"><span data-stu-id="5b16e-148">-SlotName</span></span>
<span data-ttu-id="5b16e-149">Nome do Slot de Implantação.</span><span class="sxs-lookup"><span data-stu-id="5b16e-149">Deployment Slot name.</span></span>

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

### <span data-ttu-id="5b16e-150">-Sub-RedeId</span><span class="sxs-lookup"><span data-stu-id="5b16e-150">-SubnetId</span></span>
<span data-ttu-id="5b16e-151">ResourceId da Sub-rede.</span><span class="sxs-lookup"><span data-stu-id="5b16e-151">ResourceId of Subnet.</span></span>

```yaml
Type: System.String
Parameter Sets: SubnetIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b16e-152">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="5b16e-152">-SubnetName</span></span>
<span data-ttu-id="5b16e-153">Nome da Sub-rede.</span><span class="sxs-lookup"><span data-stu-id="5b16e-153">Name of Subnet.</span></span>

```yaml
Type: System.String
Parameter Sets: SubnetNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b16e-154">-TargetScmSite</span><span class="sxs-lookup"><span data-stu-id="5b16e-154">-TargetScmSite</span></span>
<span data-ttu-id="5b16e-155">A regra destina-se ao site principal ou ao site Scm.</span><span class="sxs-lookup"><span data-stu-id="5b16e-155">Rule is aimed for Main site or Scm site.</span></span>

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

### <span data-ttu-id="5b16e-156">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="5b16e-156">-VirtualNetworkName</span></span>
<span data-ttu-id="5b16e-157">Nome da Rede Virtual.</span><span class="sxs-lookup"><span data-stu-id="5b16e-157">Name of Virtual Network.</span></span>

```yaml
Type: System.String
Parameter Sets: SubnetNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b16e-158">-WebAppName</span><span class="sxs-lookup"><span data-stu-id="5b16e-158">-WebAppName</span></span>
<span data-ttu-id="5b16e-159">O nome do aplicativo Web.</span><span class="sxs-lookup"><span data-stu-id="5b16e-159">The name of the web app.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5b16e-160">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="5b16e-160">-Confirm</span></span>
<span data-ttu-id="5b16e-161">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5b16e-161">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5b16e-162">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5b16e-162">-WhatIf</span></span>
<span data-ttu-id="5b16e-163">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="5b16e-163">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5b16e-164">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="5b16e-164">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5b16e-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b16e-165">CommonParameters</span></span>
<span data-ttu-id="5b16e-166">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5b16e-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b16e-167">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5b16e-167">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b16e-168">Entradas</span><span class="sxs-lookup"><span data-stu-id="5b16e-168">INPUTS</span></span>

### <span data-ttu-id="5b16e-169">System.String</span><span class="sxs-lookup"><span data-stu-id="5b16e-169">System.String</span></span>

## <span data-ttu-id="5b16e-170">Saídas</span><span class="sxs-lookup"><span data-stu-id="5b16e-170">OUTPUTS</span></span>

### <span data-ttu-id="5b16e-171">Microsoft.Azure.Commands.WebApps.Models.PSAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="5b16e-171">Microsoft.Azure.Commands.WebApps.Models.PSAccessRestrictionConfig</span></span>

## <span data-ttu-id="5b16e-172">Notas</span><span class="sxs-lookup"><span data-stu-id="5b16e-172">NOTES</span></span>

## <span data-ttu-id="5b16e-173">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5b16e-173">RELATED LINKS</span></span>

[<span data-ttu-id="5b16e-174">Update-AzWebAppAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="5b16e-174">Update-AzWebAppAccessRestrictionConfig</span></span>](./Update-AzWebAppAccessRestrictionConfig.md)

[<span data-ttu-id="5b16e-175">Get-AzWebAppAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="5b16e-175">Get-AzWebAppAccessRestrictionConfig</span></span>](./Get-AzWebAppAccessRestrictionConfig.md)

[<span data-ttu-id="5b16e-176">Remove-AzWebAppAccessRestrictionRule</span><span class="sxs-lookup"><span data-stu-id="5b16e-176">Remove-AzWebAppAccessRestrictionRule</span></span>](./Remove-AzWebAppAccessRestrictionRule.md)
