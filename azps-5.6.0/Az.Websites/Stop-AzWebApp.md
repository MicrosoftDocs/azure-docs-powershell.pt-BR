---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: A12FFDB1-9849-4150-9716-068BE6EFC681
online version: https://docs.microsoft.com/powershell/module/az.websites/stop-azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Stop-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Stop-AzWebApp.md
ms.openlocfilehash: 102dbd678fe6fe46034a43c46cb713428b8564d5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101893032"
---
# <span data-ttu-id="0c009-101">Stop-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="0c009-101">Stop-AzWebApp</span></span>

## <span data-ttu-id="0c009-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0c009-102">SYNOPSIS</span></span>
<span data-ttu-id="0c009-103">Interrompe um Aplicativo Web do Azure.</span><span class="sxs-lookup"><span data-stu-id="0c009-103">Stops an Azure Web App.</span></span>

## <span data-ttu-id="0c009-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="0c009-104">SYNTAX</span></span>

### <span data-ttu-id="0c009-105">S1</span><span class="sxs-lookup"><span data-stu-id="0c009-105">S1</span></span>
```
Stop-AzWebApp [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0c009-106">S2</span><span class="sxs-lookup"><span data-stu-id="0c009-106">S2</span></span>
```
Stop-AzWebApp [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0c009-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="0c009-107">DESCRIPTION</span></span>
<span data-ttu-id="0c009-108">O cmdlet **Stop-AzWebApp** interrompe um Aplicativo Web do Azure.</span><span class="sxs-lookup"><span data-stu-id="0c009-108">The **Stop-AzWebApp** cmdlet stops an Azure Web App.</span></span>

## <span data-ttu-id="0c009-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0c009-109">EXAMPLES</span></span>

### <span data-ttu-id="0c009-110">Exemplo 1: Parar um aplicativo Web</span><span class="sxs-lookup"><span data-stu-id="0c009-110">Example 1: Stop a Web App</span></span>
```
PS C:\>Stop-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp"
```

<span data-ttu-id="0c009-111">Este comando interrompe o Aplicativo Web chamado ContosoWebApp que pertence ao grupo de recursos chamado Default-Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="0c009-111">This command stops the Web App named ContosoWebApp that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="0c009-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="0c009-112">PARAMETERS</span></span>

### <span data-ttu-id="0c009-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c009-113">-DefaultProfile</span></span>
<span data-ttu-id="0c009-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="0c009-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0c009-115">-Name</span><span class="sxs-lookup"><span data-stu-id="0c009-115">-Name</span></span>
<span data-ttu-id="0c009-116">Nome do WebApp</span><span class="sxs-lookup"><span data-stu-id="0c009-116">WebApp Name</span></span>

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

### <span data-ttu-id="0c009-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0c009-117">-ResourceGroupName</span></span>
<span data-ttu-id="0c009-118">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="0c009-118">Resource Group Name</span></span>

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

### <span data-ttu-id="0c009-119">-WebApp</span><span class="sxs-lookup"><span data-stu-id="0c009-119">-WebApp</span></span>
<span data-ttu-id="0c009-120">Objeto WebApp</span><span class="sxs-lookup"><span data-stu-id="0c009-120">WebApp Object</span></span>

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

### <span data-ttu-id="0c009-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c009-121">CommonParameters</span></span>
<span data-ttu-id="0c009-122">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0c009-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c009-123">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0c009-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c009-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0c009-124">INPUTS</span></span>

### <span data-ttu-id="0c009-125">System.String</span><span class="sxs-lookup"><span data-stu-id="0c009-125">System.String</span></span>

### <span data-ttu-id="0c009-126">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="0c009-126">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="0c009-127">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="0c009-127">OUTPUTS</span></span>

### <span data-ttu-id="0c009-128">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="0c009-128">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="0c009-129">NOTES</span><span class="sxs-lookup"><span data-stu-id="0c009-129">NOTES</span></span>

## <span data-ttu-id="0c009-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0c009-130">RELATED LINKS</span></span>

[<span data-ttu-id="0c009-131">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="0c009-131">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="0c009-132">New-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="0c009-132">New-AzWebApp</span></span>](./New-AzWebApp.md)

[<span data-ttu-id="0c009-133">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="0c009-133">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)

[<span data-ttu-id="0c009-134">Restart-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="0c009-134">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="0c009-135">Start-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="0c009-135">Start-AzWebApp</span></span>](./Start-AzWebApp.md)


