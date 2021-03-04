---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Update-AzWebAppAccessRestrictionConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Update-AzWebAppAccessRestrictionConfig.md
ms.openlocfilehash: b2d2a2eb24fce89c65561c9d86f18072d4ac4e0a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101893024"
---
# <span data-ttu-id="8512d-101">Update-AzWebAppAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="8512d-101">Update-AzWebAppAccessRestrictionConfig</span></span>

## <span data-ttu-id="8512d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8512d-102">SYNOPSIS</span></span>
<span data-ttu-id="8512d-103">Atualiza a herança da configuração Restiction de Acesso ao Site principal do Site do Azure para um Aplicativo Web do Azure.</span><span class="sxs-lookup"><span data-stu-id="8512d-103">Updates the inheritance of Main site Access Restiction config to SCM Site for an Azure Web App.</span></span>

## <span data-ttu-id="8512d-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="8512d-104">SYNTAX</span></span>

### <span data-ttu-id="8512d-105">InputValuesParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="8512d-105">InputValuesParameterSet (Default)</span></span>
```
Update-AzWebAppAccessRestrictionConfig [-ResourceGroupName] <String> [-Name] <String>
 [-ScmSiteUseMainSiteRestrictionConfig] [-SlotName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8512d-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8512d-106">InputObjectParameterSet</span></span>
```
Update-AzWebAppAccessRestrictionConfig [-PassThru] -InputObject <PSAccessRestrictionConfig>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8512d-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="8512d-107">DESCRIPTION</span></span>
<span data-ttu-id="8512d-108">O cmdlet **Update-AzWebAppAccessRestrictionConfig** atualiza a configuração de Restrição de Acesso para um Aplicativo Web do Azure.</span><span class="sxs-lookup"><span data-stu-id="8512d-108">The **Update-AzWebAppAccessRestrictionConfig** cmdlet updates Access Restriction config for an Azure Web App.</span></span>

## <span data-ttu-id="8512d-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8512d-109">EXAMPLES</span></span>

### <span data-ttu-id="8512d-110">Exemplo 1: atualizar um site SCM do Aplicativo Web para usar restrições de acesso do Site Principal</span><span class="sxs-lookup"><span data-stu-id="8512d-110">Example 1: Update a Web App SCM Site to use Access Restrictions from Main Site</span></span>

<span data-ttu-id="8512d-111">O exemplo a seguir atualiza um Aplicativo Web chamado IpRule que pertence ao grupo de recursos MyResourceGroup para usar a configuração de restrição de acesso do site principal no site scm.</span><span class="sxs-lookup"><span data-stu-id="8512d-111">The following example updates a Web App named IpRule that belongs to the resource group MyResourceGroup to use access restriction config of main site on the scm site.</span></span>

```powershell <!-- Aladdin Generated Example --> 
Update-AzWebAppAccessRestrictionConfig -Name IpRule -ResourceGroupName MyResourceGroup -ScmSiteUseMainSiteRestrictionConfig
```

## <span data-ttu-id="8512d-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="8512d-112">PARAMETERS</span></span>

### <span data-ttu-id="8512d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8512d-113">-DefaultProfile</span></span>
<span data-ttu-id="8512d-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="8512d-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8512d-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8512d-115">-InputObject</span></span>
<span data-ttu-id="8512d-116">O objeto config de restrição de acesso</span><span class="sxs-lookup"><span data-stu-id="8512d-116">The access restriction config object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSAccessRestrictionConfig
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8512d-117">-Name</span><span class="sxs-lookup"><span data-stu-id="8512d-117">-Name</span></span>
<span data-ttu-id="8512d-118">Nome do WebApp</span><span class="sxs-lookup"><span data-stu-id="8512d-118">WebApp Name</span></span>

```yaml
Type: System.String
Parameter Sets: InputValuesParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8512d-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8512d-119">-PassThru</span></span>
<span data-ttu-id="8512d-120">Retorne o objeto config de restrição de acesso.</span><span class="sxs-lookup"><span data-stu-id="8512d-120">Return the access restriction config object.</span></span>

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

### <span data-ttu-id="8512d-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8512d-121">-ResourceGroupName</span></span>
<span data-ttu-id="8512d-122">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="8512d-122">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: InputValuesParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8512d-123">-ScmSiteUseMainSiteRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="8512d-123">-ScmSiteUseMainSiteRestrictionConfig</span></span>
<span data-ttu-id="8512d-124">O site Scm herda regras definidas no site principal.</span><span class="sxs-lookup"><span data-stu-id="8512d-124">Scm site inherits rules set on Main site.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: InputValuesParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8512d-125">-SlotName</span><span class="sxs-lookup"><span data-stu-id="8512d-125">-SlotName</span></span>
<span data-ttu-id="8512d-126">Nome do slot de implantação.</span><span class="sxs-lookup"><span data-stu-id="8512d-126">Deployment Slot name.</span></span>

```yaml
Type: System.String
Parameter Sets: InputValuesParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8512d-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8512d-127">-Confirm</span></span>
<span data-ttu-id="8512d-128">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8512d-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8512d-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8512d-129">-WhatIf</span></span>
<span data-ttu-id="8512d-130">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="8512d-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8512d-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="8512d-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8512d-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8512d-132">CommonParameters</span></span>
<span data-ttu-id="8512d-133">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8512d-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8512d-134">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8512d-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8512d-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8512d-135">INPUTS</span></span>

### <span data-ttu-id="8512d-136">System.String</span><span class="sxs-lookup"><span data-stu-id="8512d-136">System.String</span></span>

### <span data-ttu-id="8512d-137">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="8512d-137">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="8512d-138">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="8512d-138">OUTPUTS</span></span>

### <span data-ttu-id="8512d-139">Microsoft.Azure.Commands.WebApps.Models.PSAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="8512d-139">Microsoft.Azure.Commands.WebApps.Models.PSAccessRestrictionConfig</span></span>

## <span data-ttu-id="8512d-140">NOTES</span><span class="sxs-lookup"><span data-stu-id="8512d-140">NOTES</span></span>

## <span data-ttu-id="8512d-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8512d-141">RELATED LINKS</span></span>

[<span data-ttu-id="8512d-142">Get-AzWebAppAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="8512d-142">Get-AzWebAppAccessRestrictionConfig</span></span>](./Get-AzWebAppAccessRestrictionConfig.md)

[<span data-ttu-id="8512d-143">Add-AzWebAppAccessRestrictionRule</span><span class="sxs-lookup"><span data-stu-id="8512d-143">Add-AzWebAppAccessRestrictionRule</span></span>](./Add-AzWebAppAccessRestrictionRule.md)

[<span data-ttu-id="8512d-144">Remove-AzWebAppAccessRestrictionRule</span><span class="sxs-lookup"><span data-stu-id="8512d-144">Remove-AzWebAppAccessRestrictionRule</span></span>](./Remove-AzWebAppAccessRestrictionRule.md)
