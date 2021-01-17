---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppAccessRestrictionRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppAccessRestrictionRule.md
ms.openlocfilehash: a7ff5c406cea050f809ef9ffa1e2d9974903fdc2
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98427796"
---
# <span data-ttu-id="e20d9-101">Remove-AzWebAppAccessRestrictionRule</span><span class="sxs-lookup"><span data-stu-id="e20d9-101">Remove-AzWebAppAccessRestrictionRule</span></span>

## <span data-ttu-id="e20d9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e20d9-102">SYNOPSIS</span></span>
<span data-ttu-id="e20d9-103">Remove uma regra de restrição de acesso de um aplicativo Web do Azure.</span><span class="sxs-lookup"><span data-stu-id="e20d9-103">Removes an Access Restriction rule from an Azure Web App.</span></span>

## <span data-ttu-id="e20d9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e20d9-104">SYNTAX</span></span>

```
Remove-AzWebAppAccessRestrictionRule [-ResourceGroupName] <String> [-WebAppName] <String> [-Name <String>]
 [-Action <String>] [-SlotName <String>] [-TargetScmSite] [-IpAddress <String>] [-SubnetName <String>]
 [-VirtualNetworkName <String>] [-SubnetId <String>] [-ServiceTag <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e20d9-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e20d9-105">DESCRIPTION</span></span>
<span data-ttu-id="e20d9-106">O cmdlet **Remove-AzWebAppAccessRestrictionRule** remove uma regra de restrição de acesso de um aplicativo Web do Azure</span><span class="sxs-lookup"><span data-stu-id="e20d9-106">The **Remove-AzWebAppAccessRestrictionRule** cmdlet removes an Access Restriction rule from an Azure Web App</span></span>

## <span data-ttu-id="e20d9-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e20d9-107">EXAMPLES</span></span>

### <span data-ttu-id="e20d9-108">Exemplo 1: remover uma regra de restrição de acesso do aplicativo Web</span><span class="sxs-lookup"><span data-stu-id="e20d9-108">Example 1: Remove a Web App Access Restriction Rule</span></span>
```
PS C:\>Remove-AzWebAppAccessRestrictionRule -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite" -Name IpRule
```

<span data-ttu-id="e20d9-109">Esse comando Remove a regra de restrição de acesso IpRule do Azure Web App chamado ContosoSite que pertence ao grupo de recursos chamado Default-Web-Oesteus.</span><span class="sxs-lookup"><span data-stu-id="e20d9-109">This command removes the IpRule access restriction rule from Azure Web App named ContosoSite that belongs to the resource group named Default-Web-WestUS.</span></span>

### <span data-ttu-id="e20d9-110">Exemplo 2: remover uma regra de restrição de acesso ao aplicativo Web de marca de serviço</span><span class="sxs-lookup"><span data-stu-id="e20d9-110">Example 2: Remove a Service Tag Web App Access Restriction Rule</span></span>
```
PS C:\>Remove-AzWebAppAccessRestrictionRule -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite" -ServiceTag AzureFrontDoor.Backend
```

<span data-ttu-id="e20d9-111">Esse comando Remove a regra de restrição de acesso com ServiceTag igual a AzureFrontDoor. back-end do Azure Web App chamado ContosoSite que pertence ao grupo de recursos chamado Default-Web-Oesteus.</span><span class="sxs-lookup"><span data-stu-id="e20d9-111">This command removes the access restriction rule with ServiceTag equals AzureFrontDoor.Backend from Azure Web App named ContosoSite that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="e20d9-112">OS</span><span class="sxs-lookup"><span data-stu-id="e20d9-112">PARAMETERS</span></span>

### <span data-ttu-id="e20d9-113">-Ação</span><span class="sxs-lookup"><span data-stu-id="e20d9-113">-Action</span></span>
<span data-ttu-id="e20d9-114">Regra de permissão ou negação.</span><span class="sxs-lookup"><span data-stu-id="e20d9-114">Allow or Deny rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Allow, Deny

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e20d9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e20d9-115">-DefaultProfile</span></span>
<span data-ttu-id="e20d9-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e20d9-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e20d9-117">-IpAddress</span><span class="sxs-lookup"><span data-stu-id="e20d9-117">-IpAddress</span></span>
<span data-ttu-id="e20d9-118">Intervalo CIDR de endereços IP V4 ou v6.</span><span class="sxs-lookup"><span data-stu-id="e20d9-118">Ip Address v4 or v6 CIDR range.</span></span> <span data-ttu-id="e20d9-119">Por exemplo: 192.168.0.0/24</span><span class="sxs-lookup"><span data-stu-id="e20d9-119">E.g.: 192.168.0.0/24</span></span>

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

### <span data-ttu-id="e20d9-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="e20d9-120">-Name</span></span>
<span data-ttu-id="e20d9-121">Nome da regra de restrição de acesso</span><span class="sxs-lookup"><span data-stu-id="e20d9-121">Access Restriction Rule Name</span></span>

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

### <span data-ttu-id="e20d9-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e20d9-122">-PassThru</span></span>
<span data-ttu-id="e20d9-123">Retorne o objeto de configuração de restrição de acesso.</span><span class="sxs-lookup"><span data-stu-id="e20d9-123">Return the access restriction config object.</span></span>

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

### <span data-ttu-id="e20d9-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e20d9-124">-ResourceGroupName</span></span>
<span data-ttu-id="e20d9-125">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="e20d9-125">Resource Group Name</span></span>

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

### <span data-ttu-id="e20d9-126">-ServiceTag</span><span class="sxs-lookup"><span data-stu-id="e20d9-126">-ServiceTag</span></span>
<span data-ttu-id="e20d9-127">Nome da etiqueta de serviço</span><span class="sxs-lookup"><span data-stu-id="e20d9-127">Name of Service Tag</span></span>

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

### <span data-ttu-id="e20d9-128">-Slotname</span><span class="sxs-lookup"><span data-stu-id="e20d9-128">-SlotName</span></span>
<span data-ttu-id="e20d9-129">Nome do slot de implantação.</span><span class="sxs-lookup"><span data-stu-id="e20d9-129">Deployment Slot Name.</span></span>

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

### <span data-ttu-id="e20d9-130">-Subnetid</span><span class="sxs-lookup"><span data-stu-id="e20d9-130">-SubnetId</span></span>
<span data-ttu-id="e20d9-131">ResourceId da sub-rede.</span><span class="sxs-lookup"><span data-stu-id="e20d9-131">ResourceId of Subnet.</span></span>

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

### <span data-ttu-id="e20d9-132">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="e20d9-132">-SubnetName</span></span>
<span data-ttu-id="e20d9-133">Nome da sub-rede.</span><span class="sxs-lookup"><span data-stu-id="e20d9-133">Name of Subnet.</span></span>

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

### <span data-ttu-id="e20d9-134">-TargetScmSite</span><span class="sxs-lookup"><span data-stu-id="e20d9-134">-TargetScmSite</span></span>
<span data-ttu-id="e20d9-135">A regra é direcionada para o site principal ou o site do SCM.</span><span class="sxs-lookup"><span data-stu-id="e20d9-135">Rule is aimed for Main site or Scm site.</span></span>

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

### <span data-ttu-id="e20d9-136">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="e20d9-136">-VirtualNetworkName</span></span>
<span data-ttu-id="e20d9-137">Nome da rede virtual (deve estar no mesmo grupo de recursos do aplicativo Web).</span><span class="sxs-lookup"><span data-stu-id="e20d9-137">Name of Virtual Network (must be in same resource group as Web App).</span></span>

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

### <span data-ttu-id="e20d9-138">-WebAppname</span><span class="sxs-lookup"><span data-stu-id="e20d9-138">-WebAppName</span></span>
<span data-ttu-id="e20d9-139">O nome do aplicativo Web.</span><span class="sxs-lookup"><span data-stu-id="e20d9-139">The name of the web app.</span></span>

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

### <span data-ttu-id="e20d9-140">-Confirme</span><span class="sxs-lookup"><span data-stu-id="e20d9-140">-Confirm</span></span>
<span data-ttu-id="e20d9-141">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e20d9-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e20d9-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e20d9-142">-WhatIf</span></span>
<span data-ttu-id="e20d9-143">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e20d9-143">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e20d9-144">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e20d9-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e20d9-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e20d9-145">CommonParameters</span></span>
<span data-ttu-id="e20d9-146">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e20d9-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e20d9-147">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e20d9-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e20d9-148">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e20d9-148">INPUTS</span></span>

### <span data-ttu-id="e20d9-149">System. String</span><span class="sxs-lookup"><span data-stu-id="e20d9-149">System.String</span></span>

## <span data-ttu-id="e20d9-150">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e20d9-150">OUTPUTS</span></span>

### <span data-ttu-id="e20d9-151">Microsoft. Azure. Commands. webapps. Models. PSAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="e20d9-151">Microsoft.Azure.Commands.WebApps.Models.PSAccessRestrictionConfig</span></span>

## <span data-ttu-id="e20d9-152">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e20d9-152">NOTES</span></span>

## <span data-ttu-id="e20d9-153">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e20d9-153">RELATED LINKS</span></span>

[<span data-ttu-id="e20d9-154">Get-AzWebAppAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="e20d9-154">Get-AzWebAppAccessRestrictionConfig</span></span>](./Get-AzWebAppAccessRestrictionConfig.md)

[<span data-ttu-id="e20d9-155">Update-AzWebAppAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="e20d9-155">Update-AzWebAppAccessRestrictionConfig</span></span>](./Update-AzWebAppAccessRestrictionConfig.md)

[<span data-ttu-id="e20d9-156">Add-AzWebAppAccessRestrictionRule</span><span class="sxs-lookup"><span data-stu-id="e20d9-156">Add-AzWebAppAccessRestrictionRule</span></span>](./Add-AzWebAppAccessRestrictionRule.md)
