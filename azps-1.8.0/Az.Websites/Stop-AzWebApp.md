---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: A12FFDB1-9849-4150-9716-068BE6EFC681
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/stop-azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Stop-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Stop-AzWebApp.md
ms.openlocfilehash: 28a6399db8f896d60c48d62d69ca75c5d85c25c7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93598285"
---
# <span data-ttu-id="63693-101">Stop-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="63693-101">Stop-AzWebApp</span></span>

## <span data-ttu-id="63693-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="63693-102">SYNOPSIS</span></span>
<span data-ttu-id="63693-103">Interrompe um aplicativo Web do Azure.</span><span class="sxs-lookup"><span data-stu-id="63693-103">Stops an Azure Web App.</span></span>

## <span data-ttu-id="63693-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="63693-104">SYNTAX</span></span>

### <span data-ttu-id="63693-105">Eles</span><span class="sxs-lookup"><span data-stu-id="63693-105">S1</span></span>
```
Stop-AzWebApp [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="63693-106">S2</span><span class="sxs-lookup"><span data-stu-id="63693-106">S2</span></span>
```
Stop-AzWebApp [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="63693-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="63693-107">DESCRIPTION</span></span>
<span data-ttu-id="63693-108">O cmdlet **Stop-AzWebApp** interrompe um aplicativo Web do Azure.</span><span class="sxs-lookup"><span data-stu-id="63693-108">The **Stop-AzWebApp** cmdlet stops an Azure Web App.</span></span>

## <span data-ttu-id="63693-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="63693-109">EXAMPLES</span></span>

### <span data-ttu-id="63693-110">Exemplo 1: parar um aplicativo Web</span><span class="sxs-lookup"><span data-stu-id="63693-110">Example 1: Stop a Web App</span></span>
```
PS C:\>Stop-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp"
```

<span data-ttu-id="63693-111">Esse comando interrompe o aplicativo Web chamado ContosoWebApp que pertence ao grupo de recursos chamado Default-Web-Oesteus.</span><span class="sxs-lookup"><span data-stu-id="63693-111">This command stops the Web App named ContosoWebApp that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="63693-112">OS</span><span class="sxs-lookup"><span data-stu-id="63693-112">PARAMETERS</span></span>

### <span data-ttu-id="63693-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63693-113">-DefaultProfile</span></span>
<span data-ttu-id="63693-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="63693-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="63693-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="63693-115">-Name</span></span>
<span data-ttu-id="63693-116">Nome do WebApp</span><span class="sxs-lookup"><span data-stu-id="63693-116">WebApp Name</span></span>

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

### <span data-ttu-id="63693-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="63693-117">-ResourceGroupName</span></span>
<span data-ttu-id="63693-118">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="63693-118">Resource Group Name</span></span>

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

### <span data-ttu-id="63693-119">-WebApp</span><span class="sxs-lookup"><span data-stu-id="63693-119">-WebApp</span></span>
<span data-ttu-id="63693-120">Objeto WebApp</span><span class="sxs-lookup"><span data-stu-id="63693-120">WebApp Object</span></span>

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

### <span data-ttu-id="63693-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63693-121">CommonParameters</span></span>
<span data-ttu-id="63693-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="63693-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63693-123">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="63693-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63693-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="63693-124">INPUTS</span></span>

### <span data-ttu-id="63693-125">System. String</span><span class="sxs-lookup"><span data-stu-id="63693-125">System.String</span></span>

### <span data-ttu-id="63693-126">Microsoft. Azure. Commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="63693-126">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="63693-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="63693-127">OUTPUTS</span></span>

### <span data-ttu-id="63693-128">Microsoft. Azure. Commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="63693-128">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="63693-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="63693-129">NOTES</span></span>

## <span data-ttu-id="63693-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="63693-130">RELATED LINKS</span></span>

[<span data-ttu-id="63693-131">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="63693-131">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="63693-132">New-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="63693-132">New-AzWebApp</span></span>](./New-AzWebApp.md)

[<span data-ttu-id="63693-133">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="63693-133">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)

[<span data-ttu-id="63693-134">Restart-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="63693-134">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="63693-135">Start-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="63693-135">Start-AzWebApp</span></span>](./Start-AzWebApp.md)


