---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 78AAF476-2E9E-4E60-9940-9A9AC6F9506A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/remove-azurermappserviceplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Remove-AzureRmAppServicePlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Remove-AzureRmAppServicePlan.md
ms.openlocfilehash: b97506b8f104859c54c55ee1a937916623f4201d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427084"
---
# <span data-ttu-id="46cb5-101">Remove-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="46cb5-101">Remove-AzureRmAppServicePlan</span></span>

## <span data-ttu-id="46cb5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="46cb5-102">SYNOPSIS</span></span>
<span data-ttu-id="46cb5-103">Remove um plano do serviço de aplicativo do Azure.</span><span class="sxs-lookup"><span data-stu-id="46cb5-103">Removes an Azure App Service plan.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="46cb5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="46cb5-104">SYNTAX</span></span>

### <span data-ttu-id="46cb5-105">Eles</span><span class="sxs-lookup"><span data-stu-id="46cb5-105">S1</span></span>
```
Remove-AzureRmAppServicePlan [-Force] [-AsJob] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="46cb5-106">S2</span><span class="sxs-lookup"><span data-stu-id="46cb5-106">S2</span></span>
```
Remove-AzureRmAppServicePlan [-Force] [-AsJob] [-AppServicePlan] <PSAppServicePlan>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="46cb5-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="46cb5-107">DESCRIPTION</span></span>
<span data-ttu-id="46cb5-108">O cmdlet **Remove-AzureRmAppServicePlan** remove um plano do serviço de aplicativo do Azure.</span><span class="sxs-lookup"><span data-stu-id="46cb5-108">The **Remove-AzureRmAppServicePlan** cmdlet removes an Azure App Service plan.</span></span>

## <span data-ttu-id="46cb5-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="46cb5-109">EXAMPLES</span></span>

### <span data-ttu-id="46cb5-110">Exemplo 1: remover um plano do serviço de aplicativo</span><span class="sxs-lookup"><span data-stu-id="46cb5-110">Example 1: Remove an App Service plan</span></span>
```
PS C:\>Remove-AzureRmAppServicePlan -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP"
```

<span data-ttu-id="46cb5-111">Esse comando Remove o plano do serviço de aplicativo Azure chamado ContosoASP que pertence ao grupo de recursos chamado Default-Web-Oesteus.</span><span class="sxs-lookup"><span data-stu-id="46cb5-111">This command removes the Azure App Service plan named ContosoASP that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="46cb5-112">OS</span><span class="sxs-lookup"><span data-stu-id="46cb5-112">PARAMETERS</span></span>

### <span data-ttu-id="46cb5-113">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="46cb5-113">-AppServicePlan</span></span>
<span data-ttu-id="46cb5-114">Objeto plano do serviço de aplicativo</span><span class="sxs-lookup"><span data-stu-id="46cb5-114">App Service Plan Object</span></span>

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

### <span data-ttu-id="46cb5-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="46cb5-115">-AsJob</span></span>
<span data-ttu-id="46cb5-116">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="46cb5-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="46cb5-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46cb5-117">-DefaultProfile</span></span>
<span data-ttu-id="46cb5-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="46cb5-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46cb5-119">-Force</span><span class="sxs-lookup"><span data-stu-id="46cb5-119">-Force</span></span>
<span data-ttu-id="46cb5-120">Opção de remoção forçada</span><span class="sxs-lookup"><span data-stu-id="46cb5-120">Forcefully Remove Option</span></span>

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

### <span data-ttu-id="46cb5-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="46cb5-121">-Name</span></span>
<span data-ttu-id="46cb5-122">Nome do plano do serviço de aplicativo</span><span class="sxs-lookup"><span data-stu-id="46cb5-122">App Service Plan Name</span></span>

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

### <span data-ttu-id="46cb5-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="46cb5-123">-ResourceGroupName</span></span>
<span data-ttu-id="46cb5-124">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="46cb5-124">Resource Group Name</span></span>

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

### <span data-ttu-id="46cb5-125">-Confirme</span><span class="sxs-lookup"><span data-stu-id="46cb5-125">-Confirm</span></span>
<span data-ttu-id="46cb5-126">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="46cb5-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="46cb5-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="46cb5-127">-WhatIf</span></span>
<span data-ttu-id="46cb5-128">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="46cb5-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="46cb5-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="46cb5-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="46cb5-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46cb5-130">CommonParameters</span></span>
<span data-ttu-id="46cb5-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="46cb5-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46cb5-132">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="46cb5-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46cb5-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="46cb5-133">INPUTS</span></span>

### <span data-ttu-id="46cb5-134">Microsoft. Azure. Management. WebSites. Models. AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="46cb5-134">Microsoft.Azure.Management.WebSites.Models.AppServicePlan</span></span>
<span data-ttu-id="46cb5-135">Parâmetros: AppServicePlan (ByValue)</span><span class="sxs-lookup"><span data-stu-id="46cb5-135">Parameters: AppServicePlan (ByValue)</span></span>

## <span data-ttu-id="46cb5-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="46cb5-136">OUTPUTS</span></span>

### <span data-ttu-id="46cb5-137">Microsoft. Azure. AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="46cb5-137">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="46cb5-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="46cb5-138">NOTES</span></span>

## <span data-ttu-id="46cb5-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="46cb5-139">RELATED LINKS</span></span>

[<span data-ttu-id="46cb5-140">Get-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="46cb5-140">Get-AzureRmAppServicePlan</span></span>](./Get-AzureRmAppServicePlan.md)

[<span data-ttu-id="46cb5-141">New-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="46cb5-141">New-AzureRmAppServicePlan</span></span>](./New-AzureRmAppServicePlan.md)

[<span data-ttu-id="46cb5-142">Set-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="46cb5-142">Set-AzureRmAppServicePlan</span></span>](./Set-AzureRmAppServicePlan.md)


