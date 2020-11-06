---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 8F36244D-A4D7-40BB-AC4C-E9AD445549F8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/new-azurermappserviceplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/New-AzureRmAppServicePlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/New-AzureRmAppServicePlan.md
ms.openlocfilehash: 09300c7d7d8394dbcfed36560c988f0193473c24
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93426249"
---
# <span data-ttu-id="43939-101">New-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="43939-101">New-AzureRmAppServicePlan</span></span>

## <span data-ttu-id="43939-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="43939-102">SYNOPSIS</span></span>
<span data-ttu-id="43939-103">Cria um plano do serviço de aplicativo Azure em uma determinada localização geográfica.</span><span class="sxs-lookup"><span data-stu-id="43939-103">Creates an Azure App Service plan in a given Geo location.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="43939-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="43939-104">SYNTAX</span></span>

### <span data-ttu-id="43939-105">Eles</span><span class="sxs-lookup"><span data-stu-id="43939-105">S1</span></span>
```
New-AzureRmAppServicePlan [-Location] <String> [[-Tier] <String>] [[-NumberofWorkers] <Int32>]
 [[-WorkerSize] <String>] [[-AseName] <String>] [[-AseResourceGroupName] <String>] [-PerSiteScaling <Boolean>]
 [-HyperV] [-AsJob] [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="43939-106">S2</span><span class="sxs-lookup"><span data-stu-id="43939-106">S2</span></span>
```
New-AzureRmAppServicePlan [-Location] <String> [[-Tier] <String>] [[-NumberofWorkers] <Int32>]
 [[-WorkerSize] <String>] [[-AseName] <String>] [[-AseResourceGroupName] <String>] [-PerSiteScaling <Boolean>]
 [-AsJob] [-AppServicePlan] <PSAppServicePlan> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="43939-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="43939-107">DESCRIPTION</span></span>
<span data-ttu-id="43939-108">O cmdlet **New-AzureRmAppServicePlan** cria um plano do serviço de aplicativo do Azure em uma determinada localização geográfica com a camada especificada, o tamanho do trabalhador e o número de trabalhadores.</span><span class="sxs-lookup"><span data-stu-id="43939-108">The **New-AzureRmAppServicePlan** cmdlet creates an Azure App Service plan in a given Geo location with the specified Tier, worker size, and number of workers.</span></span>

## <span data-ttu-id="43939-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="43939-109">EXAMPLES</span></span>

### <span data-ttu-id="43939-110">Exemplo 1: criar um plano do serviço de aplicativo</span><span class="sxs-lookup"><span data-stu-id="43939-110">Example 1: Create an App Service plan</span></span>
```
PS C:\>New-AzureRmAppServicePlan -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP" -Location "West US" -Tier "Basic" -NumberofWorkers 2 -WorkerSize "Small"
```

<span data-ttu-id="43939-111">Esse comando cria um plano do serviço de aplicativo chamado ContosoASP no grupo de recursos chamado Default-Web-Oesteus na localização geográfica oeste dos EUA.</span><span class="sxs-lookup"><span data-stu-id="43939-111">This command creates an App Service plan named ContosoASP in the resource group named Default-Web-WestUS in Geo location West US.</span></span>
<span data-ttu-id="43939-112">O comando especifica um nível básico e aloca dois trabalhadores pequenos.</span><span class="sxs-lookup"><span data-stu-id="43939-112">The command specifies a Basic Tier and allocates two small workers.</span></span>

## <span data-ttu-id="43939-113">OS</span><span class="sxs-lookup"><span data-stu-id="43939-113">PARAMETERS</span></span>

### <span data-ttu-id="43939-114">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="43939-114">-AppServicePlan</span></span>
<span data-ttu-id="43939-115">Objeto plano do serviço de aplicativo</span><span class="sxs-lookup"><span data-stu-id="43939-115">App Service Plan Object</span></span>

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

### <span data-ttu-id="43939-116">-AseName</span><span class="sxs-lookup"><span data-stu-id="43939-116">-AseName</span></span>
<span data-ttu-id="43939-117">Nome do ambiente do serviço de aplicativo</span><span class="sxs-lookup"><span data-stu-id="43939-117">App Service Environment Name</span></span>

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

### <span data-ttu-id="43939-118">-AseResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="43939-118">-AseResourceGroupName</span></span>
<span data-ttu-id="43939-119">Nome do grupo de recursos do ambiente do serviço de aplicativo</span><span class="sxs-lookup"><span data-stu-id="43939-119">App Service Environment Resource Group Name</span></span>

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

### <span data-ttu-id="43939-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="43939-120">-AsJob</span></span>
<span data-ttu-id="43939-121">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="43939-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="43939-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43939-122">-DefaultProfile</span></span>
<span data-ttu-id="43939-123">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="43939-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="43939-124">-HyperV</span><span class="sxs-lookup"><span data-stu-id="43939-124">-HyperV</span></span>
<span data-ttu-id="43939-125">Especificar isso, o plano do serviço de aplicativo executará os contêineres do Windows</span><span class="sxs-lookup"><span data-stu-id="43939-125">Specify this, App Service Plan will run Windows Containers</span></span>

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

### <span data-ttu-id="43939-126">-Local</span><span class="sxs-lookup"><span data-stu-id="43939-126">-Location</span></span>
<span data-ttu-id="43939-127">Ponto</span><span class="sxs-lookup"><span data-stu-id="43939-127">Location</span></span> 

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

### <span data-ttu-id="43939-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="43939-128">-Name</span></span>
<span data-ttu-id="43939-129">Nome do plano do serviço de aplicativo</span><span class="sxs-lookup"><span data-stu-id="43939-129">App Service Plan Name</span></span>

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

### <span data-ttu-id="43939-130">-NumberofWorkers</span><span class="sxs-lookup"><span data-stu-id="43939-130">-NumberofWorkers</span></span>
<span data-ttu-id="43939-131">Número de trabalhadores</span><span class="sxs-lookup"><span data-stu-id="43939-131">Number Of Workers</span></span>

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

### <span data-ttu-id="43939-132">-PerSiteScaling</span><span class="sxs-lookup"><span data-stu-id="43939-132">-PerSiteScaling</span></span>
<span data-ttu-id="43939-133">Se o dimensionamento por site deve ou não ser habilitado</span><span class="sxs-lookup"><span data-stu-id="43939-133">Whether or not to enable Per Site Scaling</span></span>

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

### <span data-ttu-id="43939-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="43939-134">-ResourceGroupName</span></span>
<span data-ttu-id="43939-135">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="43939-135">Resource Group Name</span></span>

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

### <span data-ttu-id="43939-136">-Tier</span><span class="sxs-lookup"><span data-stu-id="43939-136">-Tier</span></span>
<span data-ttu-id="43939-137">Hierarquiza</span><span class="sxs-lookup"><span data-stu-id="43939-137">Tier</span></span>

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

### <span data-ttu-id="43939-138">-Trabalhadores</span><span class="sxs-lookup"><span data-stu-id="43939-138">-WorkerSize</span></span>
<span data-ttu-id="43939-139">Tamanho do Web Worker</span><span class="sxs-lookup"><span data-stu-id="43939-139">Size of web worker</span></span>

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

### <span data-ttu-id="43939-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43939-140">CommonParameters</span></span>
<span data-ttu-id="43939-141">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="43939-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43939-142">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="43939-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43939-143">SENSORES</span><span class="sxs-lookup"><span data-stu-id="43939-143">INPUTS</span></span>

### <span data-ttu-id="43939-144">Microsoft. Azure. Management. WebSites. Models. AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="43939-144">Microsoft.Azure.Management.WebSites.Models.AppServicePlan</span></span>
<span data-ttu-id="43939-145">Parâmetros: AppServicePlan (ByValue)</span><span class="sxs-lookup"><span data-stu-id="43939-145">Parameters: AppServicePlan (ByValue)</span></span>

## <span data-ttu-id="43939-146">EXIBE</span><span class="sxs-lookup"><span data-stu-id="43939-146">OUTPUTS</span></span>

### <span data-ttu-id="43939-147">Microsoft. Azure. Management. WebSites. Models. AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="43939-147">Microsoft.Azure.Management.WebSites.Models.AppServicePlan</span></span>

## <span data-ttu-id="43939-148">INFORMA</span><span class="sxs-lookup"><span data-stu-id="43939-148">NOTES</span></span>

## <span data-ttu-id="43939-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="43939-149">RELATED LINKS</span></span>

[<span data-ttu-id="43939-150">Get-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="43939-150">Get-AzureRmAppServicePlan</span></span>](./Get-AzureRmAppServicePlan.md)

[<span data-ttu-id="43939-151">Remove-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="43939-151">Remove-AzureRmAppServicePlan</span></span>](./Remove-AzureRmAppServicePlan.md)

[<span data-ttu-id="43939-152">Set-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="43939-152">Set-AzureRmAppServicePlan</span></span>](./Set-AzureRmAppServicePlan.md)

