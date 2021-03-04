---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppAccessRestrictionRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppAccessRestrictionRule.md
ms.openlocfilehash: a7ff5c406cea050f809ef9ffa1e2d9974903fdc2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891068"
---
# <span data-ttu-id="ad1dd-101">Remove-AzWebAppAccessRestrictionRule</span><span class="sxs-lookup"><span data-stu-id="ad1dd-101">Remove-AzWebAppAccessRestrictionRule</span></span>

## <span data-ttu-id="ad1dd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ad1dd-102">SYNOPSIS</span></span>
<span data-ttu-id="ad1dd-103">Remove uma regra de Restrição de Acesso de um Aplicativo Web do Azure.</span><span class="sxs-lookup"><span data-stu-id="ad1dd-103">Removes an Access Restriction rule from an Azure Web App.</span></span>

## <span data-ttu-id="ad1dd-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="ad1dd-104">SYNTAX</span></span>

```
Remove-AzWebAppAccessRestrictionRule [-ResourceGroupName] <String> [-WebAppName] <String> [-Name <String>]
 [-Action <String>] [-SlotName <String>] [-TargetScmSite] [-IpAddress <String>] [-SubnetName <String>]
 [-VirtualNetworkName <String>] [-SubnetId <String>] [-ServiceTag <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ad1dd-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="ad1dd-105">DESCRIPTION</span></span>
<span data-ttu-id="ad1dd-106">O cmdlet **Remove-AzWebAppAccessRestrictionRule** remove uma regra de Restrição de Acesso de um Aplicativo Web do Azure</span><span class="sxs-lookup"><span data-stu-id="ad1dd-106">The **Remove-AzWebAppAccessRestrictionRule** cmdlet removes an Access Restriction rule from an Azure Web App</span></span>

## <span data-ttu-id="ad1dd-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ad1dd-107">EXAMPLES</span></span>

### <span data-ttu-id="ad1dd-108">Exemplo 1: Remover uma regra de restrição de acesso a aplicativo web</span><span class="sxs-lookup"><span data-stu-id="ad1dd-108">Example 1: Remove a Web App Access Restriction Rule</span></span>
```
PS C:\>Remove-AzWebAppAccessRestrictionRule -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite" -Name IpRule
```

<span data-ttu-id="ad1dd-109">Este comando remove a regra de restrição de acesso IpRule do Azure Web App chamada ContosoSite que pertence ao grupo de recursos chamado Default-Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="ad1dd-109">This command removes the IpRule access restriction rule from Azure Web App named ContosoSite that belongs to the resource group named Default-Web-WestUS.</span></span>

### <span data-ttu-id="ad1dd-110">Exemplo 2: Remover uma regra de restrição de acesso a aplicativo web de marca de serviço</span><span class="sxs-lookup"><span data-stu-id="ad1dd-110">Example 2: Remove a Service Tag Web App Access Restriction Rule</span></span>
```
PS C:\>Remove-AzWebAppAccessRestrictionRule -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite" -ServiceTag AzureFrontDoor.Backend
```

<span data-ttu-id="ad1dd-111">Este comando remove a regra de restrição de acesso com ServiceTag igual a AzureFrontDoor.Backend do Azure Web App chamado ContosoSite que pertence ao grupo de recursos chamado Default-Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="ad1dd-111">This command removes the access restriction rule with ServiceTag equals AzureFrontDoor.Backend from Azure Web App named ContosoSite that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="ad1dd-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="ad1dd-112">PARAMETERS</span></span>

### <span data-ttu-id="ad1dd-113">-Action</span><span class="sxs-lookup"><span data-stu-id="ad1dd-113">-Action</span></span>
<span data-ttu-id="ad1dd-114">Regra Permitir ou Negar.</span><span class="sxs-lookup"><span data-stu-id="ad1dd-114">Allow or Deny rule.</span></span>

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

### <span data-ttu-id="ad1dd-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad1dd-115">-DefaultProfile</span></span>
<span data-ttu-id="ad1dd-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="ad1dd-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ad1dd-117">-IpAddress</span><span class="sxs-lookup"><span data-stu-id="ad1dd-117">-IpAddress</span></span>
<span data-ttu-id="ad1dd-118">Intervalo de CIDR do Endereço Ip v4 ou v6.</span><span class="sxs-lookup"><span data-stu-id="ad1dd-118">Ip Address v4 or v6 CIDR range.</span></span> <span data-ttu-id="ad1dd-119">Por exemplo: 192.168.0.0/24</span><span class="sxs-lookup"><span data-stu-id="ad1dd-119">E.g.: 192.168.0.0/24</span></span>

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

### <span data-ttu-id="ad1dd-120">-Name</span><span class="sxs-lookup"><span data-stu-id="ad1dd-120">-Name</span></span>
<span data-ttu-id="ad1dd-121">Nome da regra de restrição de acesso</span><span class="sxs-lookup"><span data-stu-id="ad1dd-121">Access Restriction Rule Name</span></span>

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

### <span data-ttu-id="ad1dd-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ad1dd-122">-PassThru</span></span>
<span data-ttu-id="ad1dd-123">Retorne o objeto config de restrição de acesso.</span><span class="sxs-lookup"><span data-stu-id="ad1dd-123">Return the access restriction config object.</span></span>

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

### <span data-ttu-id="ad1dd-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ad1dd-124">-ResourceGroupName</span></span>
<span data-ttu-id="ad1dd-125">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="ad1dd-125">Resource Group Name</span></span>

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

### <span data-ttu-id="ad1dd-126">-ServiceTag</span><span class="sxs-lookup"><span data-stu-id="ad1dd-126">-ServiceTag</span></span>
<span data-ttu-id="ad1dd-127">Nome da marca de serviço</span><span class="sxs-lookup"><span data-stu-id="ad1dd-127">Name of Service Tag</span></span>

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

### <span data-ttu-id="ad1dd-128">-SlotName</span><span class="sxs-lookup"><span data-stu-id="ad1dd-128">-SlotName</span></span>
<span data-ttu-id="ad1dd-129">Nome do slot de implantação.</span><span class="sxs-lookup"><span data-stu-id="ad1dd-129">Deployment Slot Name.</span></span>

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

### <span data-ttu-id="ad1dd-130">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="ad1dd-130">-SubnetId</span></span>
<span data-ttu-id="ad1dd-131">ResourceId da Sub-rede.</span><span class="sxs-lookup"><span data-stu-id="ad1dd-131">ResourceId of Subnet.</span></span>

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

### <span data-ttu-id="ad1dd-132">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="ad1dd-132">-SubnetName</span></span>
<span data-ttu-id="ad1dd-133">Nome da Sub-rede.</span><span class="sxs-lookup"><span data-stu-id="ad1dd-133">Name of Subnet.</span></span>

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

### <span data-ttu-id="ad1dd-134">-TargetScmSite</span><span class="sxs-lookup"><span data-stu-id="ad1dd-134">-TargetScmSite</span></span>
<span data-ttu-id="ad1dd-135">A regra destina-se ao site principal ou ao site Scm.</span><span class="sxs-lookup"><span data-stu-id="ad1dd-135">Rule is aimed for Main site or Scm site.</span></span>

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

### <span data-ttu-id="ad1dd-136">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="ad1dd-136">-VirtualNetworkName</span></span>
<span data-ttu-id="ad1dd-137">Nome da Rede Virtual (deve estar no mesmo grupo de recursos que o Web App).</span><span class="sxs-lookup"><span data-stu-id="ad1dd-137">Name of Virtual Network (must be in same resource group as Web App).</span></span>

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

### <span data-ttu-id="ad1dd-138">-WebAppName</span><span class="sxs-lookup"><span data-stu-id="ad1dd-138">-WebAppName</span></span>
<span data-ttu-id="ad1dd-139">O nome do aplicativo Web.</span><span class="sxs-lookup"><span data-stu-id="ad1dd-139">The name of the web app.</span></span>

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

### <span data-ttu-id="ad1dd-140">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ad1dd-140">-Confirm</span></span>
<span data-ttu-id="ad1dd-141">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ad1dd-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ad1dd-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ad1dd-142">-WhatIf</span></span>
<span data-ttu-id="ad1dd-143">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="ad1dd-143">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ad1dd-144">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ad1dd-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ad1dd-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad1dd-145">CommonParameters</span></span>
<span data-ttu-id="ad1dd-146">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ad1dd-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad1dd-147">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ad1dd-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad1dd-148">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ad1dd-148">INPUTS</span></span>

### <span data-ttu-id="ad1dd-149">System.String</span><span class="sxs-lookup"><span data-stu-id="ad1dd-149">System.String</span></span>

## <span data-ttu-id="ad1dd-150">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="ad1dd-150">OUTPUTS</span></span>

### <span data-ttu-id="ad1dd-151">Microsoft.Azure.Commands.WebApps.Models.PSAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="ad1dd-151">Microsoft.Azure.Commands.WebApps.Models.PSAccessRestrictionConfig</span></span>

## <span data-ttu-id="ad1dd-152">NOTES</span><span class="sxs-lookup"><span data-stu-id="ad1dd-152">NOTES</span></span>

## <span data-ttu-id="ad1dd-153">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ad1dd-153">RELATED LINKS</span></span>

[<span data-ttu-id="ad1dd-154">Get-AzWebAppAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="ad1dd-154">Get-AzWebAppAccessRestrictionConfig</span></span>](./Get-AzWebAppAccessRestrictionConfig.md)

[<span data-ttu-id="ad1dd-155">Update-AzWebAppAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="ad1dd-155">Update-AzWebAppAccessRestrictionConfig</span></span>](./Update-AzWebAppAccessRestrictionConfig.md)

[<span data-ttu-id="ad1dd-156">Add-AzWebAppAccessRestrictionRule</span><span class="sxs-lookup"><span data-stu-id="ad1dd-156">Add-AzWebAppAccessRestrictionRule</span></span>](./Add-AzWebAppAccessRestrictionRule.md)
