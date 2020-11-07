---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Update-AzWebAppAccessRestrictionConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Update-AzWebAppAccessRestrictionConfig.md
ms.openlocfilehash: 7c3caf3dfc033e6edefaf81b5f6bf5729ae86126
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93774412"
---
# <span data-ttu-id="7ebcb-101">Update-AzWebAppAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="7ebcb-101">Update-AzWebAppAccessRestrictionConfig</span></span>

## <span data-ttu-id="7ebcb-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7ebcb-102">SYNOPSIS</span></span>
<span data-ttu-id="7ebcb-103">Atualiza a herança de configuração do restiction de acesso ao site principal para o site do SCM para um aplicativo Web do Azure.</span><span class="sxs-lookup"><span data-stu-id="7ebcb-103">Updates the inheritance of Main site Access Restiction config to SCM Site for an Azure Web App.</span></span>

## <span data-ttu-id="7ebcb-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7ebcb-104">SYNTAX</span></span>

### <span data-ttu-id="7ebcb-105">InputValuesParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="7ebcb-105">InputValuesParameterSet (Default)</span></span>
```
Update-AzWebAppAccessRestrictionConfig [-ResourceGroupName] <String> [-Name] <String>
 [-ScmSiteUseMainSiteRestrictionConfig] [-SlotName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7ebcb-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7ebcb-106">InputObjectParameterSet</span></span>
```
Update-AzWebAppAccessRestrictionConfig [-PassThru] -InputObject <PSAccessRestrictionConfig>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7ebcb-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7ebcb-107">DESCRIPTION</span></span>
<span data-ttu-id="7ebcb-108">O cmdlet **Update-AzWebAppAccessRestrictionConfig** atualiza a configuração de restrição de acesso para um aplicativo Web do Azure.</span><span class="sxs-lookup"><span data-stu-id="7ebcb-108">The **Update-AzWebAppAccessRestrictionConfig** cmdlet updates Access Restriction config for an Azure Web App.</span></span>

## <span data-ttu-id="7ebcb-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7ebcb-109">EXAMPLES</span></span>

### <span data-ttu-id="7ebcb-110">Exemplo 1: atualizar um site de SCM do aplicativo Web para usar as restrições de acesso do site principal</span><span class="sxs-lookup"><span data-stu-id="7ebcb-110">Example 1: Update a Web App SCM Site to use Access Restrictions from Main Site</span></span>
```
PS C:\>Set-AzWebAppAccessRestriction -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite" -ScmSiteUseMainSiteRestrictionConfig
```

<span data-ttu-id="7ebcb-111">Esse comando atualiza um aplicativo Web chamado ContosoSite que pertence ao grupo de recursos Default-Web-Oesteus para usar a configuração de restrição de acesso do site principal no site do SCM.</span><span class="sxs-lookup"><span data-stu-id="7ebcb-111">This command updates a Web App named ContosoSite that belongs to the resource group Default-Web-WestUS to use access restriction config of main site on the scm site.</span></span>

## <span data-ttu-id="7ebcb-112">OS</span><span class="sxs-lookup"><span data-stu-id="7ebcb-112">PARAMETERS</span></span>

### <span data-ttu-id="7ebcb-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ebcb-113">-DefaultProfile</span></span>
<span data-ttu-id="7ebcb-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7ebcb-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7ebcb-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7ebcb-115">-InputObject</span></span>
<span data-ttu-id="7ebcb-116">O objeto config da restrição de acesso</span><span class="sxs-lookup"><span data-stu-id="7ebcb-116">The access restriction config object</span></span>

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

### <span data-ttu-id="7ebcb-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="7ebcb-117">-Name</span></span>
<span data-ttu-id="7ebcb-118">Nome do WebApp</span><span class="sxs-lookup"><span data-stu-id="7ebcb-118">WebApp Name</span></span>

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

### <span data-ttu-id="7ebcb-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7ebcb-119">-PassThru</span></span>
<span data-ttu-id="7ebcb-120">Retorne o objeto de configuração de restrição de acesso.</span><span class="sxs-lookup"><span data-stu-id="7ebcb-120">Return the access restriction config object.</span></span>

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

### <span data-ttu-id="7ebcb-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7ebcb-121">-ResourceGroupName</span></span>
<span data-ttu-id="7ebcb-122">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="7ebcb-122">Resource Group Name</span></span>

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

### <span data-ttu-id="7ebcb-123">-ScmSiteUseMainSiteRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="7ebcb-123">-ScmSiteUseMainSiteRestrictionConfig</span></span>
<span data-ttu-id="7ebcb-124">O site do SCM herda as regras definidas no site principal.</span><span class="sxs-lookup"><span data-stu-id="7ebcb-124">Scm site inherits rules set on Main site.</span></span>

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

### <span data-ttu-id="7ebcb-125">-Slotname</span><span class="sxs-lookup"><span data-stu-id="7ebcb-125">-SlotName</span></span>
<span data-ttu-id="7ebcb-126">Nome do slot de implantação.</span><span class="sxs-lookup"><span data-stu-id="7ebcb-126">Deployment Slot name.</span></span>

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

### <span data-ttu-id="7ebcb-127">-Confirme</span><span class="sxs-lookup"><span data-stu-id="7ebcb-127">-Confirm</span></span>
<span data-ttu-id="7ebcb-128">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7ebcb-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7ebcb-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7ebcb-129">-WhatIf</span></span>
<span data-ttu-id="7ebcb-130">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="7ebcb-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7ebcb-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="7ebcb-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7ebcb-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ebcb-132">CommonParameters</span></span>
<span data-ttu-id="7ebcb-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7ebcb-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ebcb-134">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7ebcb-134">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ebcb-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7ebcb-135">INPUTS</span></span>

### <span data-ttu-id="7ebcb-136">System. String</span><span class="sxs-lookup"><span data-stu-id="7ebcb-136">System.String</span></span>

### <span data-ttu-id="7ebcb-137">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="7ebcb-137">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="7ebcb-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7ebcb-138">OUTPUTS</span></span>

### <span data-ttu-id="7ebcb-139">Microsoft. Azure. Commands. webapps. Models. PSAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="7ebcb-139">Microsoft.Azure.Commands.WebApps.Models.PSAccessRestrictionConfig</span></span>

## <span data-ttu-id="7ebcb-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7ebcb-140">NOTES</span></span>

## <span data-ttu-id="7ebcb-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7ebcb-141">RELATED LINKS</span></span>

[<span data-ttu-id="7ebcb-142">Get-AzWebAppAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="7ebcb-142">Get-AzWebAppAccessRestrictionConfig</span></span>](./Get-AzWebAppAccessRestrictionConfig.md)

[<span data-ttu-id="7ebcb-143">Add-AzWebAppAccessRestrictionRule</span><span class="sxs-lookup"><span data-stu-id="7ebcb-143">Add-AzWebAppAccessRestrictionRule</span></span>](./Add-AzWebAppAccessRestrictionRule.md)

[<span data-ttu-id="7ebcb-144">Remove-AzWebAppAccessRestrictionRule</span><span class="sxs-lookup"><span data-stu-id="7ebcb-144">Remove-AzWebAppAccessRestrictionRule</span></span>](./Remove-AzWebAppAccessRestrictionRule.md)
