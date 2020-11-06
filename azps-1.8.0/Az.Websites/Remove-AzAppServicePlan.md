---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 78AAF476-2E9E-4E60-9940-9A9AC6F9506A
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/remove-azappserviceplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzAppServicePlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzAppServicePlan.md
ms.openlocfilehash: f541ac58fe8512d67fab1755cfededc8839388e9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93598322"
---
# <span data-ttu-id="95bdc-101">Remove-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="95bdc-101">Remove-AzAppServicePlan</span></span>

## <span data-ttu-id="95bdc-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="95bdc-102">SYNOPSIS</span></span>
<span data-ttu-id="95bdc-103">Remove um plano do serviço de aplicativo do Azure.</span><span class="sxs-lookup"><span data-stu-id="95bdc-103">Removes an Azure App Service plan.</span></span>

## <span data-ttu-id="95bdc-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="95bdc-104">SYNTAX</span></span>

### <span data-ttu-id="95bdc-105">Eles</span><span class="sxs-lookup"><span data-stu-id="95bdc-105">S1</span></span>
```
Remove-AzAppServicePlan [-Force] [-AsJob] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="95bdc-106">S2</span><span class="sxs-lookup"><span data-stu-id="95bdc-106">S2</span></span>
```
Remove-AzAppServicePlan [-Force] [-AsJob] [-AppServicePlan] <PSAppServicePlan>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="95bdc-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="95bdc-107">DESCRIPTION</span></span>
<span data-ttu-id="95bdc-108">O cmdlet **Remove-AzAppServicePlan** remove um plano do serviço de aplicativo do Azure.</span><span class="sxs-lookup"><span data-stu-id="95bdc-108">The **Remove-AzAppServicePlan** cmdlet removes an Azure App Service plan.</span></span>

## <span data-ttu-id="95bdc-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="95bdc-109">EXAMPLES</span></span>

### <span data-ttu-id="95bdc-110">Exemplo 1: remover um plano do serviço de aplicativo</span><span class="sxs-lookup"><span data-stu-id="95bdc-110">Example 1: Remove an App Service plan</span></span>
```
PS C:\>Remove-AzAppServicePlan -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP"
```

<span data-ttu-id="95bdc-111">Esse comando Remove o plano do serviço de aplicativo Azure chamado ContosoASP que pertence ao grupo de recursos chamado Default-Web-Oesteus.</span><span class="sxs-lookup"><span data-stu-id="95bdc-111">This command removes the Azure App Service plan named ContosoASP that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="95bdc-112">OS</span><span class="sxs-lookup"><span data-stu-id="95bdc-112">PARAMETERS</span></span>

### <span data-ttu-id="95bdc-113">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="95bdc-113">-AppServicePlan</span></span>
<span data-ttu-id="95bdc-114">Objeto plano do serviço de aplicativo</span><span class="sxs-lookup"><span data-stu-id="95bdc-114">App Service Plan Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.WebApp.PSAppServicePlan
Parameter Sets: S2
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="95bdc-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="95bdc-115">-AsJob</span></span>
<span data-ttu-id="95bdc-116">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="95bdc-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="95bdc-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95bdc-117">-DefaultProfile</span></span>
<span data-ttu-id="95bdc-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="95bdc-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="95bdc-119">-Force</span><span class="sxs-lookup"><span data-stu-id="95bdc-119">-Force</span></span>
<span data-ttu-id="95bdc-120">Opção de remoção forçada</span><span class="sxs-lookup"><span data-stu-id="95bdc-120">Forcefully Remove Option</span></span>

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

### <span data-ttu-id="95bdc-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="95bdc-121">-Name</span></span>
<span data-ttu-id="95bdc-122">Nome do plano do serviço de aplicativo</span><span class="sxs-lookup"><span data-stu-id="95bdc-122">App Service Plan Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95bdc-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="95bdc-123">-ResourceGroupName</span></span>
<span data-ttu-id="95bdc-124">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="95bdc-124">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95bdc-125">-Confirme</span><span class="sxs-lookup"><span data-stu-id="95bdc-125">-Confirm</span></span>
<span data-ttu-id="95bdc-126">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="95bdc-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95bdc-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="95bdc-127">-WhatIf</span></span>
<span data-ttu-id="95bdc-128">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="95bdc-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="95bdc-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="95bdc-129">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95bdc-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95bdc-130">CommonParameters</span></span>
<span data-ttu-id="95bdc-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="95bdc-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95bdc-132">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="95bdc-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95bdc-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="95bdc-133">INPUTS</span></span>

### <span data-ttu-id="95bdc-134">Microsoft. Azure. Commands. webapps. Models. WebApp. PSAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="95bdc-134">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSAppServicePlan</span></span>

## <span data-ttu-id="95bdc-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="95bdc-135">OUTPUTS</span></span>

### <span data-ttu-id="95bdc-136">Microsoft. Azure. AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="95bdc-136">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="95bdc-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="95bdc-137">NOTES</span></span>

## <span data-ttu-id="95bdc-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="95bdc-138">RELATED LINKS</span></span>

[<span data-ttu-id="95bdc-139">Get-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="95bdc-139">Get-AzAppServicePlan</span></span>](./Get-AzAppServicePlan.md)

[<span data-ttu-id="95bdc-140">New-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="95bdc-140">New-AzAppServicePlan</span></span>](./New-AzAppServicePlan.md)

[<span data-ttu-id="95bdc-141">Set-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="95bdc-141">Set-AzAppServicePlan</span></span>](./Set-AzAppServicePlan.md)


