---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: A12FFDB1-9849-4150-9716-068BE6EFC681
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/stop-azurermwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Stop-AzureRmWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Stop-AzureRmWebApp.md
ms.openlocfilehash: b389a84ea57902e2e7a7dabaea2d853827a728e1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427080"
---
# <span data-ttu-id="254f5-101">Stop-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="254f5-101">Stop-AzureRmWebApp</span></span>

## <span data-ttu-id="254f5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="254f5-102">SYNOPSIS</span></span>
<span data-ttu-id="254f5-103">Interrompe um aplicativo Web do Azure.</span><span class="sxs-lookup"><span data-stu-id="254f5-103">Stops an Azure Web App.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="254f5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="254f5-104">SYNTAX</span></span>

### <span data-ttu-id="254f5-105">Eles</span><span class="sxs-lookup"><span data-stu-id="254f5-105">S1</span></span>
```
Stop-AzureRmWebApp [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="254f5-106">S2</span><span class="sxs-lookup"><span data-stu-id="254f5-106">S2</span></span>
```
Stop-AzureRmWebApp [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="254f5-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="254f5-107">DESCRIPTION</span></span>
<span data-ttu-id="254f5-108">O cmdlet **Stop-AzureRmWebApp** interrompe um aplicativo Web do Azure.</span><span class="sxs-lookup"><span data-stu-id="254f5-108">The **Stop-AzureRmWebApp** cmdlet stops an Azure Web App.</span></span>

## <span data-ttu-id="254f5-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="254f5-109">EXAMPLES</span></span>

### <span data-ttu-id="254f5-110">Exemplo 1: parar um aplicativo Web</span><span class="sxs-lookup"><span data-stu-id="254f5-110">Example 1: Stop a Web App</span></span>
```
PS C:\>Stop-AzureRmWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp"
```

<span data-ttu-id="254f5-111">Esse comando interrompe o aplicativo Web chamado ContosoWebApp que pertence ao grupo de recursos chamado Default-Web-Oesteus.</span><span class="sxs-lookup"><span data-stu-id="254f5-111">This command stops the Web App named ContosoWebApp that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="254f5-112">OS</span><span class="sxs-lookup"><span data-stu-id="254f5-112">PARAMETERS</span></span>

### <span data-ttu-id="254f5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="254f5-113">-DefaultProfile</span></span>
<span data-ttu-id="254f5-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="254f5-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="254f5-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="254f5-115">-Name</span></span>
<span data-ttu-id="254f5-116">Nome do WebApp</span><span class="sxs-lookup"><span data-stu-id="254f5-116">WebApp Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="254f5-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="254f5-117">-ResourceGroupName</span></span>
<span data-ttu-id="254f5-118">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="254f5-118">Resource Group Name</span></span>

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

### <span data-ttu-id="254f5-119">-WebApp</span><span class="sxs-lookup"><span data-stu-id="254f5-119">-WebApp</span></span>
<span data-ttu-id="254f5-120">Objeto WebApp</span><span class="sxs-lookup"><span data-stu-id="254f5-120">WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: S2
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="254f5-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="254f5-121">CommonParameters</span></span>
<span data-ttu-id="254f5-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="254f5-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="254f5-123">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="254f5-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="254f5-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="254f5-124">INPUTS</span></span>

### <span data-ttu-id="254f5-125">System. String</span><span class="sxs-lookup"><span data-stu-id="254f5-125">System.String</span></span>

### <span data-ttu-id="254f5-126">Microsoft. Azure. Management. WebSites. Models. site</span><span class="sxs-lookup"><span data-stu-id="254f5-126">Microsoft.Azure.Management.WebSites.Models.Site</span></span>
<span data-ttu-id="254f5-127">Parâmetros: WebApp (ByValue)</span><span class="sxs-lookup"><span data-stu-id="254f5-127">Parameters: WebApp (ByValue)</span></span>

## <span data-ttu-id="254f5-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="254f5-128">OUTPUTS</span></span>

### <span data-ttu-id="254f5-129">Microsoft. Azure. Management. WebSites. Models. site</span><span class="sxs-lookup"><span data-stu-id="254f5-129">Microsoft.Azure.Management.WebSites.Models.Site</span></span>

## <span data-ttu-id="254f5-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="254f5-130">NOTES</span></span>

## <span data-ttu-id="254f5-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="254f5-131">RELATED LINKS</span></span>

[<span data-ttu-id="254f5-132">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="254f5-132">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)

[<span data-ttu-id="254f5-133">New-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="254f5-133">New-AzureRmWebApp</span></span>](./New-AzureRmWebApp.md)

[<span data-ttu-id="254f5-134">Remove-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="254f5-134">Remove-AzureRmWebApp</span></span>](./Remove-AzureRmWebApp.md)

[<span data-ttu-id="254f5-135">Restart-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="254f5-135">Restart-AzureRmWebApp</span></span>](./Restart-AzureRmWebApp.md)

[<span data-ttu-id="254f5-136">Start-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="254f5-136">Start-AzureRmWebApp</span></span>](./Start-AzureRmWebApp.md)


