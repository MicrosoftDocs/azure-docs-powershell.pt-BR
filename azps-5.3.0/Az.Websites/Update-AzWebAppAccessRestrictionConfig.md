---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Update-AzWebAppAccessRestrictionConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Update-AzWebAppAccessRestrictionConfig.md
ms.openlocfilehash: b2d2a2eb24fce89c65561c9d86f18072d4ac4e0a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98427749"
---
# <span data-ttu-id="acc1e-101">Update-AzWebAppAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="acc1e-101">Update-AzWebAppAccessRestrictionConfig</span></span>

## <span data-ttu-id="acc1e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="acc1e-102">SYNOPSIS</span></span>
<span data-ttu-id="acc1e-103">Atualiza a herança de configuração do restiction de acesso ao site principal para o site do SCM para um aplicativo Web do Azure.</span><span class="sxs-lookup"><span data-stu-id="acc1e-103">Updates the inheritance of Main site Access Restiction config to SCM Site for an Azure Web App.</span></span>

## <span data-ttu-id="acc1e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="acc1e-104">SYNTAX</span></span>

### <span data-ttu-id="acc1e-105">InputValuesParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="acc1e-105">InputValuesParameterSet (Default)</span></span>
```
Update-AzWebAppAccessRestrictionConfig [-ResourceGroupName] <String> [-Name] <String>
 [-ScmSiteUseMainSiteRestrictionConfig] [-SlotName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="acc1e-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="acc1e-106">InputObjectParameterSet</span></span>
```
Update-AzWebAppAccessRestrictionConfig [-PassThru] -InputObject <PSAccessRestrictionConfig>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="acc1e-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="acc1e-107">DESCRIPTION</span></span>
<span data-ttu-id="acc1e-108">O cmdlet **Update-AzWebAppAccessRestrictionConfig** atualiza a configuração de restrição de acesso para um aplicativo Web do Azure.</span><span class="sxs-lookup"><span data-stu-id="acc1e-108">The **Update-AzWebAppAccessRestrictionConfig** cmdlet updates Access Restriction config for an Azure Web App.</span></span>

## <span data-ttu-id="acc1e-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="acc1e-109">EXAMPLES</span></span>

### <span data-ttu-id="acc1e-110">Exemplo 1: atualizar um site de SCM do aplicativo Web para usar as restrições de acesso do site principal</span><span class="sxs-lookup"><span data-stu-id="acc1e-110">Example 1: Update a Web App SCM Site to use Access Restrictions from Main Site</span></span>

<span data-ttu-id="acc1e-111">O exemplo a seguir atualiza um aplicativo Web chamado IpRule que pertence ao grupo de recursos MyResource do grupo de recursos para usar a configuração de restrição de acesso do site principal no site do SCM.</span><span class="sxs-lookup"><span data-stu-id="acc1e-111">The following example updates a Web App named IpRule that belongs to the resource group MyResourceGroup to use access restriction config of main site on the scm site.</span></span>

```powershell <!-- Aladdin Generated Example --> 
Update-AzWebAppAccessRestrictionConfig -Name IpRule -ResourceGroupName MyResourceGroup -ScmSiteUseMainSiteRestrictionConfig
```

## <span data-ttu-id="acc1e-112">OS</span><span class="sxs-lookup"><span data-stu-id="acc1e-112">PARAMETERS</span></span>

### <span data-ttu-id="acc1e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="acc1e-113">-DefaultProfile</span></span>
<span data-ttu-id="acc1e-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="acc1e-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="acc1e-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="acc1e-115">-InputObject</span></span>
<span data-ttu-id="acc1e-116">O objeto config da restrição de acesso</span><span class="sxs-lookup"><span data-stu-id="acc1e-116">The access restriction config object</span></span>

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

### <span data-ttu-id="acc1e-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="acc1e-117">-Name</span></span>
<span data-ttu-id="acc1e-118">Nome do WebApp</span><span class="sxs-lookup"><span data-stu-id="acc1e-118">WebApp Name</span></span>

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

### <span data-ttu-id="acc1e-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="acc1e-119">-PassThru</span></span>
<span data-ttu-id="acc1e-120">Retorne o objeto de configuração de restrição de acesso.</span><span class="sxs-lookup"><span data-stu-id="acc1e-120">Return the access restriction config object.</span></span>

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

### <span data-ttu-id="acc1e-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="acc1e-121">-ResourceGroupName</span></span>
<span data-ttu-id="acc1e-122">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="acc1e-122">Resource Group Name</span></span>

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

### <span data-ttu-id="acc1e-123">-ScmSiteUseMainSiteRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="acc1e-123">-ScmSiteUseMainSiteRestrictionConfig</span></span>
<span data-ttu-id="acc1e-124">O site do SCM herda as regras definidas no site principal.</span><span class="sxs-lookup"><span data-stu-id="acc1e-124">Scm site inherits rules set on Main site.</span></span>

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

### <span data-ttu-id="acc1e-125">-Slotname</span><span class="sxs-lookup"><span data-stu-id="acc1e-125">-SlotName</span></span>
<span data-ttu-id="acc1e-126">Nome do slot de implantação.</span><span class="sxs-lookup"><span data-stu-id="acc1e-126">Deployment Slot name.</span></span>

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

### <span data-ttu-id="acc1e-127">-Confirme</span><span class="sxs-lookup"><span data-stu-id="acc1e-127">-Confirm</span></span>
<span data-ttu-id="acc1e-128">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="acc1e-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="acc1e-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="acc1e-129">-WhatIf</span></span>
<span data-ttu-id="acc1e-130">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="acc1e-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="acc1e-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="acc1e-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="acc1e-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="acc1e-132">CommonParameters</span></span>
<span data-ttu-id="acc1e-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="acc1e-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="acc1e-134">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="acc1e-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="acc1e-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="acc1e-135">INPUTS</span></span>

### <span data-ttu-id="acc1e-136">System. String</span><span class="sxs-lookup"><span data-stu-id="acc1e-136">System.String</span></span>

### <span data-ttu-id="acc1e-137">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="acc1e-137">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="acc1e-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="acc1e-138">OUTPUTS</span></span>

### <span data-ttu-id="acc1e-139">Microsoft. Azure. Commands. webapps. Models. PSAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="acc1e-139">Microsoft.Azure.Commands.WebApps.Models.PSAccessRestrictionConfig</span></span>

## <span data-ttu-id="acc1e-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="acc1e-140">NOTES</span></span>

## <span data-ttu-id="acc1e-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="acc1e-141">RELATED LINKS</span></span>

[<span data-ttu-id="acc1e-142">Get-AzWebAppAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="acc1e-142">Get-AzWebAppAccessRestrictionConfig</span></span>](./Get-AzWebAppAccessRestrictionConfig.md)

[<span data-ttu-id="acc1e-143">Add-AzWebAppAccessRestrictionRule</span><span class="sxs-lookup"><span data-stu-id="acc1e-143">Add-AzWebAppAccessRestrictionRule</span></span>](./Add-AzWebAppAccessRestrictionRule.md)

[<span data-ttu-id="acc1e-144">Remove-AzWebAppAccessRestrictionRule</span><span class="sxs-lookup"><span data-stu-id="acc1e-144">Remove-AzWebAppAccessRestrictionRule</span></span>](./Remove-AzWebAppAccessRestrictionRule.md)
