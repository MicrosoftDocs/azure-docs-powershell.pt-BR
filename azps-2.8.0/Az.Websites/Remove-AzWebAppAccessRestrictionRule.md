---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppAccessRestrictionRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppAccessRestrictionRule.md
ms.openlocfilehash: 0631492bf2574fed7a9bb755088d811483504763
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93774440"
---
# <span data-ttu-id="67969-101">Remove-AzWebAppAccessRestrictionRule</span><span class="sxs-lookup"><span data-stu-id="67969-101">Remove-AzWebAppAccessRestrictionRule</span></span>

## <span data-ttu-id="67969-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="67969-102">SYNOPSIS</span></span>
<span data-ttu-id="67969-103">Remove uma regra de restrição de acesso de um aplicativo Web do Azure.</span><span class="sxs-lookup"><span data-stu-id="67969-103">Removes an Access Restriction rule from an Azure Web App.</span></span>

## <span data-ttu-id="67969-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="67969-104">SYNTAX</span></span>

```
Remove-AzWebAppAccessRestrictionRule [-ResourceGroupName] <String> [-WebAppName] <String> -Name <String>
 [-TargetScmSite] [-SlotName <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="67969-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="67969-105">DESCRIPTION</span></span>
<span data-ttu-id="67969-106">O cmdlet **Remove-AzWebAppAccessRestrictionRule** remove uma regra de restrição de acesso de um aplicativo Web do Azure</span><span class="sxs-lookup"><span data-stu-id="67969-106">The **Remove-AzWebAppAccessRestrictionRule** cmdlet removes an Access Restriction rule from an Azure Web App</span></span>

## <span data-ttu-id="67969-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="67969-107">EXAMPLES</span></span>

### <span data-ttu-id="67969-108">Exemplo 1: remover uma regra de restrição de acesso do aplicativo Web</span><span class="sxs-lookup"><span data-stu-id="67969-108">Example 1: Remove a Web App Access Restriction Rule</span></span>
```
PS C:\>Remove-AzWebAppAccessRestrictionRule -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite" -Name IpRule
```

<span data-ttu-id="67969-109">Esse comando Remove a regra de restrição de acesso IpRule do Azure Web App chamado ContosoSite que pertence ao grupo de recursos chamado Default-Web-Oesteus.</span><span class="sxs-lookup"><span data-stu-id="67969-109">This command removes the IpRule access restriction rule from Azure Web App named ContosoSite that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="67969-110">OS</span><span class="sxs-lookup"><span data-stu-id="67969-110">PARAMETERS</span></span>

### <span data-ttu-id="67969-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67969-111">-DefaultProfile</span></span>
<span data-ttu-id="67969-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="67969-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="67969-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="67969-113">-Name</span></span>
<span data-ttu-id="67969-114">Nome da regra de restrição de acesso</span><span class="sxs-lookup"><span data-stu-id="67969-114">Access Restriction Rule Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67969-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="67969-115">-PassThru</span></span>
<span data-ttu-id="67969-116">Retorne o objeto de configuração de restrição de acesso.</span><span class="sxs-lookup"><span data-stu-id="67969-116">Return the access restriction config object.</span></span>

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

### <span data-ttu-id="67969-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="67969-117">-ResourceGroupName</span></span>
<span data-ttu-id="67969-118">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="67969-118">Resource Group Name</span></span>

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

### <span data-ttu-id="67969-119">-Slotname</span><span class="sxs-lookup"><span data-stu-id="67969-119">-SlotName</span></span>
<span data-ttu-id="67969-120">Nome do slot de implantação.</span><span class="sxs-lookup"><span data-stu-id="67969-120">Deployment Slot Name.</span></span>

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

### <span data-ttu-id="67969-121">-TargetScmSite</span><span class="sxs-lookup"><span data-stu-id="67969-121">-TargetScmSite</span></span>
<span data-ttu-id="67969-122">A regra é direcionada para o site principal ou o site do SCM.</span><span class="sxs-lookup"><span data-stu-id="67969-122">Rule is aimed for Main site or Scm site.</span></span>

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

### <span data-ttu-id="67969-123">-WebAppname</span><span class="sxs-lookup"><span data-stu-id="67969-123">-WebAppName</span></span>
<span data-ttu-id="67969-124">O nome do aplicativo Web.</span><span class="sxs-lookup"><span data-stu-id="67969-124">The name of the web app.</span></span>

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

### <span data-ttu-id="67969-125">-Confirme</span><span class="sxs-lookup"><span data-stu-id="67969-125">-Confirm</span></span>
<span data-ttu-id="67969-126">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="67969-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="67969-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="67969-127">-WhatIf</span></span>
<span data-ttu-id="67969-128">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="67969-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="67969-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="67969-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="67969-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67969-130">CommonParameters</span></span>
<span data-ttu-id="67969-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="67969-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67969-132">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="67969-132">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67969-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="67969-133">INPUTS</span></span>

### <span data-ttu-id="67969-134">System. String</span><span class="sxs-lookup"><span data-stu-id="67969-134">System.String</span></span>

## <span data-ttu-id="67969-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="67969-135">OUTPUTS</span></span>

### <span data-ttu-id="67969-136">Microsoft. Azure. Commands. webapps. Models. PSAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="67969-136">Microsoft.Azure.Commands.WebApps.Models.PSAccessRestrictionConfig</span></span>

## <span data-ttu-id="67969-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="67969-137">NOTES</span></span>

## <span data-ttu-id="67969-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="67969-138">RELATED LINKS</span></span>

[<span data-ttu-id="67969-139">Get-AzWebAppAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="67969-139">Get-AzWebAppAccessRestrictionConfig</span></span>](./Get-AzWebAppAccessRestrictionConfig.md)

[<span data-ttu-id="67969-140">Update-AzWebAppAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="67969-140">Update-AzWebAppAccessRestrictionConfig</span></span>](./Update-AzWebAppAccessRestrictionConfig.md)

[<span data-ttu-id="67969-141">Add-AzWebAppAccessRestrictionRule</span><span class="sxs-lookup"><span data-stu-id="67969-141">Add-AzWebAppAccessRestrictionRule</span></span>](./Add-AzWebAppAccessRestrictionRule.md)
