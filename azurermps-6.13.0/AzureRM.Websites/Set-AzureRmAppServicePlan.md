---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 32D45795-FBCD-4157-BF45-41BD1F61782E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/set-azurermappserviceplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Set-AzureRmAppServicePlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Set-AzureRmAppServicePlan.md
ms.openlocfilehash: 2163c18fecadba069b7c3fba260ab81538ed5583
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430771"
---
# <span data-ttu-id="1131f-101">Set-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="1131f-101">Set-AzureRmAppServicePlan</span></span>

## <span data-ttu-id="1131f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1131f-102">SYNOPSIS</span></span>
<span data-ttu-id="1131f-103">Define um plano do serviço de aplicativo Azure.</span><span class="sxs-lookup"><span data-stu-id="1131f-103">Sets an Azure App Service plan.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1131f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1131f-104">SYNTAX</span></span>

### <span data-ttu-id="1131f-105">Eles</span><span class="sxs-lookup"><span data-stu-id="1131f-105">S1</span></span>
```
Set-AzureRmAppServicePlan [[-AdminSiteName] <String>] [[-Tier] <String>] [[-NumberofWorkers] <Int32>]
 [[-WorkerSize] <String>] [-PerSiteScaling <Boolean>] [-AsJob] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1131f-106">S2</span><span class="sxs-lookup"><span data-stu-id="1131f-106">S2</span></span>
```
Set-AzureRmAppServicePlan [-AsJob] [-AppServicePlan] <PSAppServicePlan>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1131f-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1131f-107">DESCRIPTION</span></span>
<span data-ttu-id="1131f-108">O cmdlet **set-AzureRmAppServicePlan** define um plano do serviço de aplicativo Azure.</span><span class="sxs-lookup"><span data-stu-id="1131f-108">The **Set-AzureRmAppServicePlan** cmdlet sets an Azure App Service plan.</span></span>

## <span data-ttu-id="1131f-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1131f-109">EXAMPLES</span></span>

### <span data-ttu-id="1131f-110">1: modificar um plano do serviço de aplicativo</span><span class="sxs-lookup"><span data-stu-id="1131f-110">1: Modify an App Service plan</span></span>
```
PS C:\>Set-AzureRmAppServicePlan -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP" -PerSiteScaling $true
```

<span data-ttu-id="1131f-111">Esse comando define a opção PerSiteScaling como true no plano do serviço de aplicativo chamado ContosoASP que pertence ao grupo de recursos chamado Default-Web-Oesteus.</span><span class="sxs-lookup"><span data-stu-id="1131f-111">This command sets the PerSiteScaling option to true on the App Service plan named ContosoASP that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="1131f-112">OS</span><span class="sxs-lookup"><span data-stu-id="1131f-112">PARAMETERS</span></span>

### <span data-ttu-id="1131f-113">-AdminSiteName</span><span class="sxs-lookup"><span data-stu-id="1131f-113">-AdminSiteName</span></span>
<span data-ttu-id="1131f-114">Nome do site de administração</span><span class="sxs-lookup"><span data-stu-id="1131f-114">Admin Site Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1131f-115">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="1131f-115">-AppServicePlan</span></span>
<span data-ttu-id="1131f-116">Objeto plano do serviço de aplicativo</span><span class="sxs-lookup"><span data-stu-id="1131f-116">App Service Plan Object</span></span>

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

### <span data-ttu-id="1131f-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1131f-117">-AsJob</span></span>
<span data-ttu-id="1131f-118">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="1131f-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1131f-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1131f-119">-DefaultProfile</span></span>
<span data-ttu-id="1131f-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1131f-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1131f-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="1131f-121">-Name</span></span>
<span data-ttu-id="1131f-122">Nome do plano do serviço de aplicativo</span><span class="sxs-lookup"><span data-stu-id="1131f-122">App Service Plan Name</span></span>

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

### <span data-ttu-id="1131f-123">-NumberofWorkers</span><span class="sxs-lookup"><span data-stu-id="1131f-123">-NumberofWorkers</span></span>
<span data-ttu-id="1131f-124">Número de trabalhadores</span><span class="sxs-lookup"><span data-stu-id="1131f-124">Number Of Workers</span></span>

```yaml
Type: System.Int32
Parameter Sets: S1
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1131f-125">-PerSiteScaling</span><span class="sxs-lookup"><span data-stu-id="1131f-125">-PerSiteScaling</span></span>
<span data-ttu-id="1131f-126">Booleano de dimensionamento por site</span><span class="sxs-lookup"><span data-stu-id="1131f-126">Per Site Scaling Boolean</span></span>

```yaml
Type: System.Boolean
Parameter Sets: S1
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1131f-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1131f-127">-ResourceGroupName</span></span>
<span data-ttu-id="1131f-128">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="1131f-128">Resource Group Name</span></span>

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

### <span data-ttu-id="1131f-129">-Tier</span><span class="sxs-lookup"><span data-stu-id="1131f-129">-Tier</span></span>
<span data-ttu-id="1131f-130">Hierarquiza</span><span class="sxs-lookup"><span data-stu-id="1131f-130">Tier</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1131f-131">-Trabalhadores</span><span class="sxs-lookup"><span data-stu-id="1131f-131">-WorkerSize</span></span>
<span data-ttu-id="1131f-132">Tamanho do trabalhador</span><span class="sxs-lookup"><span data-stu-id="1131f-132">Worker Size</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1131f-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1131f-133">CommonParameters</span></span>
<span data-ttu-id="1131f-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1131f-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1131f-135">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1131f-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1131f-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1131f-136">INPUTS</span></span>

### <span data-ttu-id="1131f-137">Microsoft. Azure. Management. WebSites. Models. AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="1131f-137">Microsoft.Azure.Management.WebSites.Models.AppServicePlan</span></span>
<span data-ttu-id="1131f-138">Parâmetros: AppServicePlan (ByValue)</span><span class="sxs-lookup"><span data-stu-id="1131f-138">Parameters: AppServicePlan (ByValue)</span></span>

## <span data-ttu-id="1131f-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1131f-139">OUTPUTS</span></span>

### <span data-ttu-id="1131f-140">Microsoft. Azure. Management. WebSites. Models. AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="1131f-140">Microsoft.Azure.Management.WebSites.Models.AppServicePlan</span></span>

## <span data-ttu-id="1131f-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1131f-141">NOTES</span></span>

## <span data-ttu-id="1131f-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1131f-142">RELATED LINKS</span></span>

[<span data-ttu-id="1131f-143">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="1131f-143">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)

[<span data-ttu-id="1131f-144">New-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="1131f-144">New-AzureRmWebApp</span></span>](./New-AzureRmWebApp.md)

[<span data-ttu-id="1131f-145">Remove-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="1131f-145">Remove-AzureRmWebApp</span></span>](./Remove-AzureRmWebApp.md)

[<span data-ttu-id="1131f-146">Restart-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="1131f-146">Restart-AzureRmWebApp</span></span>](./Restart-AzureRmWebApp.md)

[<span data-ttu-id="1131f-147">Start-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="1131f-147">Start-AzureRmWebApp</span></span>](./Start-AzureRmWebApp.md)

[<span data-ttu-id="1131f-148">Parar-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="1131f-148">Stop-AzureRmWebApp</span></span>](./Stop-AzureRmWebApp.md)


