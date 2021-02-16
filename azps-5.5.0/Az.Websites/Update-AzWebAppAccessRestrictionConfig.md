---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Update-AzWebAppAccessRestrictionConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Update-AzWebAppAccessRestrictionConfig.md
ms.openlocfilehash: b2d2a2eb24fce89c65561c9d86f18072d4ac4e0a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118491"
---
# <span data-ttu-id="eb4e7-101">Update-AzWebAppAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="eb4e7-101">Update-AzWebAppAccessRestrictionConfig</span></span>

## <span data-ttu-id="eb4e7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="eb4e7-102">SYNOPSIS</span></span>
<span data-ttu-id="eb4e7-103">Atualiza a herança da configuração Restiction do Access do site principal para o Site de SCM de um Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="eb4e7-103">Updates the inheritance of Main site Access Restiction config to SCM Site for an Azure Web App.</span></span>

## <span data-ttu-id="eb4e7-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="eb4e7-104">SYNTAX</span></span>

### <span data-ttu-id="eb4e7-105">InputValuesParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="eb4e7-105">InputValuesParameterSet (Default)</span></span>
```
Update-AzWebAppAccessRestrictionConfig [-ResourceGroupName] <String> [-Name] <String>
 [-ScmSiteUseMainSiteRestrictionConfig] [-SlotName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eb4e7-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="eb4e7-106">InputObjectParameterSet</span></span>
```
Update-AzWebAppAccessRestrictionConfig [-PassThru] -InputObject <PSAccessRestrictionConfig>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eb4e7-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="eb4e7-107">DESCRIPTION</span></span>
<span data-ttu-id="eb4e7-108">O cmdlet **Update-AzWebAppAccessRestrictionConfig** atualiza o configuração de Restrição do Access para um Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="eb4e7-108">The **Update-AzWebAppAccessRestrictionConfig** cmdlet updates Access Restriction config for an Azure Web App.</span></span>

## <span data-ttu-id="eb4e7-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="eb4e7-109">EXAMPLES</span></span>

### <span data-ttu-id="eb4e7-110">Exemplo 1: Atualizar um site de SCM do Aplicativo Web para usar as Restrições de Acesso do Site Principal</span><span class="sxs-lookup"><span data-stu-id="eb4e7-110">Example 1: Update a Web App SCM Site to use Access Restrictions from Main Site</span></span>

<span data-ttu-id="eb4e7-111">O exemplo a seguir atualiza um Web App chamado IpRule que pertence ao grupo de recursos MyResourceGroup para usar o config de restrição de acesso do site principal no site de scm.</span><span class="sxs-lookup"><span data-stu-id="eb4e7-111">The following example updates a Web App named IpRule that belongs to the resource group MyResourceGroup to use access restriction config of main site on the scm site.</span></span>

```powershell <!-- Aladdin Generated Example --> 
Update-AzWebAppAccessRestrictionConfig -Name IpRule -ResourceGroupName MyResourceGroup -ScmSiteUseMainSiteRestrictionConfig
```

## <span data-ttu-id="eb4e7-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="eb4e7-112">PARAMETERS</span></span>

### <span data-ttu-id="eb4e7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb4e7-113">-DefaultProfile</span></span>
<span data-ttu-id="eb4e7-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="eb4e7-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eb4e7-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="eb4e7-115">-InputObject</span></span>
<span data-ttu-id="eb4e7-116">O objeto de configuração de restrição de acesso</span><span class="sxs-lookup"><span data-stu-id="eb4e7-116">The access restriction config object</span></span>

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

### <span data-ttu-id="eb4e7-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="eb4e7-117">-Name</span></span>
<span data-ttu-id="eb4e7-118">Nome webapp</span><span class="sxs-lookup"><span data-stu-id="eb4e7-118">WebApp Name</span></span>

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

### <span data-ttu-id="eb4e7-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="eb4e7-119">-PassThru</span></span>
<span data-ttu-id="eb4e7-120">Retornar o objeto de configuração de restrição de acesso.</span><span class="sxs-lookup"><span data-stu-id="eb4e7-120">Return the access restriction config object.</span></span>

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

### <span data-ttu-id="eb4e7-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eb4e7-121">-ResourceGroupName</span></span>
<span data-ttu-id="eb4e7-122">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="eb4e7-122">Resource Group Name</span></span>

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

### <span data-ttu-id="eb4e7-123">-ScmSiteUseMainSiteRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="eb4e7-123">-ScmSiteUseMainSiteRestrictionConfig</span></span>
<span data-ttu-id="eb4e7-124">O site Scm herda regras definidas no site principal.</span><span class="sxs-lookup"><span data-stu-id="eb4e7-124">Scm site inherits rules set on Main site.</span></span>

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

### <span data-ttu-id="eb4e7-125">-SlotName</span><span class="sxs-lookup"><span data-stu-id="eb4e7-125">-SlotName</span></span>
<span data-ttu-id="eb4e7-126">Nome do Slot de Implantação.</span><span class="sxs-lookup"><span data-stu-id="eb4e7-126">Deployment Slot name.</span></span>

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

### <span data-ttu-id="eb4e7-127">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="eb4e7-127">-Confirm</span></span>
<span data-ttu-id="eb4e7-128">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="eb4e7-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eb4e7-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eb4e7-129">-WhatIf</span></span>
<span data-ttu-id="eb4e7-130">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="eb4e7-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="eb4e7-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="eb4e7-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eb4e7-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb4e7-132">CommonParameters</span></span>
<span data-ttu-id="eb4e7-133">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eb4e7-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb4e7-134">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="eb4e7-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb4e7-135">Entradas</span><span class="sxs-lookup"><span data-stu-id="eb4e7-135">INPUTS</span></span>

### <span data-ttu-id="eb4e7-136">System.String</span><span class="sxs-lookup"><span data-stu-id="eb4e7-136">System.String</span></span>

### <span data-ttu-id="eb4e7-137">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="eb4e7-137">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="eb4e7-138">Saídas</span><span class="sxs-lookup"><span data-stu-id="eb4e7-138">OUTPUTS</span></span>

### <span data-ttu-id="eb4e7-139">Microsoft.Azure.Commands.WebApps.Models.PSAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="eb4e7-139">Microsoft.Azure.Commands.WebApps.Models.PSAccessRestrictionConfig</span></span>

## <span data-ttu-id="eb4e7-140">Notas</span><span class="sxs-lookup"><span data-stu-id="eb4e7-140">NOTES</span></span>

## <span data-ttu-id="eb4e7-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="eb4e7-141">RELATED LINKS</span></span>

[<span data-ttu-id="eb4e7-142">Get-AzWebAppAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="eb4e7-142">Get-AzWebAppAccessRestrictionConfig</span></span>](./Get-AzWebAppAccessRestrictionConfig.md)

[<span data-ttu-id="eb4e7-143">Add-AzWebAppAccessRestrictionRule</span><span class="sxs-lookup"><span data-stu-id="eb4e7-143">Add-AzWebAppAccessRestrictionRule</span></span>](./Add-AzWebAppAccessRestrictionRule.md)

[<span data-ttu-id="eb4e7-144">Remove-AzWebAppAccessRestrictionRule</span><span class="sxs-lookup"><span data-stu-id="eb4e7-144">Remove-AzWebAppAccessRestrictionRule</span></span>](./Remove-AzWebAppAccessRestrictionRule.md)
