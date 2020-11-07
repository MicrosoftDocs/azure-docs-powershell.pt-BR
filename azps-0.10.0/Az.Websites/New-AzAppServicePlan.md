---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az
ms.assetid: 8F36244D-A4D7-40BB-AC4C-E9AD445549F8
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/new-Azappserviceplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/New-AzAppServicePlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/New-AzAppServicePlan.md
ms.openlocfilehash: 040efd4e483825db637345fbd8bcb54a27e8675b
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93776099"
---
# <span data-ttu-id="6ebd9-101">New-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="6ebd9-101">New-AzAppServicePlan</span></span>

## <span data-ttu-id="6ebd9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6ebd9-102">SYNOPSIS</span></span>
<span data-ttu-id="6ebd9-103">Cria um plano do serviço de aplicativo Azure em uma determinada localização geográfica.</span><span class="sxs-lookup"><span data-stu-id="6ebd9-103">Creates an Azure App Service plan in a given Geo location.</span></span>

## <span data-ttu-id="6ebd9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6ebd9-104">SYNTAX</span></span>

### <span data-ttu-id="6ebd9-105">Eles</span><span class="sxs-lookup"><span data-stu-id="6ebd9-105">S1</span></span>
```
New-AzAppServicePlan [-Location] <String> [[-Tier] <String>] [[-NumberofWorkers] <Int32>]
 [[-WorkerSize] <String>] [[-AseName] <String>] [[-AseResourceGroupName] <String>] [-PerSiteScaling <Boolean>]
 [-ResourceGroupName] <String> [-Name] <String> [-AsJob][-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6ebd9-106">S2</span><span class="sxs-lookup"><span data-stu-id="6ebd9-106">S2</span></span>
```
New-AzAppServicePlan [-Location] <String> [[-Tier] <String>] [[-NumberofWorkers] <Int32>]
 [[-WorkerSize] <String>] [[-AseName] <String>] [[-AseResourceGroupName] <String>] [-PerSiteScaling <Boolean>]
 [-AppServicePlan] <ServerFarmWithRichSku> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6ebd9-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6ebd9-107">DESCRIPTION</span></span>
<span data-ttu-id="6ebd9-108">O cmdlet **New-AzAppServicePlan** cria um plano do serviço de aplicativo do Azure em uma determinada localização geográfica com a camada especificada, o tamanho do trabalhador e o número de trabalhadores.</span><span class="sxs-lookup"><span data-stu-id="6ebd9-108">The **New-AzAppServicePlan** cmdlet creates an Azure App Service plan in a given Geo location with the specified Tier, worker size, and number of workers.</span></span>

## <span data-ttu-id="6ebd9-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6ebd9-109">EXAMPLES</span></span>

### <span data-ttu-id="6ebd9-110">Exemplo 1: criar um plano do serviço de aplicativo</span><span class="sxs-lookup"><span data-stu-id="6ebd9-110">Example 1: Create an App Service plan</span></span>
```
PS C:\>New-AzAppServicePlan -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP" -Location "West US" -Tier "Basic" -NumberofWorkers 2 -WorkerSize "Small"
```

<span data-ttu-id="6ebd9-111">Esse comando cria um plano do serviço de aplicativo chamado ContosoASP no grupo de recursos chamado Default-Web-Oesteus na localização geográfica oeste dos EUA.</span><span class="sxs-lookup"><span data-stu-id="6ebd9-111">This command creates an App Service plan named ContosoASP in the resource group named Default-Web-WestUS in Geo location West US.</span></span>
<span data-ttu-id="6ebd9-112">O comando especifica um nível básico e aloca dois trabalhadores pequenos.</span><span class="sxs-lookup"><span data-stu-id="6ebd9-112">The command specifies a Basic Tier and allocates two small workers.</span></span>

## <span data-ttu-id="6ebd9-113">OS</span><span class="sxs-lookup"><span data-stu-id="6ebd9-113">PARAMETERS</span></span>

### <span data-ttu-id="6ebd9-114">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="6ebd9-114">-AppServicePlan</span></span>
<span data-ttu-id="6ebd9-115">Objeto plano do serviço de aplicativo</span><span class="sxs-lookup"><span data-stu-id="6ebd9-115">App Service Plan Object</span></span>

```yaml
Type: ServerFarmWithRichSku
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6ebd9-116">-AseName</span><span class="sxs-lookup"><span data-stu-id="6ebd9-116">-AseName</span></span>
<span data-ttu-id="6ebd9-117">Nome do ambiente do serviço de aplicativo</span><span class="sxs-lookup"><span data-stu-id="6ebd9-117">App Service Environment Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ebd9-118">-AseResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6ebd9-118">-AseResourceGroupName</span></span>
<span data-ttu-id="6ebd9-119">Nome do grupo de recursos do ambiente do serviço de aplicativo</span><span class="sxs-lookup"><span data-stu-id="6ebd9-119">App Service Environment Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ebd9-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ebd9-120">-DefaultProfile</span></span>
<span data-ttu-id="6ebd9-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6ebd9-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ebd9-122">-Local</span><span class="sxs-lookup"><span data-stu-id="6ebd9-122">-Location</span></span>
<span data-ttu-id="6ebd9-123">Ponto</span><span class="sxs-lookup"><span data-stu-id="6ebd9-123">Location</span></span> 

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ebd9-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="6ebd9-124">-Name</span></span>
<span data-ttu-id="6ebd9-125">Nome do plano do serviço de aplicativo</span><span class="sxs-lookup"><span data-stu-id="6ebd9-125">App Service Plan Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ebd9-126">-NumberofWorkers</span><span class="sxs-lookup"><span data-stu-id="6ebd9-126">-NumberofWorkers</span></span>
<span data-ttu-id="6ebd9-127">Número de trabalhadores</span><span class="sxs-lookup"><span data-stu-id="6ebd9-127">Number Of Workers</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: 1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ebd9-128">-PerSiteScaling</span><span class="sxs-lookup"><span data-stu-id="6ebd9-128">-PerSiteScaling</span></span>
<span data-ttu-id="6ebd9-129">Se o dimensionamento por site deve ou não ser habilitado</span><span class="sxs-lookup"><span data-stu-id="6ebd9-129">Whether or not to enable Per Site Scaling</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ebd9-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6ebd9-130">-ResourceGroupName</span></span>
<span data-ttu-id="6ebd9-131">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="6ebd9-131">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ebd9-132">-Tier</span><span class="sxs-lookup"><span data-stu-id="6ebd9-132">-Tier</span></span>
<span data-ttu-id="6ebd9-133">Hierarquiza</span><span class="sxs-lookup"><span data-stu-id="6ebd9-133">Tier</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Free, Shared, Basic, Standard, Premium, PremiumV2

Required: False
Position: 3
Default value: Free
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ebd9-134">-Trabalhadores</span><span class="sxs-lookup"><span data-stu-id="6ebd9-134">-WorkerSize</span></span>
<span data-ttu-id="6ebd9-135">Tamanho do Web Worker</span><span class="sxs-lookup"><span data-stu-id="6ebd9-135">Size of web worker</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Small, Medium, Large, ExtraLarge

Required: False
Position: 5
Default value: Small
Accept pipeline input: False
Accept wildcard characters: False
```
### <span data-ttu-id="6ebd9-136">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6ebd9-136">-AsJob</span></span>
<span data-ttu-id="6ebd9-137">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="6ebd9-137">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ebd9-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ebd9-138">CommonParameters</span></span>
<span data-ttu-id="6ebd9-139">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6ebd9-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ebd9-140">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6ebd9-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ebd9-141">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6ebd9-141">INPUTS</span></span>

### <span data-ttu-id="6ebd9-142">ServerFarmWithRichSku</span><span class="sxs-lookup"><span data-stu-id="6ebd9-142">ServerFarmWithRichSku</span></span>
<span data-ttu-id="6ebd9-143">O parâmetro ' AppServicePlan ' aceita o valor do tipo ' ServerFarmWithRichSku ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="6ebd9-143">Parameter 'AppServicePlan' accepts value of type 'ServerFarmWithRichSku' from the pipeline</span></span>

## <span data-ttu-id="6ebd9-144">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6ebd9-144">OUTPUTS</span></span>

### <span data-ttu-id="6ebd9-145">Microsoft. Azure. Management. WebSites. Models. ServerFarmWithRichSku</span><span class="sxs-lookup"><span data-stu-id="6ebd9-145">Microsoft.Azure.Management.WebSites.Models.ServerFarmWithRichSku</span></span>

## <span data-ttu-id="6ebd9-146">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6ebd9-146">NOTES</span></span>

## <span data-ttu-id="6ebd9-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6ebd9-147">RELATED LINKS</span></span>

[<span data-ttu-id="6ebd9-148">Get-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="6ebd9-148">Get-AzAppServicePlan</span></span>](./Get-AzAppServicePlan.md)

[<span data-ttu-id="6ebd9-149">Remove-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="6ebd9-149">Remove-AzAppServicePlan</span></span>](./Remove-AzAppServicePlan.md)

[<span data-ttu-id="6ebd9-150">Set-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="6ebd9-150">Set-AzAppServicePlan</span></span>](./Set-AzAppServicePlan.md)


