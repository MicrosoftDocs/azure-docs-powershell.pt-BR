---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppAccessRestrictionRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppAccessRestrictionRule.md
ms.openlocfilehash: a7ff5c406cea050f809ef9ffa1e2d9974903fdc2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116027"
---
# <span data-ttu-id="2fb48-101">Remove-AzWebAppAccessRestrictionRule</span><span class="sxs-lookup"><span data-stu-id="2fb48-101">Remove-AzWebAppAccessRestrictionRule</span></span>

## <span data-ttu-id="2fb48-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2fb48-102">SYNOPSIS</span></span>
<span data-ttu-id="2fb48-103">Remove uma regra de Restrição de Acesso de um Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="2fb48-103">Removes an Access Restriction rule from an Azure Web App.</span></span>

## <span data-ttu-id="2fb48-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2fb48-104">SYNTAX</span></span>

```
Remove-AzWebAppAccessRestrictionRule [-ResourceGroupName] <String> [-WebAppName] <String> [-Name <String>]
 [-Action <String>] [-SlotName <String>] [-TargetScmSite] [-IpAddress <String>] [-SubnetName <String>]
 [-VirtualNetworkName <String>] [-SubnetId <String>] [-ServiceTag <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2fb48-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="2fb48-105">DESCRIPTION</span></span>
<span data-ttu-id="2fb48-106">O cmdlet **Remove-AzWebAppAccessRestrictionRule** remove uma regra de Restrição do Access de um Azure Web App</span><span class="sxs-lookup"><span data-stu-id="2fb48-106">The **Remove-AzWebAppAccessRestrictionRule** cmdlet removes an Access Restriction rule from an Azure Web App</span></span>

## <span data-ttu-id="2fb48-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="2fb48-107">EXAMPLES</span></span>

### <span data-ttu-id="2fb48-108">Exemplo 1: Remover uma Regra de Restrição de Acesso do Aplicativo Web</span><span class="sxs-lookup"><span data-stu-id="2fb48-108">Example 1: Remove a Web App Access Restriction Rule</span></span>
```
PS C:\>Remove-AzWebAppAccessRestrictionRule -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite" -Name IpRule
```

<span data-ttu-id="2fb48-109">Esse comando remove a regra de restrição de acesso IpRule do Azure Web App chamada ContosoSite que pertence ao grupo de recursos chamado Default-Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="2fb48-109">This command removes the IpRule access restriction rule from Azure Web App named ContosoSite that belongs to the resource group named Default-Web-WestUS.</span></span>

### <span data-ttu-id="2fb48-110">Exemplo 2: Remover uma Regra de Restrição de Acesso de Marca de Serviço Web App</span><span class="sxs-lookup"><span data-stu-id="2fb48-110">Example 2: Remove a Service Tag Web App Access Restriction Rule</span></span>
```
PS C:\>Remove-AzWebAppAccessRestrictionRule -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite" -ServiceTag AzureFrontDoor.Backend
```

<span data-ttu-id="2fb48-111">Este comando remove a regra de restrição de acesso com ServiceTag igual a AzureFrontDoor.Backend do Azure Web App chamado ContosoSite que pertence ao grupo de recursos chamado Default-Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="2fb48-111">This command removes the access restriction rule with ServiceTag equals AzureFrontDoor.Backend from Azure Web App named ContosoSite that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="2fb48-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2fb48-112">PARAMETERS</span></span>

### <span data-ttu-id="2fb48-113">-Ação</span><span class="sxs-lookup"><span data-stu-id="2fb48-113">-Action</span></span>
<span data-ttu-id="2fb48-114">Regra Permitir ou Negar.</span><span class="sxs-lookup"><span data-stu-id="2fb48-114">Allow or Deny rule.</span></span>

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

### <span data-ttu-id="2fb48-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2fb48-115">-DefaultProfile</span></span>
<span data-ttu-id="2fb48-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="2fb48-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2fb48-117">-IpAddress</span><span class="sxs-lookup"><span data-stu-id="2fb48-117">-IpAddress</span></span>
<span data-ttu-id="2fb48-118">Ip Address v4 ou v6 CIDR range.</span><span class="sxs-lookup"><span data-stu-id="2fb48-118">Ip Address v4 or v6 CIDR range.</span></span> <span data-ttu-id="2fb48-119">Por exemplo: 192.168.0.0/24</span><span class="sxs-lookup"><span data-stu-id="2fb48-119">E.g.: 192.168.0.0/24</span></span>

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

### <span data-ttu-id="2fb48-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="2fb48-120">-Name</span></span>
<span data-ttu-id="2fb48-121">Nome da regra de restrição de acesso</span><span class="sxs-lookup"><span data-stu-id="2fb48-121">Access Restriction Rule Name</span></span>

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

### <span data-ttu-id="2fb48-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2fb48-122">-PassThru</span></span>
<span data-ttu-id="2fb48-123">Retornar o objeto de configuração de restrição de acesso.</span><span class="sxs-lookup"><span data-stu-id="2fb48-123">Return the access restriction config object.</span></span>

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

### <span data-ttu-id="2fb48-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2fb48-124">-ResourceGroupName</span></span>
<span data-ttu-id="2fb48-125">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="2fb48-125">Resource Group Name</span></span>

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

### <span data-ttu-id="2fb48-126">-ServiceTag</span><span class="sxs-lookup"><span data-stu-id="2fb48-126">-ServiceTag</span></span>
<span data-ttu-id="2fb48-127">Nome da marca de serviço</span><span class="sxs-lookup"><span data-stu-id="2fb48-127">Name of Service Tag</span></span>

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

### <span data-ttu-id="2fb48-128">-SlotName</span><span class="sxs-lookup"><span data-stu-id="2fb48-128">-SlotName</span></span>
<span data-ttu-id="2fb48-129">Nome do slot de implantação.</span><span class="sxs-lookup"><span data-stu-id="2fb48-129">Deployment Slot Name.</span></span>

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

### <span data-ttu-id="2fb48-130">-Sub-RedeId</span><span class="sxs-lookup"><span data-stu-id="2fb48-130">-SubnetId</span></span>
<span data-ttu-id="2fb48-131">ResourceId da Sub-rede.</span><span class="sxs-lookup"><span data-stu-id="2fb48-131">ResourceId of Subnet.</span></span>

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

### <span data-ttu-id="2fb48-132">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="2fb48-132">-SubnetName</span></span>
<span data-ttu-id="2fb48-133">Nome da Sub-rede.</span><span class="sxs-lookup"><span data-stu-id="2fb48-133">Name of Subnet.</span></span>

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

### <span data-ttu-id="2fb48-134">-TargetScmSite</span><span class="sxs-lookup"><span data-stu-id="2fb48-134">-TargetScmSite</span></span>
<span data-ttu-id="2fb48-135">A regra destina-se ao site principal ou ao site Scm.</span><span class="sxs-lookup"><span data-stu-id="2fb48-135">Rule is aimed for Main site or Scm site.</span></span>

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

### <span data-ttu-id="2fb48-136">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="2fb48-136">-VirtualNetworkName</span></span>
<span data-ttu-id="2fb48-137">Nome da Rede Virtual (deve estar no mesmo grupo de recursos que o Web App).</span><span class="sxs-lookup"><span data-stu-id="2fb48-137">Name of Virtual Network (must be in same resource group as Web App).</span></span>

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

### <span data-ttu-id="2fb48-138">-WebAppName</span><span class="sxs-lookup"><span data-stu-id="2fb48-138">-WebAppName</span></span>
<span data-ttu-id="2fb48-139">O nome do aplicativo Web.</span><span class="sxs-lookup"><span data-stu-id="2fb48-139">The name of the web app.</span></span>

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

### <span data-ttu-id="2fb48-140">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="2fb48-140">-Confirm</span></span>
<span data-ttu-id="2fb48-141">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2fb48-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2fb48-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2fb48-142">-WhatIf</span></span>
<span data-ttu-id="2fb48-143">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="2fb48-143">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2fb48-144">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="2fb48-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2fb48-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2fb48-145">CommonParameters</span></span>
<span data-ttu-id="2fb48-146">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2fb48-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2fb48-147">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2fb48-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2fb48-148">Entradas</span><span class="sxs-lookup"><span data-stu-id="2fb48-148">INPUTS</span></span>

### <span data-ttu-id="2fb48-149">System.String</span><span class="sxs-lookup"><span data-stu-id="2fb48-149">System.String</span></span>

## <span data-ttu-id="2fb48-150">Saídas</span><span class="sxs-lookup"><span data-stu-id="2fb48-150">OUTPUTS</span></span>

### <span data-ttu-id="2fb48-151">Microsoft.Azure.Commands.WebApps.Models.PSAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="2fb48-151">Microsoft.Azure.Commands.WebApps.Models.PSAccessRestrictionConfig</span></span>

## <span data-ttu-id="2fb48-152">Notas</span><span class="sxs-lookup"><span data-stu-id="2fb48-152">NOTES</span></span>

## <span data-ttu-id="2fb48-153">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2fb48-153">RELATED LINKS</span></span>

[<span data-ttu-id="2fb48-154">Get-AzWebAppAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="2fb48-154">Get-AzWebAppAccessRestrictionConfig</span></span>](./Get-AzWebAppAccessRestrictionConfig.md)

[<span data-ttu-id="2fb48-155">Update-AzWebAppAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="2fb48-155">Update-AzWebAppAccessRestrictionConfig</span></span>](./Update-AzWebAppAccessRestrictionConfig.md)

[<span data-ttu-id="2fb48-156">Add-AzWebAppAccessRestrictionRule</span><span class="sxs-lookup"><span data-stu-id="2fb48-156">Add-AzWebAppAccessRestrictionRule</span></span>](./Add-AzWebAppAccessRestrictionRule.md)
