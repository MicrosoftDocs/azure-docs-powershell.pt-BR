---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: 32D45795-FBCD-4157-BF45-41BD1F61782E
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/set-Azappserviceplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Set-AzAppServicePlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Set-AzAppServicePlan.md
ms.openlocfilehash: b679b98e84f389e35e7dc291822049e554d40a9a
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93776063"
---
# <span data-ttu-id="b1eb8-101">Set-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="b1eb8-101">Set-AzAppServicePlan</span></span>

## <span data-ttu-id="b1eb8-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b1eb8-102">SYNOPSIS</span></span>
<span data-ttu-id="b1eb8-103">Define um plano do serviço de aplicativo Azure.</span><span class="sxs-lookup"><span data-stu-id="b1eb8-103">Sets an Azure App Service plan.</span></span>

## <span data-ttu-id="b1eb8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b1eb8-104">SYNTAX</span></span>

### <span data-ttu-id="b1eb8-105">Eles</span><span class="sxs-lookup"><span data-stu-id="b1eb8-105">S1</span></span>
```
Set-AzAppServicePlan [[-AdminSiteName] <String>] [[-Tier] <String>] [[-NumberofWorkers] <Int32>]
 [[-WorkerSize] <String>] [-PerSiteScaling <Boolean>] [-ResourceGroupName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b1eb8-106">S2</span><span class="sxs-lookup"><span data-stu-id="b1eb8-106">S2</span></span>
```
Set-AzAppServicePlan [-AppServicePlan] <AppServicePlan> [-AsJob]
[-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b1eb8-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b1eb8-107">DESCRIPTION</span></span>
<span data-ttu-id="b1eb8-108">O cmdlet **set-AzAppServicePlan** define um plano do serviço de aplicativo Azure.</span><span class="sxs-lookup"><span data-stu-id="b1eb8-108">The **Set-AzAppServicePlan** cmdlet sets an Azure App Service plan.</span></span>

## <span data-ttu-id="b1eb8-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b1eb8-109">EXAMPLES</span></span>

### <span data-ttu-id="b1eb8-110">1: modificar um plano do serviço de aplicativo</span><span class="sxs-lookup"><span data-stu-id="b1eb8-110">1: Modify an App Service plan</span></span>
```
PS C:\>Set-AzAppServicePlan -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP" -PerSiteScaling $true
```

<span data-ttu-id="b1eb8-111">Esse comando define a opção PerSiteScaling como true no plano do serviço de aplicativo chamado ContosoASP que pertence ao grupo de recursos chamado Default-Web-Oesteus.</span><span class="sxs-lookup"><span data-stu-id="b1eb8-111">This command sets the PerSiteScaling option to true on the App Service plan named ContosoASP that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="b1eb8-112">OS</span><span class="sxs-lookup"><span data-stu-id="b1eb8-112">PARAMETERS</span></span>

### <span data-ttu-id="b1eb8-113">-AdminSiteName</span><span class="sxs-lookup"><span data-stu-id="b1eb8-113">-AdminSiteName</span></span>
<span data-ttu-id="b1eb8-114">Nome do site de administração</span><span class="sxs-lookup"><span data-stu-id="b1eb8-114">Admin Site Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1eb8-115">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="b1eb8-115">-AppServicePlan</span></span>
<span data-ttu-id="b1eb8-116">Objeto plano do serviço de aplicativo</span><span class="sxs-lookup"><span data-stu-id="b1eb8-116">App Service Plan Object</span></span>

```yaml
Type: AppServicePlan
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b1eb8-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1eb8-117">-DefaultProfile</span></span>
<span data-ttu-id="b1eb8-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b1eb8-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b1eb8-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="b1eb8-119">-Name</span></span>
<span data-ttu-id="b1eb8-120">Nome do plano do serviço de aplicativo</span><span class="sxs-lookup"><span data-stu-id="b1eb8-120">App Service Plan Name</span></span>

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

### <span data-ttu-id="b1eb8-121">-NumberofWorkers</span><span class="sxs-lookup"><span data-stu-id="b1eb8-121">-NumberofWorkers</span></span>
<span data-ttu-id="b1eb8-122">Número de trabalhadores</span><span class="sxs-lookup"><span data-stu-id="b1eb8-122">Number Of Workers</span></span>

```yaml
Type: Int32
Parameter Sets: S1
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1eb8-123">-PerSiteScaling</span><span class="sxs-lookup"><span data-stu-id="b1eb8-123">-PerSiteScaling</span></span>
<span data-ttu-id="b1eb8-124">Booleano de dimensionamento por site</span><span class="sxs-lookup"><span data-stu-id="b1eb8-124">Per Site Scaling Boolean</span></span>

```yaml
Type: Boolean
Parameter Sets: S1
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1eb8-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b1eb8-125">-ResourceGroupName</span></span>
<span data-ttu-id="b1eb8-126">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="b1eb8-126">Resource Group Name</span></span>

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

### <span data-ttu-id="b1eb8-127">-Tier</span><span class="sxs-lookup"><span data-stu-id="b1eb8-127">-Tier</span></span>
<span data-ttu-id="b1eb8-128">Hierarquiza</span><span class="sxs-lookup"><span data-stu-id="b1eb8-128">Tier</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 
Accepted values: Free, Shared, Basic, Standard, Premium, PremiumV2

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1eb8-129">-Trabalhadores</span><span class="sxs-lookup"><span data-stu-id="b1eb8-129">-WorkerSize</span></span>
<span data-ttu-id="b1eb8-130">Tamanho do trabalhador</span><span class="sxs-lookup"><span data-stu-id="b1eb8-130">Worker Size</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 
Accepted values: Small, Medium, Large, ExtraLarge

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```
### <span data-ttu-id="b1eb8-131">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b1eb8-131">-AsJob</span></span>
<span data-ttu-id="b1eb8-132">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="b1eb8-132">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b1eb8-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1eb8-133">CommonParameters</span></span>
<span data-ttu-id="b1eb8-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b1eb8-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1eb8-135">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b1eb8-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1eb8-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b1eb8-136">INPUTS</span></span>

### <span data-ttu-id="b1eb8-137">ServerFarmWithRichSku</span><span class="sxs-lookup"><span data-stu-id="b1eb8-137">ServerFarmWithRichSku</span></span>
<span data-ttu-id="b1eb8-138">O parâmetro ' AppServicePlan ' aceita o valor do tipo ' ServerFarmWithRichSku ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="b1eb8-138">Parameter 'AppServicePlan' accepts value of type 'ServerFarmWithRichSku' from the pipeline</span></span>

## <span data-ttu-id="b1eb8-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b1eb8-139">OUTPUTS</span></span>

### <span data-ttu-id="b1eb8-140">Microsoft. Azure. Management. WebSites. Models. ServerFarmWithRichSku</span><span class="sxs-lookup"><span data-stu-id="b1eb8-140">Microsoft.Azure.Management.WebSites.Models.ServerFarmWithRichSku</span></span>

## <span data-ttu-id="b1eb8-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b1eb8-141">NOTES</span></span>

## <span data-ttu-id="b1eb8-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b1eb8-142">RELATED LINKS</span></span>

[<span data-ttu-id="b1eb8-143">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="b1eb8-143">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="b1eb8-144">New-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="b1eb8-144">New-AzWebApp</span></span>](./New-AzWebApp.md)

[<span data-ttu-id="b1eb8-145">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="b1eb8-145">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)

[<span data-ttu-id="b1eb8-146">Restart-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="b1eb8-146">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="b1eb8-147">Start-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="b1eb8-147">Start-AzWebApp</span></span>](./Start-AzWebApp.md)

[<span data-ttu-id="b1eb8-148">Parar-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="b1eb8-148">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)


