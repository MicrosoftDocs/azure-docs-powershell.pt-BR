---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 32D45795-FBCD-4157-BF45-41BD1F61782E
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/set-azappserviceplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzAppServicePlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzAppServicePlan.md
ms.openlocfilehash: e33e80207b6490ef7197754af8857b2359e01400
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93942900"
---
# <span data-ttu-id="3890e-101">Set-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="3890e-101">Set-AzAppServicePlan</span></span>

## <span data-ttu-id="3890e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3890e-102">SYNOPSIS</span></span>
<span data-ttu-id="3890e-103">Define um plano do serviço de aplicativo Azure.</span><span class="sxs-lookup"><span data-stu-id="3890e-103">Sets an Azure App Service plan.</span></span>

## <span data-ttu-id="3890e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3890e-104">SYNTAX</span></span>

### <span data-ttu-id="3890e-105">Eles</span><span class="sxs-lookup"><span data-stu-id="3890e-105">S1</span></span>
```
Set-AzAppServicePlan [[-AdminSiteName] <String>] [[-Tier] <String>] [[-NumberofWorkers] <Int32>]
 [[-WorkerSize] <String>] [-PerSiteScaling <Boolean>] [-AsJob] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3890e-106">S2</span><span class="sxs-lookup"><span data-stu-id="3890e-106">S2</span></span>
```
Set-AzAppServicePlan [-AsJob] [-AppServicePlan] <PSAppServicePlan> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3890e-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3890e-107">DESCRIPTION</span></span>
<span data-ttu-id="3890e-108">O cmdlet **set-AzAppServicePlan** define um plano do serviço de aplicativo Azure.</span><span class="sxs-lookup"><span data-stu-id="3890e-108">The **Set-AzAppServicePlan** cmdlet sets an Azure App Service plan.</span></span>

## <span data-ttu-id="3890e-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3890e-109">EXAMPLES</span></span>

### <span data-ttu-id="3890e-110">1: modificar um plano do serviço de aplicativo</span><span class="sxs-lookup"><span data-stu-id="3890e-110">1: Modify an App Service plan</span></span>
```
PS C:\>Set-AzAppServicePlan -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP" -PerSiteScaling $true
```

<span data-ttu-id="3890e-111">Esse comando define a opção PerSiteScaling como true no plano do serviço de aplicativo chamado ContosoASP que pertence ao grupo de recursos chamado Default-Web-Oesteus.</span><span class="sxs-lookup"><span data-stu-id="3890e-111">This command sets the PerSiteScaling option to true on the App Service plan named ContosoASP that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="3890e-112">OS</span><span class="sxs-lookup"><span data-stu-id="3890e-112">PARAMETERS</span></span>

### <span data-ttu-id="3890e-113">-AdminSiteName</span><span class="sxs-lookup"><span data-stu-id="3890e-113">-AdminSiteName</span></span>
<span data-ttu-id="3890e-114">Nome do site de administração</span><span class="sxs-lookup"><span data-stu-id="3890e-114">Admin Site Name</span></span>

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

### <span data-ttu-id="3890e-115">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="3890e-115">-AppServicePlan</span></span>
<span data-ttu-id="3890e-116">Objeto plano do serviço de aplicativo</span><span class="sxs-lookup"><span data-stu-id="3890e-116">App Service Plan Object</span></span>

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

### <span data-ttu-id="3890e-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3890e-117">-AsJob</span></span>
<span data-ttu-id="3890e-118">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="3890e-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3890e-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3890e-119">-DefaultProfile</span></span>
<span data-ttu-id="3890e-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3890e-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3890e-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="3890e-121">-Name</span></span>
<span data-ttu-id="3890e-122">Nome do plano do serviço de aplicativo</span><span class="sxs-lookup"><span data-stu-id="3890e-122">App Service Plan Name</span></span>

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

### <span data-ttu-id="3890e-123">-NumberofWorkers</span><span class="sxs-lookup"><span data-stu-id="3890e-123">-NumberofWorkers</span></span>
<span data-ttu-id="3890e-124">Número de trabalhadores</span><span class="sxs-lookup"><span data-stu-id="3890e-124">Number Of Workers</span></span>

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

### <span data-ttu-id="3890e-125">-PerSiteScaling</span><span class="sxs-lookup"><span data-stu-id="3890e-125">-PerSiteScaling</span></span>
<span data-ttu-id="3890e-126">Booleano de dimensionamento por site</span><span class="sxs-lookup"><span data-stu-id="3890e-126">Per Site Scaling Boolean</span></span>

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

### <span data-ttu-id="3890e-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3890e-127">-ResourceGroupName</span></span>
<span data-ttu-id="3890e-128">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="3890e-128">Resource Group Name</span></span>

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

### <span data-ttu-id="3890e-129">-Tier</span><span class="sxs-lookup"><span data-stu-id="3890e-129">-Tier</span></span>
<span data-ttu-id="3890e-130">Hierarquiza</span><span class="sxs-lookup"><span data-stu-id="3890e-130">Tier</span></span>

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

### <span data-ttu-id="3890e-131">-Trabalhadores</span><span class="sxs-lookup"><span data-stu-id="3890e-131">-WorkerSize</span></span>
<span data-ttu-id="3890e-132">Tamanho do trabalhador</span><span class="sxs-lookup"><span data-stu-id="3890e-132">Worker Size</span></span>

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

### <span data-ttu-id="3890e-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3890e-133">CommonParameters</span></span>
<span data-ttu-id="3890e-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3890e-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3890e-135">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3890e-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3890e-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3890e-136">INPUTS</span></span>

### <span data-ttu-id="3890e-137">Microsoft. Azure. Commands. webapps. Models. WebApp. PSAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="3890e-137">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSAppServicePlan</span></span>

## <span data-ttu-id="3890e-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3890e-138">OUTPUTS</span></span>

### <span data-ttu-id="3890e-139">Microsoft. Azure. Commands. webapps. Models. WebApp. PSAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="3890e-139">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSAppServicePlan</span></span>

## <span data-ttu-id="3890e-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3890e-140">NOTES</span></span>

## <span data-ttu-id="3890e-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3890e-141">RELATED LINKS</span></span>

[<span data-ttu-id="3890e-142">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="3890e-142">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="3890e-143">New-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="3890e-143">New-AzWebApp</span></span>](./New-AzWebApp.md)

[<span data-ttu-id="3890e-144">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="3890e-144">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)

[<span data-ttu-id="3890e-145">Restart-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="3890e-145">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="3890e-146">Start-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="3890e-146">Start-AzWebApp</span></span>](./Start-AzWebApp.md)

[<span data-ttu-id="3890e-147">Parar-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="3890e-147">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)


