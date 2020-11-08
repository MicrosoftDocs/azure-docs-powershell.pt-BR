---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Add-AzWebAppAccessRestrictionRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Add-AzWebAppAccessRestrictionRule.md
ms.openlocfilehash: 0abad2b3d38a5f614222a8eda7e3c27b9fda9556
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94116494"
---
# <span data-ttu-id="44c0e-101">Add-AzWebAppAccessRestrictionRule</span><span class="sxs-lookup"><span data-stu-id="44c0e-101">Add-AzWebAppAccessRestrictionRule</span></span>

## <span data-ttu-id="44c0e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="44c0e-102">SYNOPSIS</span></span>
<span data-ttu-id="44c0e-103">Adiciona uma regra de restiction do Access a um aplicativo Web do Azure.</span><span class="sxs-lookup"><span data-stu-id="44c0e-103">Adds an Access Restiction rule to an Azure Web App.</span></span>

## <span data-ttu-id="44c0e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="44c0e-104">SYNTAX</span></span>

### <span data-ttu-id="44c0e-105">IpAddressParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="44c0e-105">IpAddressParameterSet (Default)</span></span>
```
Add-AzWebAppAccessRestrictionRule [-ResourceGroupName] <String> [-WebAppName] <String> [-Name <String>]
 [-Description <String>] -Priority <UInt32> [-Action <String>] [-SlotName <String>] [-TargetScmSite]
 -IpAddress <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="44c0e-106">SubnetNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="44c0e-106">SubnetNameParameterSet</span></span>
```
Add-AzWebAppAccessRestrictionRule [-ResourceGroupName] <String> [-WebAppName] <String> [-Name <String>]
 [-Description <String>] -Priority <UInt32> [-Action <String>] [-SlotName <String>] [-TargetScmSite]
 -SubnetName <String> -VirtualNetworkName <String> [-IgnoreMissingServiceEndpoint] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="44c0e-107">SubnetIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="44c0e-107">SubnetIdParameterSet</span></span>
```
Add-AzWebAppAccessRestrictionRule [-ResourceGroupName] <String> [-WebAppName] <String> [-Name <String>]
 [-Description <String>] -Priority <UInt32> [-Action <String>] [-SlotName <String>] [-TargetScmSite]
 -SubnetId <String> [-IgnoreMissingServiceEndpoint] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="44c0e-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="44c0e-108">DESCRIPTION</span></span>
<span data-ttu-id="44c0e-109">O cmdlet **Add-AzWebAppAccessRestrictionRule** adiciona uma regra de restrição de acesso a um aplicativo Web do Azure.</span><span class="sxs-lookup"><span data-stu-id="44c0e-109">The **Add-AzWebAppAccessRestrictionRule** cmdlet adds an Access Restriction rule to an Azure Web App.</span></span>

## <span data-ttu-id="44c0e-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="44c0e-110">EXAMPLES</span></span>

### <span data-ttu-id="44c0e-111">Exemplo 1: Adicionar regra de restrição de acesso IpAddress a um aplicativo Web</span><span class="sxs-lookup"><span data-stu-id="44c0e-111">Example 1: Add IpAddress Access Restriction rule to a Web App</span></span>
```
PS C:\>Add-AzWebAppAccessRestrictionRule -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite" 
-Name IpRule -Priority 200 -Action Allow -IpAddress 10.10.0.0/8
```

<span data-ttu-id="44c0e-112">Esse comando adiciona uma regra de restrição de acesso com Priority 200 e intervalo de IP a um aplicativo Web chamado ContosoSite que pertence ao grupo de recursos-Web-Westus padrão.</span><span class="sxs-lookup"><span data-stu-id="44c0e-112">This command adds an access restriction rule with priority 200 and ip range to a Web App named ContosoSite that belongs to the resource group Default-Web-WestUS.</span></span>

### <span data-ttu-id="44c0e-113">Exemplo 2: Adicionar regra de restrição de acesso de ponto de extremidade do serviço de sub-rede a um aplicativo Web</span><span class="sxs-lookup"><span data-stu-id="44c0e-113">Example 2: Add Subnet Service Endpoint Access Restriction rule to a Web App</span></span>
```
PS C:\>Add-AzWebAppAccessRestrictionRule -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite" 
-Name SubnetRule -Priority 300 -Action Allow -SubnetName appgw-subnet -VirtualNetworkName corp-vnet
```

<span data-ttu-id="44c0e-114">Esse comando adiciona uma regra de restrição de acesso com prioridade 300 e com o subnet appgw-subnet em Corp-vnet a um aplicativo Web chamado ContosoSite que pertence à parte padrão do grupo de recursos-Oesteus.</span><span class="sxs-lookup"><span data-stu-id="44c0e-114">This command adds an access restriction rule with priority 300 and with subnet appgw-subnet in corp-vnet to a Web App named ContosoSite that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="44c0e-115">OS</span><span class="sxs-lookup"><span data-stu-id="44c0e-115">PARAMETERS</span></span>

### <span data-ttu-id="44c0e-116">-Ação</span><span class="sxs-lookup"><span data-stu-id="44c0e-116">-Action</span></span>
<span data-ttu-id="44c0e-117">Regra de permissão ou negação.</span><span class="sxs-lookup"><span data-stu-id="44c0e-117">Allow or Deny rule.</span></span>

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

### <span data-ttu-id="44c0e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44c0e-118">-DefaultProfile</span></span>
<span data-ttu-id="44c0e-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="44c0e-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="44c0e-120">-Descrição</span><span class="sxs-lookup"><span data-stu-id="44c0e-120">-Description</span></span>
<span data-ttu-id="44c0e-121">Descrição da restrição de acesso.</span><span class="sxs-lookup"><span data-stu-id="44c0e-121">Access Restriction description.</span></span>

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

### <span data-ttu-id="44c0e-122">-IgnoreMissingServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="44c0e-122">-IgnoreMissingServiceEndpoint</span></span>
<span data-ttu-id="44c0e-123">Especifique se o registro de ponto de extremidade do serviço na sub-rede deve ser validado.</span><span class="sxs-lookup"><span data-stu-id="44c0e-123">Specify if Service Endpoint registration at Subnet should be validated.</span></span>

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

### <span data-ttu-id="44c0e-124">-IpAddress</span><span class="sxs-lookup"><span data-stu-id="44c0e-124">-IpAddress</span></span>
<span data-ttu-id="44c0e-125">Intervalo CIDR de endereços IP V4 ou v6.</span><span class="sxs-lookup"><span data-stu-id="44c0e-125">Ip Address v4 or v6 CIDR range.</span></span> <span data-ttu-id="44c0e-126">Por exemplo: 192.168.0.0/24</span><span class="sxs-lookup"><span data-stu-id="44c0e-126">E.g.: 192.168.0.0/24</span></span>

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

### <span data-ttu-id="44c0e-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="44c0e-127">-Name</span></span>
<span data-ttu-id="44c0e-128">Nome da regra</span><span class="sxs-lookup"><span data-stu-id="44c0e-128">Rule Name</span></span>

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

### <span data-ttu-id="44c0e-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="44c0e-129">-PassThru</span></span>
<span data-ttu-id="44c0e-130">Retorne o objeto de configuração de restrição de acesso.</span><span class="sxs-lookup"><span data-stu-id="44c0e-130">Return the access restriction config object.</span></span>

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

### <span data-ttu-id="44c0e-131">-Priority</span><span class="sxs-lookup"><span data-stu-id="44c0e-131">-Priority</span></span>
<span data-ttu-id="44c0e-132">Prioridade de restrição de acesso.</span><span class="sxs-lookup"><span data-stu-id="44c0e-132">Access Restriction priority.</span></span> <span data-ttu-id="44c0e-133">Por exemplo: 500.</span><span class="sxs-lookup"><span data-stu-id="44c0e-133">E.g.: 500.</span></span>

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

### <span data-ttu-id="44c0e-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="44c0e-134">-ResourceGroupName</span></span>
<span data-ttu-id="44c0e-135">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="44c0e-135">Resource Group Name</span></span>

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

### <span data-ttu-id="44c0e-136">-Slotname</span><span class="sxs-lookup"><span data-stu-id="44c0e-136">-SlotName</span></span>
<span data-ttu-id="44c0e-137">Nome do slot de implantação.</span><span class="sxs-lookup"><span data-stu-id="44c0e-137">Deployment Slot name.</span></span>

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

### <span data-ttu-id="44c0e-138">-Subnetid</span><span class="sxs-lookup"><span data-stu-id="44c0e-138">-SubnetId</span></span>
<span data-ttu-id="44c0e-139">ResourceId da sub-rede.</span><span class="sxs-lookup"><span data-stu-id="44c0e-139">ResourceId of Subnet.</span></span>

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

### <span data-ttu-id="44c0e-140">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="44c0e-140">-SubnetName</span></span>
<span data-ttu-id="44c0e-141">Nome da sub-rede.</span><span class="sxs-lookup"><span data-stu-id="44c0e-141">Name of Subnet.</span></span>

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

### <span data-ttu-id="44c0e-142">-TargetScmSite</span><span class="sxs-lookup"><span data-stu-id="44c0e-142">-TargetScmSite</span></span>
<span data-ttu-id="44c0e-143">A regra é direcionada para o site principal ou o site do SCM.</span><span class="sxs-lookup"><span data-stu-id="44c0e-143">Rule is aimed for Main site or Scm site.</span></span>

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

### <span data-ttu-id="44c0e-144">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="44c0e-144">-VirtualNetworkName</span></span>
<span data-ttu-id="44c0e-145">Nome da rede virtual.</span><span class="sxs-lookup"><span data-stu-id="44c0e-145">Name of Virtual Network.</span></span>

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

### <span data-ttu-id="44c0e-146">-WebAppname</span><span class="sxs-lookup"><span data-stu-id="44c0e-146">-WebAppName</span></span>
<span data-ttu-id="44c0e-147">O nome do aplicativo Web.</span><span class="sxs-lookup"><span data-stu-id="44c0e-147">The name of the web app.</span></span>

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

### <span data-ttu-id="44c0e-148">-Confirme</span><span class="sxs-lookup"><span data-stu-id="44c0e-148">-Confirm</span></span>
<span data-ttu-id="44c0e-149">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="44c0e-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="44c0e-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="44c0e-150">-WhatIf</span></span>
<span data-ttu-id="44c0e-151">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="44c0e-151">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="44c0e-152">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="44c0e-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="44c0e-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44c0e-153">CommonParameters</span></span>
<span data-ttu-id="44c0e-154">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="44c0e-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44c0e-155">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="44c0e-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44c0e-156">SENSORES</span><span class="sxs-lookup"><span data-stu-id="44c0e-156">INPUTS</span></span>

### <span data-ttu-id="44c0e-157">System. String</span><span class="sxs-lookup"><span data-stu-id="44c0e-157">System.String</span></span>

## <span data-ttu-id="44c0e-158">EXIBE</span><span class="sxs-lookup"><span data-stu-id="44c0e-158">OUTPUTS</span></span>

### <span data-ttu-id="44c0e-159">Microsoft. Azure. Commands. webapps. Models. PSAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="44c0e-159">Microsoft.Azure.Commands.WebApps.Models.PSAccessRestrictionConfig</span></span>

## <span data-ttu-id="44c0e-160">INFORMA</span><span class="sxs-lookup"><span data-stu-id="44c0e-160">NOTES</span></span>

## <span data-ttu-id="44c0e-161">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="44c0e-161">RELATED LINKS</span></span>

[<span data-ttu-id="44c0e-162">Update-AzWebAppAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="44c0e-162">Update-AzWebAppAccessRestrictionConfig</span></span>](./Update-AzWebAppAccessRestrictionConfig.md)

[<span data-ttu-id="44c0e-163">Get-AzWebAppAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="44c0e-163">Get-AzWebAppAccessRestrictionConfig</span></span>](./Get-AzWebAppAccessRestrictionConfig.md)

[<span data-ttu-id="44c0e-164">Remove-AzWebAppAccessRestrictionRule</span><span class="sxs-lookup"><span data-stu-id="44c0e-164">Remove-AzWebAppAccessRestrictionRule</span></span>](./Remove-AzWebAppAccessRestrictionRule.md)
