---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppAccessRestrictionRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppAccessRestrictionRule.md
ms.openlocfilehash: ad0bdc95ea3d582a2f8b6b6b1f8bc772c795352c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93940725"
---
# <span data-ttu-id="bc4e2-101">Remove-AzWebAppAccessRestrictionRule</span><span class="sxs-lookup"><span data-stu-id="bc4e2-101">Remove-AzWebAppAccessRestrictionRule</span></span>

## <span data-ttu-id="bc4e2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="bc4e2-102">SYNOPSIS</span></span>
<span data-ttu-id="bc4e2-103">Remove uma regra de restrição de acesso de um aplicativo Web do Azure.</span><span class="sxs-lookup"><span data-stu-id="bc4e2-103">Removes an Access Restriction rule from an Azure Web App.</span></span>

## <span data-ttu-id="bc4e2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bc4e2-104">SYNTAX</span></span>

```
Remove-AzWebAppAccessRestrictionRule [-ResourceGroupName] <String> [-WebAppName] <String> [-Name <String>]
 [-Action <String>] [-TargetScmSite] [-SlotName <String>] [-IpAddress <String>] [-SubnetName <String>]
 [-VirtualNetworkName <String>] [-SubnetId <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bc4e2-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="bc4e2-105">DESCRIPTION</span></span>
<span data-ttu-id="bc4e2-106">O cmdlet **Remove-AzWebAppAccessRestrictionRule** remove uma regra de restrição de acesso de um aplicativo Web do Azure</span><span class="sxs-lookup"><span data-stu-id="bc4e2-106">The **Remove-AzWebAppAccessRestrictionRule** cmdlet removes an Access Restriction rule from an Azure Web App</span></span>

## <span data-ttu-id="bc4e2-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="bc4e2-107">EXAMPLES</span></span>

### <span data-ttu-id="bc4e2-108">Exemplo 1: remover uma regra de restrição de acesso do aplicativo Web</span><span class="sxs-lookup"><span data-stu-id="bc4e2-108">Example 1: Remove a Web App Access Restriction Rule</span></span>
```
PS C:\>Remove-AzWebAppAccessRestrictionRule -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite" -Name IpRule
```

<span data-ttu-id="bc4e2-109">Esse comando Remove a regra de restrição de acesso IpRule do Azure Web App chamado ContosoSite que pertence ao grupo de recursos chamado Default-Web-Oesteus.</span><span class="sxs-lookup"><span data-stu-id="bc4e2-109">This command removes the IpRule access restriction rule from Azure Web App named ContosoSite that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="bc4e2-110">OS</span><span class="sxs-lookup"><span data-stu-id="bc4e2-110">PARAMETERS</span></span>

### <span data-ttu-id="bc4e2-111">-Ação</span><span class="sxs-lookup"><span data-stu-id="bc4e2-111">-Action</span></span>
<span data-ttu-id="bc4e2-112">Regra de permissão ou negação.</span><span class="sxs-lookup"><span data-stu-id="bc4e2-112">Allow or Deny rule.</span></span>

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

### <span data-ttu-id="bc4e2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc4e2-113">-DefaultProfile</span></span>
<span data-ttu-id="bc4e2-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="bc4e2-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bc4e2-115">-IpAddress</span><span class="sxs-lookup"><span data-stu-id="bc4e2-115">-IpAddress</span></span>
<span data-ttu-id="bc4e2-116">Intervalo CIDR de endereços IP V4 ou v6.</span><span class="sxs-lookup"><span data-stu-id="bc4e2-116">Ip Address v4 or v6 CIDR range.</span></span> <span data-ttu-id="bc4e2-117">Por exemplo: 192.168.0.0/24</span><span class="sxs-lookup"><span data-stu-id="bc4e2-117">E.g.: 192.168.0.0/24</span></span>

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

### <span data-ttu-id="bc4e2-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="bc4e2-118">-Name</span></span>
<span data-ttu-id="bc4e2-119">Nome da regra de restrição de acesso</span><span class="sxs-lookup"><span data-stu-id="bc4e2-119">Access Restriction Rule Name</span></span>

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

### <span data-ttu-id="bc4e2-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bc4e2-120">-PassThru</span></span>
<span data-ttu-id="bc4e2-121">Retorne o objeto de configuração de restrição de acesso.</span><span class="sxs-lookup"><span data-stu-id="bc4e2-121">Return the access restriction config object.</span></span>

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

### <span data-ttu-id="bc4e2-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bc4e2-122">-ResourceGroupName</span></span>
<span data-ttu-id="bc4e2-123">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="bc4e2-123">Resource Group Name</span></span>

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

### <span data-ttu-id="bc4e2-124">-Slotname</span><span class="sxs-lookup"><span data-stu-id="bc4e2-124">-SlotName</span></span>
<span data-ttu-id="bc4e2-125">Nome do slot de implantação.</span><span class="sxs-lookup"><span data-stu-id="bc4e2-125">Deployment Slot Name.</span></span>

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

### <span data-ttu-id="bc4e2-126">-Subnetid</span><span class="sxs-lookup"><span data-stu-id="bc4e2-126">-SubnetId</span></span>
<span data-ttu-id="bc4e2-127">ResourceId da sub-rede.</span><span class="sxs-lookup"><span data-stu-id="bc4e2-127">ResourceId of Subnet.</span></span>

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

### <span data-ttu-id="bc4e2-128">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="bc4e2-128">-SubnetName</span></span>
<span data-ttu-id="bc4e2-129">Nome da sub-rede.</span><span class="sxs-lookup"><span data-stu-id="bc4e2-129">Name of Subnet.</span></span>

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

### <span data-ttu-id="bc4e2-130">-TargetScmSite</span><span class="sxs-lookup"><span data-stu-id="bc4e2-130">-TargetScmSite</span></span>
<span data-ttu-id="bc4e2-131">A regra é direcionada para o site principal ou o site do SCM.</span><span class="sxs-lookup"><span data-stu-id="bc4e2-131">Rule is aimed for Main site or Scm site.</span></span>

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

### <span data-ttu-id="bc4e2-132">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="bc4e2-132">-VirtualNetworkName</span></span>
<span data-ttu-id="bc4e2-133">Nome da rede virtual (deve estar no mesmo grupo de recursos do aplicativo Web).</span><span class="sxs-lookup"><span data-stu-id="bc4e2-133">Name of Virtual Network (must be in same resource group as Web App).</span></span>

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

### <span data-ttu-id="bc4e2-134">-WebAppname</span><span class="sxs-lookup"><span data-stu-id="bc4e2-134">-WebAppName</span></span>
<span data-ttu-id="bc4e2-135">O nome do aplicativo Web.</span><span class="sxs-lookup"><span data-stu-id="bc4e2-135">The name of the web app.</span></span>

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

### <span data-ttu-id="bc4e2-136">-Confirme</span><span class="sxs-lookup"><span data-stu-id="bc4e2-136">-Confirm</span></span>
<span data-ttu-id="bc4e2-137">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bc4e2-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bc4e2-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bc4e2-138">-WhatIf</span></span>
<span data-ttu-id="bc4e2-139">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="bc4e2-139">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="bc4e2-140">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="bc4e2-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bc4e2-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc4e2-141">CommonParameters</span></span>
<span data-ttu-id="bc4e2-142">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bc4e2-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc4e2-143">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bc4e2-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc4e2-144">SENSORES</span><span class="sxs-lookup"><span data-stu-id="bc4e2-144">INPUTS</span></span>

### <span data-ttu-id="bc4e2-145">System. String</span><span class="sxs-lookup"><span data-stu-id="bc4e2-145">System.String</span></span>

## <span data-ttu-id="bc4e2-146">EXIBE</span><span class="sxs-lookup"><span data-stu-id="bc4e2-146">OUTPUTS</span></span>

### <span data-ttu-id="bc4e2-147">Microsoft. Azure. Commands. webapps. Models. PSAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="bc4e2-147">Microsoft.Azure.Commands.WebApps.Models.PSAccessRestrictionConfig</span></span>

## <span data-ttu-id="bc4e2-148">INFORMA</span><span class="sxs-lookup"><span data-stu-id="bc4e2-148">NOTES</span></span>

## <span data-ttu-id="bc4e2-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bc4e2-149">RELATED LINKS</span></span>

[<span data-ttu-id="bc4e2-150">Get-AzWebAppAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="bc4e2-150">Get-AzWebAppAccessRestrictionConfig</span></span>](./Get-AzWebAppAccessRestrictionConfig.md)

[<span data-ttu-id="bc4e2-151">Update-AzWebAppAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="bc4e2-151">Update-AzWebAppAccessRestrictionConfig</span></span>](./Update-AzWebAppAccessRestrictionConfig.md)

[<span data-ttu-id="bc4e2-152">Add-AzWebAppAccessRestrictionRule</span><span class="sxs-lookup"><span data-stu-id="bc4e2-152">Add-AzWebAppAccessRestrictionRule</span></span>](./Add-AzWebAppAccessRestrictionRule.md)
