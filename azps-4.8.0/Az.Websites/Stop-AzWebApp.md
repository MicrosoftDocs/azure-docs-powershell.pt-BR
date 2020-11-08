---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: A12FFDB1-9849-4150-9716-068BE6EFC681
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/stop-azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Stop-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Stop-AzWebApp.md
ms.openlocfilehash: d08303ec0057a42569455c9e52c38e561de73e4d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94114651"
---
# <span data-ttu-id="cf006-101">Stop-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="cf006-101">Stop-AzWebApp</span></span>

## <span data-ttu-id="cf006-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="cf006-102">SYNOPSIS</span></span>
<span data-ttu-id="cf006-103">Interrompe um aplicativo Web do Azure.</span><span class="sxs-lookup"><span data-stu-id="cf006-103">Stops an Azure Web App.</span></span>

## <span data-ttu-id="cf006-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="cf006-104">SYNTAX</span></span>

### <span data-ttu-id="cf006-105">Eles</span><span class="sxs-lookup"><span data-stu-id="cf006-105">S1</span></span>
```
Stop-AzWebApp [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="cf006-106">S2</span><span class="sxs-lookup"><span data-stu-id="cf006-106">S2</span></span>
```
Stop-AzWebApp [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cf006-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="cf006-107">DESCRIPTION</span></span>
<span data-ttu-id="cf006-108">O cmdlet **Stop-AzWebApp** interrompe um aplicativo Web do Azure.</span><span class="sxs-lookup"><span data-stu-id="cf006-108">The **Stop-AzWebApp** cmdlet stops an Azure Web App.</span></span>

## <span data-ttu-id="cf006-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="cf006-109">EXAMPLES</span></span>

### <span data-ttu-id="cf006-110">Exemplo 1: parar um aplicativo Web</span><span class="sxs-lookup"><span data-stu-id="cf006-110">Example 1: Stop a Web App</span></span>
```
PS C:\>Stop-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp"
```

<span data-ttu-id="cf006-111">Esse comando interrompe o aplicativo Web chamado ContosoWebApp que pertence ao grupo de recursos chamado Default-Web-Oesteus.</span><span class="sxs-lookup"><span data-stu-id="cf006-111">This command stops the Web App named ContosoWebApp that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="cf006-112">OS</span><span class="sxs-lookup"><span data-stu-id="cf006-112">PARAMETERS</span></span>

### <span data-ttu-id="cf006-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf006-113">-DefaultProfile</span></span>
<span data-ttu-id="cf006-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="cf006-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cf006-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="cf006-115">-Name</span></span>
<span data-ttu-id="cf006-116">Nome do WebApp</span><span class="sxs-lookup"><span data-stu-id="cf006-116">WebApp Name</span></span>

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

### <span data-ttu-id="cf006-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cf006-117">-ResourceGroupName</span></span>
<span data-ttu-id="cf006-118">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="cf006-118">Resource Group Name</span></span>

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

### <span data-ttu-id="cf006-119">-WebApp</span><span class="sxs-lookup"><span data-stu-id="cf006-119">-WebApp</span></span>
<span data-ttu-id="cf006-120">Objeto WebApp</span><span class="sxs-lookup"><span data-stu-id="cf006-120">WebApp Object</span></span>

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

### <span data-ttu-id="cf006-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf006-121">CommonParameters</span></span>
<span data-ttu-id="cf006-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cf006-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf006-123">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cf006-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf006-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="cf006-124">INPUTS</span></span>

### <span data-ttu-id="cf006-125">System. String</span><span class="sxs-lookup"><span data-stu-id="cf006-125">System.String</span></span>

### <span data-ttu-id="cf006-126">Microsoft. Azure. Commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="cf006-126">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="cf006-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="cf006-127">OUTPUTS</span></span>

### <span data-ttu-id="cf006-128">Microsoft. Azure. Commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="cf006-128">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="cf006-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="cf006-129">NOTES</span></span>

## <span data-ttu-id="cf006-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="cf006-130">RELATED LINKS</span></span>

[<span data-ttu-id="cf006-131">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="cf006-131">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="cf006-132">New-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="cf006-132">New-AzWebApp</span></span>](./New-AzWebApp.md)

[<span data-ttu-id="cf006-133">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="cf006-133">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)

[<span data-ttu-id="cf006-134">Restart-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="cf006-134">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="cf006-135">Start-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="cf006-135">Start-AzWebApp</span></span>](./Start-AzWebApp.md)


