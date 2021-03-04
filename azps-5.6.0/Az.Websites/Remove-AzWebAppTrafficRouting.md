---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppTrafficRouting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppTrafficRouting.md
ms.openlocfilehash: 0dda79130d150265d8050fcb5ba951cd243bebda
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890336"
---
# <span data-ttu-id="2c00d-101">Remove-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="2c00d-101">Remove-AzWebAppTrafficRouting</span></span>

## <span data-ttu-id="2c00d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2c00d-102">SYNOPSIS</span></span>
<span data-ttu-id="2c00d-103">Remova uma regra de roteamento do Slot.</span><span class="sxs-lookup"><span data-stu-id="2c00d-103">Remove a routing Rule from the Slot.</span></span>

## <span data-ttu-id="2c00d-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="2c00d-104">SYNTAX</span></span>

```
Remove-AzWebAppTrafficRouting -ResourceGroupName <String> -WebAppName <String> -RuleName <String>
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2c00d-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="2c00d-105">DESCRIPTION</span></span>
<span data-ttu-id="2c00d-106">O cmdlet **Remove-AzWebAppTrafficRouting** remove uma regra de roteamento de um Slot de Aplicativo Web do Azure.</span><span class="sxs-lookup"><span data-stu-id="2c00d-106">The **Remove-AzWebAppTrafficRouting** cmdlet removes a routing rule from an Azure Web App Slot.</span></span>

## <span data-ttu-id="2c00d-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2c00d-107">EXAMPLES</span></span>

### <span data-ttu-id="2c00d-108">Exemplo 1 Remove a regra de roteamento específica do slot webapp</span><span class="sxs-lookup"><span data-stu-id="2c00d-108">Example 1 Removes the specific routing rule from webapp slot</span></span>
```powershell
PS C:\> Remove-AzWebAppTrafficRouting -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite"  -RuleName 'Stg'
```

<span data-ttu-id="2c00d-109">Este comando remove uma regra de roteamento para um determinado slot de webapp.</span><span class="sxs-lookup"><span data-stu-id="2c00d-109">This command removes a routing rule for a given webapp slot.</span></span>

## <span data-ttu-id="2c00d-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="2c00d-110">PARAMETERS</span></span>

### <span data-ttu-id="2c00d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c00d-111">-DefaultProfile</span></span>
<span data-ttu-id="2c00d-112">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2c00d-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2c00d-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2c00d-113">-ResourceGroupName</span></span>
<span data-ttu-id="2c00d-114">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="2c00d-114">Resource Group Name</span></span>

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

### <span data-ttu-id="2c00d-115">-RuleName</span><span class="sxs-lookup"><span data-stu-id="2c00d-115">-RuleName</span></span>
<span data-ttu-id="2c00d-116">Nome da regra</span><span class="sxs-lookup"><span data-stu-id="2c00d-116">Rule Name</span></span>

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

### <span data-ttu-id="2c00d-117">-WebAppName</span><span class="sxs-lookup"><span data-stu-id="2c00d-117">-WebAppName</span></span>
<span data-ttu-id="2c00d-118">Nome do WebApp</span><span class="sxs-lookup"><span data-stu-id="2c00d-118">WebApp Name</span></span>

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

### <span data-ttu-id="2c00d-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2c00d-119">-PassThru</span></span>
<span data-ttu-id="2c00d-120">Retorne o objeto config de restrição de acesso.</span><span class="sxs-lookup"><span data-stu-id="2c00d-120">Return the access restriction config object.</span></span>

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

### <span data-ttu-id="2c00d-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2c00d-121">-Confirm</span></span>
<span data-ttu-id="2c00d-122">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2c00d-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2c00d-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2c00d-123">-WhatIf</span></span>
<span data-ttu-id="2c00d-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="2c00d-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2c00d-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="2c00d-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2c00d-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c00d-126">CommonParameters</span></span>
<span data-ttu-id="2c00d-127">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2c00d-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c00d-128">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2c00d-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c00d-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2c00d-129">INPUTS</span></span>

### <span data-ttu-id="2c00d-130">Nenhum</span><span class="sxs-lookup"><span data-stu-id="2c00d-130">None</span></span>

## <span data-ttu-id="2c00d-131">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="2c00d-131">OUTPUTS</span></span>

### <span data-ttu-id="2c00d-132">Microsoft.Azure.Management.WebSites.Models.RampUpRule</span><span class="sxs-lookup"><span data-stu-id="2c00d-132">Microsoft.Azure.Management.WebSites.Models.RampUpRule</span></span>

## <span data-ttu-id="2c00d-133">NOTES</span><span class="sxs-lookup"><span data-stu-id="2c00d-133">NOTES</span></span>

## <span data-ttu-id="2c00d-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2c00d-134">RELATED LINKS</span></span>
[<span data-ttu-id="2c00d-135">Add-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="2c00d-135">Add-AzWebAppTrafficRouting</span></span>](./Add-AzWebAppTrafficRouting.md)

[<span data-ttu-id="2c00d-136">Get-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="2c00d-136">Get-AzWebAppTrafficRouting</span></span>](./Get-AzWebAppTrafficRouting.md)

[<span data-ttu-id="2c00d-137">Update-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="2c00d-137">Update-AzWebAppTrafficRouting</span></span>](./Update-AzWebAppTrafficRouting.md)