---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Add-AzWebAppAccessRestrictionRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Add-AzWebAppAccessRestrictionRule.md
ms.openlocfilehash: b28cb8ac408ff281930eac68bf2b97d288150dd6
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98427842"
---
# <span data-ttu-id="3ff94-101">Add-AzWebAppAccessRestrictionRule</span><span class="sxs-lookup"><span data-stu-id="3ff94-101">Add-AzWebAppAccessRestrictionRule</span></span>

## <span data-ttu-id="3ff94-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3ff94-102">SYNOPSIS</span></span>
<span data-ttu-id="3ff94-103">Adiciona uma regra de restiction do Access a um aplicativo Web do Azure.</span><span class="sxs-lookup"><span data-stu-id="3ff94-103">Adds an Access Restiction rule to an Azure Web App.</span></span>

## <span data-ttu-id="3ff94-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3ff94-104">SYNTAX</span></span>

### <span data-ttu-id="3ff94-105">IpAddressParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="3ff94-105">IpAddressParameterSet (Default)</span></span>
```
Add-AzWebAppAccessRestrictionRule [-ResourceGroupName] <String> [-WebAppName] <String> [-Name <String>]
 [-Description <String>] -Priority <UInt32> [-Action <String>] [-SlotName <String>] [-TargetScmSite]
 -IpAddress <String> [-PassThru] [-HttpHeader <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3ff94-106">ServiceTagParameterSet</span><span class="sxs-lookup"><span data-stu-id="3ff94-106">ServiceTagParameterSet</span></span>
```
Add-AzWebAppAccessRestrictionRule [-ResourceGroupName] <String> [-WebAppName] <String> [-Name <String>]
 [-Description <String>] -Priority <UInt32> [-Action <String>] [-SlotName <String>] [-TargetScmSite]
 [-PassThru] -ServiceTag <String> [-HttpHeader <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3ff94-107">SubnetNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="3ff94-107">SubnetNameParameterSet</span></span>
```
Add-AzWebAppAccessRestrictionRule [-ResourceGroupName] <String> [-WebAppName] <String> [-Name <String>]
 [-Description <String>] -Priority <UInt32> [-Action <String>] [-SlotName <String>] [-TargetScmSite]
 -SubnetName <String> -VirtualNetworkName <String> [-IgnoreMissingServiceEndpoint] [-PassThru]
 [-HttpHeader <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3ff94-108">SubnetIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3ff94-108">SubnetIdParameterSet</span></span>
```
Add-AzWebAppAccessRestrictionRule [-ResourceGroupName] <String> [-WebAppName] <String> [-Name <String>]
 [-Description <String>] -Priority <UInt32> [-Action <String>] [-SlotName <String>] [-TargetScmSite]
 -SubnetId <String> [-IgnoreMissingServiceEndpoint] [-PassThru] [-HttpHeader <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3ff94-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3ff94-109">DESCRIPTION</span></span>
<span data-ttu-id="3ff94-110">O cmdlet **Add-AzWebAppAccessRestrictionRule** adiciona uma regra de restrição de acesso a um aplicativo Web do Azure.</span><span class="sxs-lookup"><span data-stu-id="3ff94-110">The **Add-AzWebAppAccessRestrictionRule** cmdlet adds an Access Restriction rule to an Azure Web App.</span></span>

## <span data-ttu-id="3ff94-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3ff94-111">EXAMPLES</span></span>

### <span data-ttu-id="3ff94-112">Exemplo 1: Adicionar regra de restrição de acesso IpAddress a um aplicativo Web</span><span class="sxs-lookup"><span data-stu-id="3ff94-112">Example 1: Add IpAddress Access Restriction rule to a Web App</span></span>
```
PS C:\>Add-AzWebAppAccessRestrictionRule -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite" 
-Name IpRule -Priority 200 -Action Allow -IpAddress 10.10.0.0/8
```

<span data-ttu-id="3ff94-113">Esse comando adiciona uma regra de restrição de acesso com Priority 200 e intervalo de IP a um aplicativo Web chamado ContosoSite que pertence ao grupo de recursos-Web-Westus padrão.</span><span class="sxs-lookup"><span data-stu-id="3ff94-113">This command adds an access restriction rule with priority 200 and ip range to a Web App named ContosoSite that belongs to the resource group Default-Web-WestUS.</span></span>

### <span data-ttu-id="3ff94-114">Exemplo 2: Adicionar regra de restrição de acesso de ponto de extremidade do serviço de sub-rede a um aplicativo Web</span><span class="sxs-lookup"><span data-stu-id="3ff94-114">Example 2: Add Subnet Service Endpoint Access Restriction rule to a Web App</span></span>
```
PS C:\>Add-AzWebAppAccessRestrictionRule -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite" 
-Name SubnetRule -Priority 300 -Action Allow -SubnetName appgw-subnet -VirtualNetworkName corp-vnet
```

<span data-ttu-id="3ff94-115">Esse comando adiciona uma regra de restrição de acesso com prioridade 300 e com o subnet appgw-subnet em Corp-vnet a um aplicativo Web chamado ContosoSite que pertence à parte padrão do grupo de recursos-Oesteus.</span><span class="sxs-lookup"><span data-stu-id="3ff94-115">This command adds an access restriction rule with priority 300 and with subnet appgw-subnet in corp-vnet to a Web App named ContosoSite that belongs to the resource group Default-Web-WestUS.</span></span>

### <span data-ttu-id="3ff94-116">Exemplo 3: Adicionar regra de restrição de acesso ServiceTag a um aplicativo Web</span><span class="sxs-lookup"><span data-stu-id="3ff94-116">Example 3: Add ServiceTag Access Restriction rule to a Web App</span></span>
```
PS C:\>Add-AzWebAppAccessRestrictionRule -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite" 
-Name ServiceTagRule -Priority 200 -Action Allow -ServiceTag AzureFrontDoor.Backend
```

<span data-ttu-id="3ff94-117">Esse comando adiciona uma regra de restrição de acesso com Priority 200 e uma etiqueta de serviço que representa o escopo de IP da porta frontal do Azure a um aplicativo Web chamado ContosoSite que pertence à parte padrão do grupo de recursos-Oesteus.</span><span class="sxs-lookup"><span data-stu-id="3ff94-117">This command adds an access restriction rule with priority 200 and a Service Tag representing the ip scope of Azure Front Door to a Web App named ContosoSite that belongs to the resource group Default-Web-WestUS.</span></span>

### <span data-ttu-id="3ff94-118">Exemplo 4: Adicionar regra de restrição de acesso de vários endereços a um aplicativo Web</span><span class="sxs-lookup"><span data-stu-id="3ff94-118">Example 4: Add multi-address Access Restriction rule to a Web App</span></span>
```
PS C:\>Add-AzWebAppAccessRestrictionRule -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite" 
-Name MultipleIpRule -Priority 200 -Action Allow -IpAddress "10.10.0.0/8,192.168.0.0/16"
```

<span data-ttu-id="3ff94-119">Esse comando adiciona uma regra de restrição de acesso com Priority 200 e dois intervalos de IP a um aplicativo Web chamado ContosoSite que pertence à grupo de recursos padrão-Oesteus.</span><span class="sxs-lookup"><span data-stu-id="3ff94-119">This command adds an access restriction rule with priority 200 and two ip ranges to a Web App named ContosoSite that belongs to the resource group Default-Web-WestUS.</span></span>

### <span data-ttu-id="3ff94-120">Exemplo 5: Adicionar regra de restrição de acesso com cabeçalho HTTP a um aplicativo Web</span><span class="sxs-lookup"><span data-stu-id="3ff94-120">Example 5: Add Access Restriction rule with http header to a Web App</span></span>
```
PS C:\>Add-AzWebAppAccessRestrictionRule -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite" 
-Name MultipleIpRule -Priority 400 -Action Allow -ServiceTag AzureFrontDoor.Backend
-HttpHeader @{'x-forwarded-host' = 'www.contoso.com', 'app.contoso.com'; 'x-azure-fdid' = '355deb06-47c4-4ba4-9641-c7d7a98b913e'}
```

<span data-ttu-id="3ff94-121">Esse comando adiciona uma regra de restrição de acesso com Priority 400 para a etiqueta de serviço AzureFrontDoor. back-end e restringe o acesso somente a cabeçalhos HTTP de certos valores para um aplicativo Web chamado ContosoSite que pertence ao grupo de recursos padrão-Web-Oesteus.</span><span class="sxs-lookup"><span data-stu-id="3ff94-121">This command adds an access restriction rule with priority 400 for Service Tag AzureFrontDoor.Backend and further restricts access only to http headers of certain values to a Web App named ContosoSite that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="3ff94-122">OS</span><span class="sxs-lookup"><span data-stu-id="3ff94-122">PARAMETERS</span></span>

### <span data-ttu-id="3ff94-123">-Ação</span><span class="sxs-lookup"><span data-stu-id="3ff94-123">-Action</span></span>
<span data-ttu-id="3ff94-124">Regra de permissão ou negação.</span><span class="sxs-lookup"><span data-stu-id="3ff94-124">Allow or Deny rule.</span></span>

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

### <span data-ttu-id="3ff94-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ff94-125">-DefaultProfile</span></span>
<span data-ttu-id="3ff94-126">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3ff94-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3ff94-127">-Descrição</span><span class="sxs-lookup"><span data-stu-id="3ff94-127">-Description</span></span>
<span data-ttu-id="3ff94-128">Descrição da restrição de acesso.</span><span class="sxs-lookup"><span data-stu-id="3ff94-128">Access Restriction description.</span></span>

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

### <span data-ttu-id="3ff94-129">-HttpHeader</span><span class="sxs-lookup"><span data-stu-id="3ff94-129">-HttpHeader</span></span>
<span data-ttu-id="3ff94-130">Restrições de cabeçalho http.</span><span class="sxs-lookup"><span data-stu-id="3ff94-130">Http header restrictions.</span></span> <span data-ttu-id="3ff94-131">Exemplo:-HttpHeader @ {' x-Azure-fdid ' = ' 7acacb02-47EA-4cd4-b568-5e880e72582e '; ' x-Forwarded-host ' = ' www.contoso.com ', ' app.contoso.com '}</span><span class="sxs-lookup"><span data-stu-id="3ff94-131">Example: -HttpHeader @{'x-azure-fdid' = '7acacb02-47ea-4cd4-b568-5e880e72582e'; 'x-forwarded-host' = 'www.contoso.com', 'app.contoso.com'}</span></span>

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

### <span data-ttu-id="3ff94-132">-IgnoreMissingServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="3ff94-132">-IgnoreMissingServiceEndpoint</span></span>
<span data-ttu-id="3ff94-133">Especifique se o registro de ponto de extremidade do serviço na sub-rede deve ser validado.</span><span class="sxs-lookup"><span data-stu-id="3ff94-133">Specify if Service Endpoint registration at Subnet should be validated.</span></span>

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

### <span data-ttu-id="3ff94-134">-IpAddress</span><span class="sxs-lookup"><span data-stu-id="3ff94-134">-IpAddress</span></span>
<span data-ttu-id="3ff94-135">Intervalo CIDR de endereços IP V4 ou v6.</span><span class="sxs-lookup"><span data-stu-id="3ff94-135">Ip Address v4 or v6 CIDR range.</span></span> <span data-ttu-id="3ff94-136">Por exemplo: 192.168.0.0/24</span><span class="sxs-lookup"><span data-stu-id="3ff94-136">E.g.: 192.168.0.0/24</span></span>

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

### <span data-ttu-id="3ff94-137">-Nome</span><span class="sxs-lookup"><span data-stu-id="3ff94-137">-Name</span></span>
<span data-ttu-id="3ff94-138">Nome da regra</span><span class="sxs-lookup"><span data-stu-id="3ff94-138">Rule Name</span></span>

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

### <span data-ttu-id="3ff94-139">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3ff94-139">-PassThru</span></span>
<span data-ttu-id="3ff94-140">Retorne o objeto de configuração de restrição de acesso.</span><span class="sxs-lookup"><span data-stu-id="3ff94-140">Return the access restriction config object.</span></span>

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

### <span data-ttu-id="3ff94-141">-Priority</span><span class="sxs-lookup"><span data-stu-id="3ff94-141">-Priority</span></span>
<span data-ttu-id="3ff94-142">Prioridade de restrição de acesso.</span><span class="sxs-lookup"><span data-stu-id="3ff94-142">Access Restriction priority.</span></span> <span data-ttu-id="3ff94-143">Por exemplo: 500.</span><span class="sxs-lookup"><span data-stu-id="3ff94-143">E.g.: 500.</span></span>

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

### <span data-ttu-id="3ff94-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3ff94-144">-ResourceGroupName</span></span>
<span data-ttu-id="3ff94-145">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="3ff94-145">Resource Group Name</span></span>

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

### <span data-ttu-id="3ff94-146">-ServiceTag</span><span class="sxs-lookup"><span data-stu-id="3ff94-146">-ServiceTag</span></span>
<span data-ttu-id="3ff94-147">Nome da etiqueta de serviço</span><span class="sxs-lookup"><span data-stu-id="3ff94-147">Name of Service Tag</span></span>

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

### <span data-ttu-id="3ff94-148">-Slotname</span><span class="sxs-lookup"><span data-stu-id="3ff94-148">-SlotName</span></span>
<span data-ttu-id="3ff94-149">Nome do slot de implantação.</span><span class="sxs-lookup"><span data-stu-id="3ff94-149">Deployment Slot name.</span></span>

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

### <span data-ttu-id="3ff94-150">-Subnetid</span><span class="sxs-lookup"><span data-stu-id="3ff94-150">-SubnetId</span></span>
<span data-ttu-id="3ff94-151">ResourceId da sub-rede.</span><span class="sxs-lookup"><span data-stu-id="3ff94-151">ResourceId of Subnet.</span></span>

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

### <span data-ttu-id="3ff94-152">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="3ff94-152">-SubnetName</span></span>
<span data-ttu-id="3ff94-153">Nome da sub-rede.</span><span class="sxs-lookup"><span data-stu-id="3ff94-153">Name of Subnet.</span></span>

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

### <span data-ttu-id="3ff94-154">-TargetScmSite</span><span class="sxs-lookup"><span data-stu-id="3ff94-154">-TargetScmSite</span></span>
<span data-ttu-id="3ff94-155">A regra é direcionada para o site principal ou o site do SCM.</span><span class="sxs-lookup"><span data-stu-id="3ff94-155">Rule is aimed for Main site or Scm site.</span></span>

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

### <span data-ttu-id="3ff94-156">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="3ff94-156">-VirtualNetworkName</span></span>
<span data-ttu-id="3ff94-157">Nome da rede virtual.</span><span class="sxs-lookup"><span data-stu-id="3ff94-157">Name of Virtual Network.</span></span>

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

### <span data-ttu-id="3ff94-158">-WebAppname</span><span class="sxs-lookup"><span data-stu-id="3ff94-158">-WebAppName</span></span>
<span data-ttu-id="3ff94-159">O nome do aplicativo Web.</span><span class="sxs-lookup"><span data-stu-id="3ff94-159">The name of the web app.</span></span>

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

### <span data-ttu-id="3ff94-160">-Confirme</span><span class="sxs-lookup"><span data-stu-id="3ff94-160">-Confirm</span></span>
<span data-ttu-id="3ff94-161">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3ff94-161">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3ff94-162">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3ff94-162">-WhatIf</span></span>
<span data-ttu-id="3ff94-163">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="3ff94-163">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3ff94-164">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="3ff94-164">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3ff94-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ff94-165">CommonParameters</span></span>
<span data-ttu-id="3ff94-166">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3ff94-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ff94-167">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3ff94-167">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ff94-168">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3ff94-168">INPUTS</span></span>

### <span data-ttu-id="3ff94-169">System. String</span><span class="sxs-lookup"><span data-stu-id="3ff94-169">System.String</span></span>

## <span data-ttu-id="3ff94-170">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3ff94-170">OUTPUTS</span></span>

### <span data-ttu-id="3ff94-171">Microsoft. Azure. Commands. webapps. Models. PSAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="3ff94-171">Microsoft.Azure.Commands.WebApps.Models.PSAccessRestrictionConfig</span></span>

## <span data-ttu-id="3ff94-172">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3ff94-172">NOTES</span></span>

## <span data-ttu-id="3ff94-173">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3ff94-173">RELATED LINKS</span></span>

[<span data-ttu-id="3ff94-174">Update-AzWebAppAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="3ff94-174">Update-AzWebAppAccessRestrictionConfig</span></span>](./Update-AzWebAppAccessRestrictionConfig.md)

[<span data-ttu-id="3ff94-175">Get-AzWebAppAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="3ff94-175">Get-AzWebAppAccessRestrictionConfig</span></span>](./Get-AzWebAppAccessRestrictionConfig.md)

[<span data-ttu-id="3ff94-176">Remove-AzWebAppAccessRestrictionRule</span><span class="sxs-lookup"><span data-stu-id="3ff94-176">Remove-AzWebAppAccessRestrictionRule</span></span>](./Remove-AzWebAppAccessRestrictionRule.md)
