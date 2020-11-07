---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 8F36244D-A4D7-40BB-AC4C-E9AD445549F8
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/new-azappserviceplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzAppServicePlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzAppServicePlan.md
ms.openlocfilehash: 918f590258e6678a66262a6ad2d72a352bf13fd3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93774326"
---
# <span data-ttu-id="1010d-101">New-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="1010d-101">New-AzAppServicePlan</span></span>

## <span data-ttu-id="1010d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1010d-102">SYNOPSIS</span></span>
<span data-ttu-id="1010d-103">Cria um plano do serviço de aplicativo Azure em uma determinada localização geográfica.</span><span class="sxs-lookup"><span data-stu-id="1010d-103">Creates an Azure App Service plan in a given Geo location.</span></span>

## <span data-ttu-id="1010d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1010d-104">SYNTAX</span></span>

### <span data-ttu-id="1010d-105">Eles</span><span class="sxs-lookup"><span data-stu-id="1010d-105">S1</span></span>
```
New-AzAppServicePlan [-Location] <String> [[-Tier] <String>] [[-NumberofWorkers] <Int32>]
 [[-WorkerSize] <String>] [[-AseName] <String>] [[-AseResourceGroupName] <String>] [-PerSiteScaling <Boolean>]
 [-HyperV] [-AsJob] [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="1010d-106">S2</span><span class="sxs-lookup"><span data-stu-id="1010d-106">S2</span></span>
```
New-AzAppServicePlan [-Location] <String> [[-Tier] <String>] [[-NumberofWorkers] <Int32>]
 [[-WorkerSize] <String>] [[-AseName] <String>] [[-AseResourceGroupName] <String>] [-PerSiteScaling <Boolean>]
 [-AsJob] [-AppServicePlan] <PSAppServicePlan> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1010d-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1010d-107">DESCRIPTION</span></span>
<span data-ttu-id="1010d-108">O cmdlet **New-AzAppServicePlan** cria um plano do serviço de aplicativo do Azure em uma determinada localização geográfica com a camada especificada, o tamanho do trabalhador e o número de trabalhadores.</span><span class="sxs-lookup"><span data-stu-id="1010d-108">The **New-AzAppServicePlan** cmdlet creates an Azure App Service plan in a given Geo location with the specified Tier, worker size, and number of workers.</span></span>

## <span data-ttu-id="1010d-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1010d-109">EXAMPLES</span></span>

### <span data-ttu-id="1010d-110">Exemplo 1: criar um plano do serviço de aplicativo</span><span class="sxs-lookup"><span data-stu-id="1010d-110">Example 1: Create an App Service plan</span></span>
```
PS C:\>New-AzAppServicePlan -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP" -Location "West US" -Tier "Basic" -NumberofWorkers 2 -WorkerSize "Small"
```

<span data-ttu-id="1010d-111">Esse comando cria um plano do serviço de aplicativo chamado ContosoASP no grupo de recursos chamado Default-Web-Oesteus na localização geográfica oeste dos EUA.</span><span class="sxs-lookup"><span data-stu-id="1010d-111">This command creates an App Service plan named ContosoASP in the resource group named Default-Web-WestUS in Geo location West US.</span></span>
<span data-ttu-id="1010d-112">O comando especifica um nível básico e aloca dois trabalhadores pequenos.</span><span class="sxs-lookup"><span data-stu-id="1010d-112">The command specifies a Basic Tier and allocates two small workers.</span></span>

## <span data-ttu-id="1010d-113">OS</span><span class="sxs-lookup"><span data-stu-id="1010d-113">PARAMETERS</span></span>

### <span data-ttu-id="1010d-114">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="1010d-114">-AppServicePlan</span></span>
<span data-ttu-id="1010d-115">Objeto plano do serviço de aplicativo</span><span class="sxs-lookup"><span data-stu-id="1010d-115">App Service Plan Object</span></span>

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

### <span data-ttu-id="1010d-116">-AseName</span><span class="sxs-lookup"><span data-stu-id="1010d-116">-AseName</span></span>
<span data-ttu-id="1010d-117">Nome do ambiente do serviço de aplicativo</span><span class="sxs-lookup"><span data-stu-id="1010d-117">App Service Environment Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1010d-118">-AseResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1010d-118">-AseResourceGroupName</span></span>
<span data-ttu-id="1010d-119">Nome do grupo de recursos do ambiente do serviço de aplicativo</span><span class="sxs-lookup"><span data-stu-id="1010d-119">App Service Environment Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1010d-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1010d-120">-AsJob</span></span>
<span data-ttu-id="1010d-121">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="1010d-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1010d-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1010d-122">-DefaultProfile</span></span>
<span data-ttu-id="1010d-123">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1010d-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1010d-124">-HyperV</span><span class="sxs-lookup"><span data-stu-id="1010d-124">-HyperV</span></span>
<span data-ttu-id="1010d-125">Especificar isso, o plano do serviço de aplicativo executará os contêineres do Windows</span><span class="sxs-lookup"><span data-stu-id="1010d-125">Specify this, App Service Plan will run Windows Containers</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: S1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1010d-126">-Local</span><span class="sxs-lookup"><span data-stu-id="1010d-126">-Location</span></span>
<span data-ttu-id="1010d-127">Ponto</span><span class="sxs-lookup"><span data-stu-id="1010d-127">Location</span></span> 

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1010d-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="1010d-128">-Name</span></span>
<span data-ttu-id="1010d-129">Nome do plano do serviço de aplicativo</span><span class="sxs-lookup"><span data-stu-id="1010d-129">App Service Plan Name</span></span>

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

### <span data-ttu-id="1010d-130">-NumberofWorkers</span><span class="sxs-lookup"><span data-stu-id="1010d-130">-NumberofWorkers</span></span>
<span data-ttu-id="1010d-131">Número de trabalhadores</span><span class="sxs-lookup"><span data-stu-id="1010d-131">Number Of Workers</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: 1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1010d-132">-PerSiteScaling</span><span class="sxs-lookup"><span data-stu-id="1010d-132">-PerSiteScaling</span></span>
<span data-ttu-id="1010d-133">Se o dimensionamento por site deve ou não ser habilitado</span><span class="sxs-lookup"><span data-stu-id="1010d-133">Whether or not to enable Per Site Scaling</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1010d-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1010d-134">-ResourceGroupName</span></span>
<span data-ttu-id="1010d-135">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="1010d-135">Resource Group Name</span></span>

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

### <span data-ttu-id="1010d-136">-Tier</span><span class="sxs-lookup"><span data-stu-id="1010d-136">-Tier</span></span>
<span data-ttu-id="1010d-137">Hierarquiza</span><span class="sxs-lookup"><span data-stu-id="1010d-137">Tier</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: Free
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1010d-138">-Trabalhadores</span><span class="sxs-lookup"><span data-stu-id="1010d-138">-WorkerSize</span></span>
<span data-ttu-id="1010d-139">Tamanho do Web Worker</span><span class="sxs-lookup"><span data-stu-id="1010d-139">Size of web worker</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Small, Medium, Large, ExtraLarge

Required: False
Position: 5
Default value: Small
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1010d-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1010d-140">CommonParameters</span></span>
<span data-ttu-id="1010d-141">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1010d-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1010d-142">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1010d-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1010d-143">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1010d-143">INPUTS</span></span>

### <span data-ttu-id="1010d-144">Microsoft. Azure. Commands. webapps. Models. WebApp. PSAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="1010d-144">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSAppServicePlan</span></span>

## <span data-ttu-id="1010d-145">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1010d-145">OUTPUTS</span></span>

### <span data-ttu-id="1010d-146">Microsoft. Azure. Commands. webapps. Models. WebApp. PSAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="1010d-146">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSAppServicePlan</span></span>

## <span data-ttu-id="1010d-147">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1010d-147">NOTES</span></span>

## <span data-ttu-id="1010d-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1010d-148">RELATED LINKS</span></span>

[<span data-ttu-id="1010d-149">Get-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="1010d-149">Get-AzAppServicePlan</span></span>](./Get-AzAppServicePlan.md)

[<span data-ttu-id="1010d-150">Remove-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="1010d-150">Remove-AzAppServicePlan</span></span>](./Remove-AzAppServicePlan.md)

[<span data-ttu-id="1010d-151">Set-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="1010d-151">Set-AzAppServicePlan</span></span>](./Set-AzAppServicePlan.md)

