---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.WebSites
ms.assetid: A87ED954-9C09-4329-A005-ABFF36C45E6E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermwebapp
schema: 2.0.0
ms.openlocfilehash: eb1f96eaf85e6a5e7234e09c319b2e0c1117d456
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93785134"
---
# <span data-ttu-id="69cb5-101">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="69cb5-101">Get-AzureRmWebApp</span></span>

## <span data-ttu-id="69cb5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="69cb5-102">SYNOPSIS</span></span>
<span data-ttu-id="69cb5-103">Obtém os aplicativos Web do Azure no grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="69cb5-103">Gets Azure Web Apps in the specified resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="69cb5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="69cb5-104">SYNTAX</span></span>

### <span data-ttu-id="69cb5-105">Eles</span><span class="sxs-lookup"><span data-stu-id="69cb5-105">S1</span></span>
```
Get-AzureRmWebApp [[-ResourceGroupName] <String>] [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="69cb5-106">S2</span><span class="sxs-lookup"><span data-stu-id="69cb5-106">S2</span></span>
```
Get-AzureRmWebApp [-AppServicePlan] <AppServicePlan> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="69cb5-107">S3</span><span class="sxs-lookup"><span data-stu-id="69cb5-107">S3</span></span>
```
Get-AzureRmWebApp [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="69cb5-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="69cb5-108">DESCRIPTION</span></span>
<span data-ttu-id="69cb5-109">O cmdlet **Get-AzureRmWebApp** Obtém informações sobre um aplicativo Web do Azure.</span><span class="sxs-lookup"><span data-stu-id="69cb5-109">The **Get-AzureRmWebApp** cmdlet gets information about an Azure Web App.</span></span>

## <span data-ttu-id="69cb5-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="69cb5-110">EXAMPLES</span></span>

### <span data-ttu-id="69cb5-111">Exemplo 1: obter um aplicativo Web a partir de um grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="69cb5-111">Example 1: Get a Web App from a resource group</span></span>
```
PS C:\>Get-AzureRmWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="69cb5-112">Esse comando obtém o aplicativo Web chamado ContosoSite que pertence ao grupo de recursos Default-Web-Oesteus.</span><span class="sxs-lookup"><span data-stu-id="69cb5-112">This command gets the Web App named ContosoSite that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="69cb5-113">OS</span><span class="sxs-lookup"><span data-stu-id="69cb5-113">PARAMETERS</span></span>

### <span data-ttu-id="69cb5-114">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="69cb5-114">-AppServicePlan</span></span>
<span data-ttu-id="69cb5-115">Objeto plano do serviço de aplicativo</span><span class="sxs-lookup"><span data-stu-id="69cb5-115">App Service Plan object</span></span>

```yaml
Type: AppServicePlan
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69cb5-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69cb5-116">-DefaultProfile</span></span>
<span data-ttu-id="69cb5-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="69cb5-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69cb5-118">-Local</span><span class="sxs-lookup"><span data-stu-id="69cb5-118">-Location</span></span>
<span data-ttu-id="69cb5-119">Ponto</span><span class="sxs-lookup"><span data-stu-id="69cb5-119">Location</span></span>

```yaml
Type: String
Parameter Sets: S3
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69cb5-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="69cb5-120">-Name</span></span>
<span data-ttu-id="69cb5-121">Nome do WebApp</span><span class="sxs-lookup"><span data-stu-id="69cb5-121">WebApp Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69cb5-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="69cb5-122">-ResourceGroupName</span></span>
<span data-ttu-id="69cb5-123">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="69cb5-123">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69cb5-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69cb5-124">CommonParameters</span></span>
<span data-ttu-id="69cb5-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="69cb5-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69cb5-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="69cb5-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69cb5-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="69cb5-127">INPUTS</span></span>

### <span data-ttu-id="69cb5-128">System. String</span><span class="sxs-lookup"><span data-stu-id="69cb5-128">System.String</span></span>

## <span data-ttu-id="69cb5-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="69cb5-129">OUTPUTS</span></span>

### <span data-ttu-id="69cb5-130">Microsoft. Azure. Management. WebSites. Models. site</span><span class="sxs-lookup"><span data-stu-id="69cb5-130">Microsoft.Azure.Management.WebSites.Models.Site</span></span>

## <span data-ttu-id="69cb5-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="69cb5-131">NOTES</span></span>

## <span data-ttu-id="69cb5-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="69cb5-132">RELATED LINKS</span></span>

[<span data-ttu-id="69cb5-133">New-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="69cb5-133">New-AzureRmWebApp</span></span>](./New-AzureRmWebApp.md)

[<span data-ttu-id="69cb5-134">Remove-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="69cb5-134">Remove-AzureRmWebApp</span></span>](./Remove-AzureRmWebApp.md)

[<span data-ttu-id="69cb5-135">Restart-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="69cb5-135">Restart-AzureRmWebApp</span></span>](./Restart-AzureRmWebApp.md)

[<span data-ttu-id="69cb5-136">Start-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="69cb5-136">Start-AzureRmWebApp</span></span>](./Start-AzureRmWebApp.md)

[<span data-ttu-id="69cb5-137">Parar-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="69cb5-137">Stop-AzureRmWebApp</span></span>](./Stop-AzureRmWebApp.md)


