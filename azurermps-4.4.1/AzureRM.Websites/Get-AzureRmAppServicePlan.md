---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 89ED4231-7616-47D0-BDAA-D849C245DC79
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmAppServicePlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmAppServicePlan.md
ms.openlocfilehash: 9cadc32a34f94a29221984e25141bcc3a844de4d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93603079"
---
# <span data-ttu-id="ccbaf-101">Get-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="ccbaf-101">Get-AzureRmAppServicePlan</span></span>

## <span data-ttu-id="ccbaf-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ccbaf-102">SYNOPSIS</span></span>
<span data-ttu-id="ccbaf-103">Obtém um plano do serviço de aplicativo do Azure no grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="ccbaf-103">Gets an Azure App Service plan in the specified resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ccbaf-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ccbaf-104">SYNTAX</span></span>

### <span data-ttu-id="ccbaf-105">Eles</span><span class="sxs-lookup"><span data-stu-id="ccbaf-105">S1</span></span>
```
Get-AzureRmAppServicePlan [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ccbaf-106">S2</span><span class="sxs-lookup"><span data-stu-id="ccbaf-106">S2</span></span>
```
Get-AzureRmAppServicePlan [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ccbaf-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ccbaf-107">DESCRIPTION</span></span>
<span data-ttu-id="ccbaf-108">O cmdlet **Get-AzureRmAppServicePlan** Obtém um plano do serviço de aplicativo do Azure no grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="ccbaf-108">The **Get-AzureRmAppServicePlan** cmdlet gets an Azure App Service plan in the specified resource group.</span></span>

## <span data-ttu-id="ccbaf-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ccbaf-109">EXAMPLES</span></span>

### <span data-ttu-id="ccbaf-110">Exemplo 1: obter um plano do serviço de aplicativo de um grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="ccbaf-110">Example 1: Get an App Service plan from a resource group</span></span>
```
PS C:\>Get-AzureRmAppServicePlan -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP"
```

<span data-ttu-id="ccbaf-111">Esse comando obtém o plano do serviço de aplicativo chamado ContosoASP que pertence ao grupo de recursos chamado Default-Web-Oesteus.</span><span class="sxs-lookup"><span data-stu-id="ccbaf-111">This command gets the App Service plan named ContosoASP that belongs to the resource group named Default-Web-WestUS.</span></span>

### <span data-ttu-id="ccbaf-112">Exemplo 2: obter todos os planos do serviço de aplicativo em um local</span><span class="sxs-lookup"><span data-stu-id="ccbaf-112">Example 2: Get all App Service plans in a location</span></span>
```
PS C:\>Get-AzureRmAppServicePlan -Location "West US"
```

<span data-ttu-id="ccbaf-113">Esse comando obtém todos os planos do serviço de aplicativo localizado na região "oeste dos EUA".</span><span class="sxs-lookup"><span data-stu-id="ccbaf-113">This command gets all App Service plans located in the "West US" region.</span></span>

## <span data-ttu-id="ccbaf-114">OS</span><span class="sxs-lookup"><span data-stu-id="ccbaf-114">PARAMETERS</span></span>

### <span data-ttu-id="ccbaf-115">-Local</span><span class="sxs-lookup"><span data-stu-id="ccbaf-115">-Location</span></span>
<span data-ttu-id="ccbaf-116">Ponto</span><span class="sxs-lookup"><span data-stu-id="ccbaf-116">Location</span></span> 

```yaml
Type: System.String
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ccbaf-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="ccbaf-117">-Name</span></span>
<span data-ttu-id="ccbaf-118">Nome do plano do serviço de aplicativo</span><span class="sxs-lookup"><span data-stu-id="ccbaf-118">App Service Plan Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ccbaf-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ccbaf-119">-ResourceGroupName</span></span>
<span data-ttu-id="ccbaf-120">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="ccbaf-120">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ccbaf-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ccbaf-121">-DefaultProfile</span></span>
<span data-ttu-id="ccbaf-122">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ccbaf-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ccbaf-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ccbaf-123">CommonParameters</span></span>
<span data-ttu-id="ccbaf-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ccbaf-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ccbaf-125">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ccbaf-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ccbaf-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ccbaf-126">INPUTS</span></span>

## <span data-ttu-id="ccbaf-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ccbaf-127">OUTPUTS</span></span>

### <span data-ttu-id="ccbaf-128">Microsoft. Azure. Management. WebSites. Models. ServerFarmWithRichSku</span><span class="sxs-lookup"><span data-stu-id="ccbaf-128">Microsoft.Azure.Management.WebSites.Models.ServerFarmWithRichSku</span></span>

### <span data-ttu-id="ccbaf-129">Microsoft. Azure. Management. WebSites. Models. ServerFarmCollection</span><span class="sxs-lookup"><span data-stu-id="ccbaf-129">Microsoft.Azure.Management.WebSites.Models.ServerFarmCollection</span></span>

## <span data-ttu-id="ccbaf-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ccbaf-130">NOTES</span></span>

## <span data-ttu-id="ccbaf-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ccbaf-131">RELATED LINKS</span></span>

[<span data-ttu-id="ccbaf-132">New-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="ccbaf-132">New-AzureRmAppServicePlan</span></span>](./New-AzureRmAppServicePlan.md)

[<span data-ttu-id="ccbaf-133">Remove-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="ccbaf-133">Remove-AzureRmAppServicePlan</span></span>](./Remove-AzureRmAppServicePlan.md)

[<span data-ttu-id="ccbaf-134">Set-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="ccbaf-134">Set-AzureRmAppServicePlan</span></span>](./Set-AzureRmAppServicePlan.md)


