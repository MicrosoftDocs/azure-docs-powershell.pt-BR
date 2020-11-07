---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: 89ED4231-7616-47D0-BDAA-D849C245DC79
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/get-Azappserviceplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Get-AzAppServicePlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Get-AzAppServicePlan.md
ms.openlocfilehash: 48d37bf19ec6613ce1f42ee8cf7609bd6383e12f
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93776128"
---
# <span data-ttu-id="8ec7c-101">Get-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="8ec7c-101">Get-AzAppServicePlan</span></span>

## <span data-ttu-id="8ec7c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8ec7c-102">SYNOPSIS</span></span>
<span data-ttu-id="8ec7c-103">Obtém um plano do serviço de aplicativo do Azure no grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="8ec7c-103">Gets an Azure App Service plan in the specified resource group.</span></span>

## <span data-ttu-id="8ec7c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8ec7c-104">SYNTAX</span></span>

### <span data-ttu-id="8ec7c-105">Eles</span><span class="sxs-lookup"><span data-stu-id="8ec7c-105">S1</span></span>
```
Get-AzAppServicePlan [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8ec7c-106">S2</span><span class="sxs-lookup"><span data-stu-id="8ec7c-106">S2</span></span>
```
Get-AzAppServicePlan [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8ec7c-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8ec7c-107">DESCRIPTION</span></span>
<span data-ttu-id="8ec7c-108">O cmdlet **Get-AzAppServicePlan** Obtém um plano do serviço de aplicativo do Azure no grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="8ec7c-108">The **Get-AzAppServicePlan** cmdlet gets an Azure App Service plan in the specified resource group.</span></span>

## <span data-ttu-id="8ec7c-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8ec7c-109">EXAMPLES</span></span>

### <span data-ttu-id="8ec7c-110">Exemplo 1: obter um plano do serviço de aplicativo de um grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="8ec7c-110">Example 1: Get an App Service plan from a resource group</span></span>
```
PS C:\>Get-AzAppServicePlan -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP"
```

<span data-ttu-id="8ec7c-111">Esse comando obtém o plano do serviço de aplicativo chamado ContosoASP que pertence ao grupo de recursos chamado Default-Web-Oesteus.</span><span class="sxs-lookup"><span data-stu-id="8ec7c-111">This command gets the App Service plan named ContosoASP that belongs to the resource group named Default-Web-WestUS.</span></span>

### <span data-ttu-id="8ec7c-112">Exemplo 2: obter todos os planos do serviço de aplicativo em um local</span><span class="sxs-lookup"><span data-stu-id="8ec7c-112">Example 2: Get all App Service plans in a location</span></span>
```
PS C:\>Get-AzAppServicePlan -Location "West US"
```

<span data-ttu-id="8ec7c-113">Esse comando obtém todos os planos do serviço de aplicativo localizado na região "oeste dos EUA".</span><span class="sxs-lookup"><span data-stu-id="8ec7c-113">This command gets all App Service plans located in the "West US" region.</span></span>

## <span data-ttu-id="8ec7c-114">OS</span><span class="sxs-lookup"><span data-stu-id="8ec7c-114">PARAMETERS</span></span>

### <span data-ttu-id="8ec7c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ec7c-115">-DefaultProfile</span></span>
<span data-ttu-id="8ec7c-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8ec7c-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8ec7c-117">-Local</span><span class="sxs-lookup"><span data-stu-id="8ec7c-117">-Location</span></span>
<span data-ttu-id="8ec7c-118">Ponto</span><span class="sxs-lookup"><span data-stu-id="8ec7c-118">Location</span></span> 

```yaml
Type: String
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ec7c-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="8ec7c-119">-Name</span></span>
<span data-ttu-id="8ec7c-120">Nome do plano do serviço de aplicativo</span><span class="sxs-lookup"><span data-stu-id="8ec7c-120">App Service Plan Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ec7c-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8ec7c-121">-ResourceGroupName</span></span>
<span data-ttu-id="8ec7c-122">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="8ec7c-122">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ec7c-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ec7c-123">CommonParameters</span></span>
<span data-ttu-id="8ec7c-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8ec7c-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ec7c-125">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8ec7c-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ec7c-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8ec7c-126">INPUTS</span></span>

### <span data-ttu-id="8ec7c-127">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="8ec7c-127">None</span></span>
<span data-ttu-id="8ec7c-128">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="8ec7c-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="8ec7c-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8ec7c-129">OUTPUTS</span></span>

### <span data-ttu-id="8ec7c-130">Microsoft. Azure. Management. WebSites. Models. ServerFarmWithRichSku</span><span class="sxs-lookup"><span data-stu-id="8ec7c-130">Microsoft.Azure.Management.WebSites.Models.ServerFarmWithRichSku</span></span>

### <span data-ttu-id="8ec7c-131">Microsoft. Azure. Management. WebSites. Models. ServerFarmCollection</span><span class="sxs-lookup"><span data-stu-id="8ec7c-131">Microsoft.Azure.Management.WebSites.Models.ServerFarmCollection</span></span>

## <span data-ttu-id="8ec7c-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8ec7c-132">NOTES</span></span>

## <span data-ttu-id="8ec7c-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8ec7c-133">RELATED LINKS</span></span>

[<span data-ttu-id="8ec7c-134">New-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="8ec7c-134">New-AzAppServicePlan</span></span>](./New-AzAppServicePlan.md)

[<span data-ttu-id="8ec7c-135">Remove-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="8ec7c-135">Remove-AzAppServicePlan</span></span>](./Remove-AzAppServicePlan.md)

[<span data-ttu-id="8ec7c-136">Set-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="8ec7c-136">Set-AzAppServicePlan</span></span>](./Set-AzAppServicePlan.md)


