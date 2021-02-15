---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppTrafficRouting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppTrafficRouting.md
ms.openlocfilehash: 0dda79130d150265d8050fcb5ba951cd243bebda
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118841"
---
# <span data-ttu-id="e4874-101">Remove-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="e4874-101">Remove-AzWebAppTrafficRouting</span></span>

## <span data-ttu-id="e4874-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e4874-102">SYNOPSIS</span></span>
<span data-ttu-id="e4874-103">Remover uma Regra de Roteamento do Slot.</span><span class="sxs-lookup"><span data-stu-id="e4874-103">Remove a routing Rule from the Slot.</span></span>

## <span data-ttu-id="e4874-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e4874-104">SYNTAX</span></span>

```
Remove-AzWebAppTrafficRouting -ResourceGroupName <String> -WebAppName <String> -RuleName <String>
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e4874-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="e4874-105">DESCRIPTION</span></span>
<span data-ttu-id="e4874-106">O cmdlet **Remove-AzWebAppTrafficRouting** remove uma regra de roteamento de um Slot do Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="e4874-106">The **Remove-AzWebAppTrafficRouting** cmdlet removes a routing rule from an Azure Web App Slot.</span></span>

## <span data-ttu-id="e4874-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="e4874-107">EXAMPLES</span></span>

### <span data-ttu-id="e4874-108">Exemplo 1 Remove a regra de roteamento específica do slot webapp</span><span class="sxs-lookup"><span data-stu-id="e4874-108">Example 1 Removes the specific routing rule from webapp slot</span></span>
```powershell
PS C:\> Remove-AzWebAppTrafficRouting -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite"  -RuleName 'Stg'
```

<span data-ttu-id="e4874-109">Esse comando remove uma regra de roteamento para um determinado slot de webapp.</span><span class="sxs-lookup"><span data-stu-id="e4874-109">This command removes a routing rule for a given webapp slot.</span></span>

## <span data-ttu-id="e4874-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e4874-110">PARAMETERS</span></span>

### <span data-ttu-id="e4874-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4874-111">-DefaultProfile</span></span>
<span data-ttu-id="e4874-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e4874-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e4874-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e4874-113">-ResourceGroupName</span></span>
<span data-ttu-id="e4874-114">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="e4874-114">Resource Group Name</span></span>

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

### <span data-ttu-id="e4874-115">-NomeDa Regra</span><span class="sxs-lookup"><span data-stu-id="e4874-115">-RuleName</span></span>
<span data-ttu-id="e4874-116">Nome da Regra</span><span class="sxs-lookup"><span data-stu-id="e4874-116">Rule Name</span></span>

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

### <span data-ttu-id="e4874-117">-WebAppName</span><span class="sxs-lookup"><span data-stu-id="e4874-117">-WebAppName</span></span>
<span data-ttu-id="e4874-118">Nome webapp</span><span class="sxs-lookup"><span data-stu-id="e4874-118">WebApp Name</span></span>

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

### <span data-ttu-id="e4874-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e4874-119">-PassThru</span></span>
<span data-ttu-id="e4874-120">Retornar o objeto de configuração de restrição de acesso.</span><span class="sxs-lookup"><span data-stu-id="e4874-120">Return the access restriction config object.</span></span>

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

### <span data-ttu-id="e4874-121">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="e4874-121">-Confirm</span></span>
<span data-ttu-id="e4874-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e4874-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e4874-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e4874-123">-WhatIf</span></span>
<span data-ttu-id="e4874-124">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="e4874-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e4874-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e4874-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e4874-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4874-126">CommonParameters</span></span>
<span data-ttu-id="e4874-127">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e4874-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4874-128">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e4874-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4874-129">Entradas</span><span class="sxs-lookup"><span data-stu-id="e4874-129">INPUTS</span></span>

### <span data-ttu-id="e4874-130">Nenhum</span><span class="sxs-lookup"><span data-stu-id="e4874-130">None</span></span>

## <span data-ttu-id="e4874-131">Saídas</span><span class="sxs-lookup"><span data-stu-id="e4874-131">OUTPUTS</span></span>

### <span data-ttu-id="e4874-132">Microsoft.Azure.Management.WebSites.Models.RampUpRule</span><span class="sxs-lookup"><span data-stu-id="e4874-132">Microsoft.Azure.Management.WebSites.Models.RampUpRule</span></span>

## <span data-ttu-id="e4874-133">Notas</span><span class="sxs-lookup"><span data-stu-id="e4874-133">NOTES</span></span>

## <span data-ttu-id="e4874-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e4874-134">RELATED LINKS</span></span>
[<span data-ttu-id="e4874-135">Add-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="e4874-135">Add-AzWebAppTrafficRouting</span></span>](./Add-AzWebAppTrafficRouting.md)

[<span data-ttu-id="e4874-136">Get-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="e4874-136">Get-AzWebAppTrafficRouting</span></span>](./Get-AzWebAppTrafficRouting.md)

[<span data-ttu-id="e4874-137">Update-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="e4874-137">Update-AzWebAppTrafficRouting</span></span>](./Update-AzWebAppTrafficRouting.md)