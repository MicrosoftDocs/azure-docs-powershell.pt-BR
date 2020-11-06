---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 32D45795-FBCD-4157-BF45-41BD1F61782E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Set-AzureRmAppServicePlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Set-AzureRmAppServicePlan.md
ms.openlocfilehash: 4b6270a6d56b8f210b2f03311bf19bb09950f361
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428227"
---
# <span data-ttu-id="94d1d-101">Set-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="94d1d-101">Set-AzureRmAppServicePlan</span></span>

## <span data-ttu-id="94d1d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="94d1d-102">SYNOPSIS</span></span>
<span data-ttu-id="94d1d-103">Define um plano do serviço de aplicativo Azure.</span><span class="sxs-lookup"><span data-stu-id="94d1d-103">Sets an Azure App Service plan.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="94d1d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="94d1d-104">SYNTAX</span></span>

### <span data-ttu-id="94d1d-105">Eles</span><span class="sxs-lookup"><span data-stu-id="94d1d-105">S1</span></span>
```
Set-AzureRmAppServicePlan [[-AdminSiteName] <String>] [[-Tier] <String>] [[-NumberofWorkers] <Int32>]
 [[-WorkerSize] <String>] [-PerSiteScaling <Boolean>] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="94d1d-106">S2</span><span class="sxs-lookup"><span data-stu-id="94d1d-106">S2</span></span>
```
Set-AzureRmAppServicePlan [-AppServicePlan] <ServerFarmWithRichSku> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="94d1d-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="94d1d-107">DESCRIPTION</span></span>
<span data-ttu-id="94d1d-108">O cmdlet **set-AzureRmAppServicePlan** define um plano do serviço de aplicativo Azure.</span><span class="sxs-lookup"><span data-stu-id="94d1d-108">The **Set-AzureRmAppServicePlan** cmdlet sets an Azure App Service plan.</span></span>

## <span data-ttu-id="94d1d-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="94d1d-109">EXAMPLES</span></span>

### <span data-ttu-id="94d1d-110">1: modificar um plano do serviço de aplicativo</span><span class="sxs-lookup"><span data-stu-id="94d1d-110">1: Modify an App Service plan</span></span>
```
PS C:\>Set-AzureRmAppServicePlan -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP" -PerSiteScaling $true
```

<span data-ttu-id="94d1d-111">Esse comando define a opção PerSiteScaling como true no plano do serviço de aplicativo chamado ContosoASP que pertence ao grupo de recursos chamado Default-Web-Oesteus.</span><span class="sxs-lookup"><span data-stu-id="94d1d-111">This command sets the PerSiteScaling option to true on the App Service plan named ContosoASP that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="94d1d-112">OS</span><span class="sxs-lookup"><span data-stu-id="94d1d-112">PARAMETERS</span></span>

### <span data-ttu-id="94d1d-113">-AdminSiteName</span><span class="sxs-lookup"><span data-stu-id="94d1d-113">-AdminSiteName</span></span>
<span data-ttu-id="94d1d-114">Nome do site de administração</span><span class="sxs-lookup"><span data-stu-id="94d1d-114">Admin Site Name</span></span>

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

### <span data-ttu-id="94d1d-115">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="94d1d-115">-AppServicePlan</span></span>
<span data-ttu-id="94d1d-116">Objeto plano do serviço de aplicativo</span><span class="sxs-lookup"><span data-stu-id="94d1d-116">App Service Plan Object</span></span>

```yaml
Type: Microsoft.Azure.Management.WebSites.Models.ServerFarmWithRichSku
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="94d1d-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="94d1d-117">-Name</span></span>
<span data-ttu-id="94d1d-118">Nome do plano do serviço de aplicativo</span><span class="sxs-lookup"><span data-stu-id="94d1d-118">App Service Plan Name</span></span>

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

### <span data-ttu-id="94d1d-119">-NumberofWorkers</span><span class="sxs-lookup"><span data-stu-id="94d1d-119">-NumberofWorkers</span></span>
<span data-ttu-id="94d1d-120">Número de trabalhadores</span><span class="sxs-lookup"><span data-stu-id="94d1d-120">Number Of Workers</span></span>

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

### <span data-ttu-id="94d1d-121">-PerSiteScaling</span><span class="sxs-lookup"><span data-stu-id="94d1d-121">-PerSiteScaling</span></span>
<span data-ttu-id="94d1d-122">Booleano de dimensionamento por site</span><span class="sxs-lookup"><span data-stu-id="94d1d-122">Per Site Scaling Boolean</span></span>

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

### <span data-ttu-id="94d1d-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="94d1d-123">-ResourceGroupName</span></span>
<span data-ttu-id="94d1d-124">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="94d1d-124">Resource Group Name</span></span>

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

### <span data-ttu-id="94d1d-125">-Tier</span><span class="sxs-lookup"><span data-stu-id="94d1d-125">-Tier</span></span>
<span data-ttu-id="94d1d-126">Hierarquiza</span><span class="sxs-lookup"><span data-stu-id="94d1d-126">Tier</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases: 
Accepted values: Free, Shared, Basic, Standard, Premium

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94d1d-127">-Trabalhadores</span><span class="sxs-lookup"><span data-stu-id="94d1d-127">-WorkerSize</span></span>
<span data-ttu-id="94d1d-128">Tamanho do trabalhador</span><span class="sxs-lookup"><span data-stu-id="94d1d-128">Worker Size</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases: 
Accepted values: Small, Medium, Large, ExtraLarge

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94d1d-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94d1d-129">-DefaultProfile</span></span>
<span data-ttu-id="94d1d-130">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="94d1d-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="94d1d-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94d1d-131">CommonParameters</span></span>
<span data-ttu-id="94d1d-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="94d1d-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94d1d-133">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="94d1d-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94d1d-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="94d1d-134">INPUTS</span></span>

### <span data-ttu-id="94d1d-135">ServerFarmWithRichSku</span><span class="sxs-lookup"><span data-stu-id="94d1d-135">ServerFarmWithRichSku</span></span>
<span data-ttu-id="94d1d-136">O parâmetro ' AppServicePlan ' aceita o valor do tipo ' ServerFarmWithRichSku ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="94d1d-136">Parameter 'AppServicePlan' accepts value of type 'ServerFarmWithRichSku' from the pipeline</span></span>

## <span data-ttu-id="94d1d-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="94d1d-137">OUTPUTS</span></span>

### <span data-ttu-id="94d1d-138">Microsoft. Azure. Management. WebSites. Models. ServerFarmWithRichSku</span><span class="sxs-lookup"><span data-stu-id="94d1d-138">Microsoft.Azure.Management.WebSites.Models.ServerFarmWithRichSku</span></span>

## <span data-ttu-id="94d1d-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="94d1d-139">NOTES</span></span>

## <span data-ttu-id="94d1d-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="94d1d-140">RELATED LINKS</span></span>

[<span data-ttu-id="94d1d-141">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="94d1d-141">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)

[<span data-ttu-id="94d1d-142">New-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="94d1d-142">New-AzureRmWebApp</span></span>](./New-AzureRmWebApp.md)

[<span data-ttu-id="94d1d-143">Remove-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="94d1d-143">Remove-AzureRmWebApp</span></span>](./Remove-AzureRmWebApp.md)

[<span data-ttu-id="94d1d-144">Restart-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="94d1d-144">Restart-AzureRmWebApp</span></span>](./Restart-AzureRmWebApp.md)

[<span data-ttu-id="94d1d-145">Start-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="94d1d-145">Start-AzureRmWebApp</span></span>](./Start-AzureRmWebApp.md)

[<span data-ttu-id="94d1d-146">Parar-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="94d1d-146">Stop-AzureRmWebApp</span></span>](./Stop-AzureRmWebApp.md)


