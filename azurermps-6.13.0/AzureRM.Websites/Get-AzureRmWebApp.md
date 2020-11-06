---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: A87ED954-9C09-4329-A005-ABFF36C45E6E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebApp.md
ms.openlocfilehash: 83afdb179a9c0f135fd17827ff59f89ad117e3b5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430790"
---
# <span data-ttu-id="c175a-101">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="c175a-101">Get-AzureRmWebApp</span></span>

## <span data-ttu-id="c175a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c175a-102">SYNOPSIS</span></span>
<span data-ttu-id="c175a-103">Obtém os aplicativos Web do Azure no grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="c175a-103">Gets Azure Web Apps in the specified resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c175a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c175a-104">SYNTAX</span></span>

### <span data-ttu-id="c175a-105">Eles</span><span class="sxs-lookup"><span data-stu-id="c175a-105">S1</span></span>
```
Get-AzureRmWebApp [[-ResourceGroupName] <String>] [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c175a-106">S2</span><span class="sxs-lookup"><span data-stu-id="c175a-106">S2</span></span>
```
Get-AzureRmWebApp [-AppServicePlan] <PSAppServicePlan> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c175a-107">S3</span><span class="sxs-lookup"><span data-stu-id="c175a-107">S3</span></span>
```
Get-AzureRmWebApp [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c175a-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c175a-108">DESCRIPTION</span></span>
<span data-ttu-id="c175a-109">O cmdlet **Get-AzureRmWebApp** Obtém informações sobre um aplicativo Web do Azure.</span><span class="sxs-lookup"><span data-stu-id="c175a-109">The **Get-AzureRmWebApp** cmdlet gets information about an Azure Web App.</span></span>

## <span data-ttu-id="c175a-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c175a-110">EXAMPLES</span></span>

### <span data-ttu-id="c175a-111">Exemplo 1: obter um aplicativo Web a partir de um grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="c175a-111">Example 1: Get a Web App from a resource group</span></span>
```
PS C:\>Get-AzureRmWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="c175a-112">Esse comando obtém o aplicativo Web chamado ContosoSite que pertence ao grupo de recursos Default-Web-Oesteus.</span><span class="sxs-lookup"><span data-stu-id="c175a-112">This command gets the Web App named ContosoSite that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="c175a-113">OS</span><span class="sxs-lookup"><span data-stu-id="c175a-113">PARAMETERS</span></span>

### <span data-ttu-id="c175a-114">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="c175a-114">-AppServicePlan</span></span>
<span data-ttu-id="c175a-115">Objeto plano do serviço de aplicativo</span><span class="sxs-lookup"><span data-stu-id="c175a-115">App Service Plan object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.WebApp.PSAppServicePlan
Parameter Sets: S2
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c175a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c175a-116">-DefaultProfile</span></span>
<span data-ttu-id="c175a-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c175a-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c175a-118">-Local</span><span class="sxs-lookup"><span data-stu-id="c175a-118">-Location</span></span>
<span data-ttu-id="c175a-119">Ponto</span><span class="sxs-lookup"><span data-stu-id="c175a-119">Location</span></span>

```yaml
Type: System.String
Parameter Sets: S3
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c175a-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="c175a-120">-Name</span></span>
<span data-ttu-id="c175a-121">Nome do WebApp</span><span class="sxs-lookup"><span data-stu-id="c175a-121">WebApp Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c175a-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c175a-122">-ResourceGroupName</span></span>
<span data-ttu-id="c175a-123">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="c175a-123">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c175a-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c175a-124">CommonParameters</span></span>
<span data-ttu-id="c175a-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c175a-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c175a-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c175a-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c175a-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c175a-127">INPUTS</span></span>

### <span data-ttu-id="c175a-128">System. String</span><span class="sxs-lookup"><span data-stu-id="c175a-128">System.String</span></span>

## <span data-ttu-id="c175a-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c175a-129">OUTPUTS</span></span>

### <span data-ttu-id="c175a-130">Microsoft. Azure. Management. WebSites. Models. site</span><span class="sxs-lookup"><span data-stu-id="c175a-130">Microsoft.Azure.Management.WebSites.Models.Site</span></span>

## <span data-ttu-id="c175a-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c175a-131">NOTES</span></span>

## <span data-ttu-id="c175a-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c175a-132">RELATED LINKS</span></span>

[<span data-ttu-id="c175a-133">New-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="c175a-133">New-AzureRmWebApp</span></span>](./New-AzureRmWebApp.md)

[<span data-ttu-id="c175a-134">Remove-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="c175a-134">Remove-AzureRmWebApp</span></span>](./Remove-AzureRmWebApp.md)

[<span data-ttu-id="c175a-135">Restart-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="c175a-135">Restart-AzureRmWebApp</span></span>](./Restart-AzureRmWebApp.md)

[<span data-ttu-id="c175a-136">Start-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="c175a-136">Start-AzureRmWebApp</span></span>](./Start-AzureRmWebApp.md)

[<span data-ttu-id="c175a-137">Parar-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="c175a-137">Stop-AzureRmWebApp</span></span>](./Stop-AzureRmWebApp.md)


