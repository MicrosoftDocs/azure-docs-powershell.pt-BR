---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 32D45795-FBCD-4157-BF45-41BD1F61782E
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/set-azappserviceplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzAppServicePlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzAppServicePlan.md
ms.openlocfilehash: d27dc8ae315eb587ccb129125500a86e22429773
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93598299"
---
# <span data-ttu-id="b2ad8-101">Set-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="b2ad8-101">Set-AzAppServicePlan</span></span>

## <span data-ttu-id="b2ad8-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b2ad8-102">SYNOPSIS</span></span>
<span data-ttu-id="b2ad8-103">Define um plano do serviço de aplicativo Azure.</span><span class="sxs-lookup"><span data-stu-id="b2ad8-103">Sets an Azure App Service plan.</span></span>

## <span data-ttu-id="b2ad8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b2ad8-104">SYNTAX</span></span>

### <span data-ttu-id="b2ad8-105">Eles</span><span class="sxs-lookup"><span data-stu-id="b2ad8-105">S1</span></span>
```
Set-AzAppServicePlan [[-AdminSiteName] <String>] [[-Tier] <String>] [[-NumberofWorkers] <Int32>]
 [[-WorkerSize] <String>] [-PerSiteScaling <Boolean>] [-AsJob] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b2ad8-106">S2</span><span class="sxs-lookup"><span data-stu-id="b2ad8-106">S2</span></span>
```
Set-AzAppServicePlan [-AsJob] [-AppServicePlan] <PSAppServicePlan> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b2ad8-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b2ad8-107">DESCRIPTION</span></span>
<span data-ttu-id="b2ad8-108">O cmdlet **set-AzAppServicePlan** define um plano do serviço de aplicativo Azure.</span><span class="sxs-lookup"><span data-stu-id="b2ad8-108">The **Set-AzAppServicePlan** cmdlet sets an Azure App Service plan.</span></span>

## <span data-ttu-id="b2ad8-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b2ad8-109">EXAMPLES</span></span>

### <span data-ttu-id="b2ad8-110">1: modificar um plano do serviço de aplicativo</span><span class="sxs-lookup"><span data-stu-id="b2ad8-110">1: Modify an App Service plan</span></span>
```
PS C:\>Set-AzAppServicePlan -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP" -PerSiteScaling $true
```

<span data-ttu-id="b2ad8-111">Esse comando define a opção PerSiteScaling como true no plano do serviço de aplicativo chamado ContosoASP que pertence ao grupo de recursos chamado Default-Web-Oesteus.</span><span class="sxs-lookup"><span data-stu-id="b2ad8-111">This command sets the PerSiteScaling option to true on the App Service plan named ContosoASP that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="b2ad8-112">OS</span><span class="sxs-lookup"><span data-stu-id="b2ad8-112">PARAMETERS</span></span>

### <span data-ttu-id="b2ad8-113">-AdminSiteName</span><span class="sxs-lookup"><span data-stu-id="b2ad8-113">-AdminSiteName</span></span>
<span data-ttu-id="b2ad8-114">Nome do site de administração</span><span class="sxs-lookup"><span data-stu-id="b2ad8-114">Admin Site Name</span></span>

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

### <span data-ttu-id="b2ad8-115">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="b2ad8-115">-AppServicePlan</span></span>
<span data-ttu-id="b2ad8-116">Objeto plano do serviço de aplicativo</span><span class="sxs-lookup"><span data-stu-id="b2ad8-116">App Service Plan Object</span></span>

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

### <span data-ttu-id="b2ad8-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b2ad8-117">-AsJob</span></span>
<span data-ttu-id="b2ad8-118">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="b2ad8-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b2ad8-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2ad8-119">-DefaultProfile</span></span>
<span data-ttu-id="b2ad8-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b2ad8-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b2ad8-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="b2ad8-121">-Name</span></span>
<span data-ttu-id="b2ad8-122">Nome do plano do serviço de aplicativo</span><span class="sxs-lookup"><span data-stu-id="b2ad8-122">App Service Plan Name</span></span>

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

### <span data-ttu-id="b2ad8-123">-NumberofWorkers</span><span class="sxs-lookup"><span data-stu-id="b2ad8-123">-NumberofWorkers</span></span>
<span data-ttu-id="b2ad8-124">Número de trabalhadores</span><span class="sxs-lookup"><span data-stu-id="b2ad8-124">Number Of Workers</span></span>

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

### <span data-ttu-id="b2ad8-125">-PerSiteScaling</span><span class="sxs-lookup"><span data-stu-id="b2ad8-125">-PerSiteScaling</span></span>
<span data-ttu-id="b2ad8-126">Booleano de dimensionamento por site</span><span class="sxs-lookup"><span data-stu-id="b2ad8-126">Per Site Scaling Boolean</span></span>

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

### <span data-ttu-id="b2ad8-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b2ad8-127">-ResourceGroupName</span></span>
<span data-ttu-id="b2ad8-128">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="b2ad8-128">Resource Group Name</span></span>

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

### <span data-ttu-id="b2ad8-129">-Tier</span><span class="sxs-lookup"><span data-stu-id="b2ad8-129">-Tier</span></span>
<span data-ttu-id="b2ad8-130">Hierarquiza</span><span class="sxs-lookup"><span data-stu-id="b2ad8-130">Tier</span></span>

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

### <span data-ttu-id="b2ad8-131">-Trabalhadores</span><span class="sxs-lookup"><span data-stu-id="b2ad8-131">-WorkerSize</span></span>
<span data-ttu-id="b2ad8-132">Tamanho do trabalhador</span><span class="sxs-lookup"><span data-stu-id="b2ad8-132">Worker Size</span></span>

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

### <span data-ttu-id="b2ad8-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2ad8-133">CommonParameters</span></span>
<span data-ttu-id="b2ad8-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b2ad8-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2ad8-135">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b2ad8-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2ad8-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b2ad8-136">INPUTS</span></span>

### <span data-ttu-id="b2ad8-137">Microsoft. Azure. Commands. webapps. Models. WebApp. PSAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="b2ad8-137">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSAppServicePlan</span></span>

## <span data-ttu-id="b2ad8-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b2ad8-138">OUTPUTS</span></span>

### <span data-ttu-id="b2ad8-139">Microsoft. Azure. Commands. webapps. Models. WebApp. PSAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="b2ad8-139">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSAppServicePlan</span></span>

## <span data-ttu-id="b2ad8-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b2ad8-140">NOTES</span></span>

## <span data-ttu-id="b2ad8-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b2ad8-141">RELATED LINKS</span></span>

[<span data-ttu-id="b2ad8-142">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="b2ad8-142">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="b2ad8-143">New-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="b2ad8-143">New-AzWebApp</span></span>](./New-AzWebApp.md)

[<span data-ttu-id="b2ad8-144">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="b2ad8-144">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)

[<span data-ttu-id="b2ad8-145">Restart-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="b2ad8-145">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="b2ad8-146">Start-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="b2ad8-146">Start-AzWebApp</span></span>](./Start-AzWebApp.md)

[<span data-ttu-id="b2ad8-147">Parar-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="b2ad8-147">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)


