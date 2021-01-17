---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: D70A61D8-0C9A-4BDB-A546-37C32D25797C
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/start-azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Start-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Start-AzWebApp.md
ms.openlocfilehash: 33fdfdc1c8b0c4b7bfddbc6b0aafd9ab38ffe701
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98427761"
---
# <span data-ttu-id="e2868-101">Start-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="e2868-101">Start-AzWebApp</span></span>

## <span data-ttu-id="e2868-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e2868-102">SYNOPSIS</span></span>
<span data-ttu-id="e2868-103">Inicia um aplicativo Web do Azure.</span><span class="sxs-lookup"><span data-stu-id="e2868-103">Starts an Azure Web App.</span></span>

## <span data-ttu-id="e2868-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e2868-104">SYNTAX</span></span>

### <span data-ttu-id="e2868-105">Eles</span><span class="sxs-lookup"><span data-stu-id="e2868-105">S1</span></span>
```
Start-AzWebApp [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e2868-106">S2</span><span class="sxs-lookup"><span data-stu-id="e2868-106">S2</span></span>
```
Start-AzWebApp [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e2868-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e2868-107">DESCRIPTION</span></span>
<span data-ttu-id="e2868-108">O cmdlet **Start-AzWebApp** inicia um aplicativo Web do Azure.</span><span class="sxs-lookup"><span data-stu-id="e2868-108">The **Start-AzWebApp** cmdlet starts an Azure Web App.</span></span>

## <span data-ttu-id="e2868-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e2868-109">EXAMPLES</span></span>

### <span data-ttu-id="e2868-110">Exemplo 1: iniciar um aplicativo Web</span><span class="sxs-lookup"><span data-stu-id="e2868-110">Example 1: Start a Web App</span></span>
```
PS C:\>Start-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp"
```

<span data-ttu-id="e2868-111">Esse comando inicia o aplicativo Web chamado ContosoWebApp que pertence ao grupo de recursos chamado Default-Web-Oesteus.</span><span class="sxs-lookup"><span data-stu-id="e2868-111">This command starts the Web App named ContosoWebApp that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="e2868-112">OS</span><span class="sxs-lookup"><span data-stu-id="e2868-112">PARAMETERS</span></span>

### <span data-ttu-id="e2868-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2868-113">-DefaultProfile</span></span>
<span data-ttu-id="e2868-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e2868-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e2868-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="e2868-115">-Name</span></span>
<span data-ttu-id="e2868-116">Nome do WebApp</span><span class="sxs-lookup"><span data-stu-id="e2868-116">WebApp Name</span></span>

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

### <span data-ttu-id="e2868-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e2868-117">-ResourceGroupName</span></span>
<span data-ttu-id="e2868-118">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="e2868-118">Resource Group Name</span></span>

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

### <span data-ttu-id="e2868-119">-WebApp</span><span class="sxs-lookup"><span data-stu-id="e2868-119">-WebApp</span></span>
<span data-ttu-id="e2868-120">Objeto WebApp</span><span class="sxs-lookup"><span data-stu-id="e2868-120">WebApp Object</span></span>

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

### <span data-ttu-id="e2868-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2868-121">CommonParameters</span></span>
<span data-ttu-id="e2868-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e2868-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2868-123">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e2868-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2868-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e2868-124">INPUTS</span></span>

### <span data-ttu-id="e2868-125">System. String</span><span class="sxs-lookup"><span data-stu-id="e2868-125">System.String</span></span>

### <span data-ttu-id="e2868-126">Microsoft. Azure. Commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="e2868-126">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="e2868-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e2868-127">OUTPUTS</span></span>

### <span data-ttu-id="e2868-128">Microsoft. Azure. Commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="e2868-128">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="e2868-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e2868-129">NOTES</span></span>

## <span data-ttu-id="e2868-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e2868-130">RELATED LINKS</span></span>

[<span data-ttu-id="e2868-131">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="e2868-131">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="e2868-132">New-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="e2868-132">New-AzWebApp</span></span>](./New-AzWebApp.md)

[<span data-ttu-id="e2868-133">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="e2868-133">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)

[<span data-ttu-id="e2868-134">Restart-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="e2868-134">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="e2868-135">Parar-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="e2868-135">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)


