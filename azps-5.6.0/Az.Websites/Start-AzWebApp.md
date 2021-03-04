---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: D70A61D8-0C9A-4BDB-A546-37C32D25797C
online version: https://docs.microsoft.com/powershell/module/az.websites/start-azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Start-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Start-AzWebApp.md
ms.openlocfilehash: a05b9ef015d1685e92bc56b0056c9213ff3370ad
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101893038"
---
# <span data-ttu-id="e4859-101">Start-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="e4859-101">Start-AzWebApp</span></span>

## <span data-ttu-id="e4859-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e4859-102">SYNOPSIS</span></span>
<span data-ttu-id="e4859-103">Inicia um Aplicativo Web do Azure.</span><span class="sxs-lookup"><span data-stu-id="e4859-103">Starts an Azure Web App.</span></span>

## <span data-ttu-id="e4859-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="e4859-104">SYNTAX</span></span>

### <span data-ttu-id="e4859-105">S1</span><span class="sxs-lookup"><span data-stu-id="e4859-105">S1</span></span>
```
Start-AzWebApp [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e4859-106">S2</span><span class="sxs-lookup"><span data-stu-id="e4859-106">S2</span></span>
```
Start-AzWebApp [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e4859-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="e4859-107">DESCRIPTION</span></span>
<span data-ttu-id="e4859-108">O cmdlet **Start-AzWebApp** inicia um Aplicativo Web do Azure.</span><span class="sxs-lookup"><span data-stu-id="e4859-108">The **Start-AzWebApp** cmdlet starts an Azure Web App.</span></span>

## <span data-ttu-id="e4859-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e4859-109">EXAMPLES</span></span>

### <span data-ttu-id="e4859-110">Exemplo 1: Iniciar um Aplicativo Web</span><span class="sxs-lookup"><span data-stu-id="e4859-110">Example 1: Start a Web App</span></span>
```
PS C:\>Start-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp"
```

<span data-ttu-id="e4859-111">Este comando inicia o Aplicativo Web chamado ContosoWebApp que pertence ao grupo de recursos chamado Default-Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="e4859-111">This command starts the Web App named ContosoWebApp that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="e4859-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="e4859-112">PARAMETERS</span></span>

### <span data-ttu-id="e4859-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4859-113">-DefaultProfile</span></span>
<span data-ttu-id="e4859-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="e4859-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e4859-115">-Name</span><span class="sxs-lookup"><span data-stu-id="e4859-115">-Name</span></span>
<span data-ttu-id="e4859-116">Nome do WebApp</span><span class="sxs-lookup"><span data-stu-id="e4859-116">WebApp Name</span></span>

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

### <span data-ttu-id="e4859-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e4859-117">-ResourceGroupName</span></span>
<span data-ttu-id="e4859-118">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="e4859-118">Resource Group Name</span></span>

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

### <span data-ttu-id="e4859-119">-WebApp</span><span class="sxs-lookup"><span data-stu-id="e4859-119">-WebApp</span></span>
<span data-ttu-id="e4859-120">Objeto WebApp</span><span class="sxs-lookup"><span data-stu-id="e4859-120">WebApp Object</span></span>

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

### <span data-ttu-id="e4859-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4859-121">CommonParameters</span></span>
<span data-ttu-id="e4859-122">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e4859-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4859-123">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e4859-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4859-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e4859-124">INPUTS</span></span>

### <span data-ttu-id="e4859-125">System.String</span><span class="sxs-lookup"><span data-stu-id="e4859-125">System.String</span></span>

### <span data-ttu-id="e4859-126">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="e4859-126">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="e4859-127">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="e4859-127">OUTPUTS</span></span>

### <span data-ttu-id="e4859-128">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="e4859-128">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="e4859-129">NOTES</span><span class="sxs-lookup"><span data-stu-id="e4859-129">NOTES</span></span>

## <span data-ttu-id="e4859-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e4859-130">RELATED LINKS</span></span>

[<span data-ttu-id="e4859-131">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="e4859-131">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="e4859-132">New-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="e4859-132">New-AzWebApp</span></span>](./New-AzWebApp.md)

[<span data-ttu-id="e4859-133">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="e4859-133">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)

[<span data-ttu-id="e4859-134">Restart-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="e4859-134">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="e4859-135">Stop-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="e4859-135">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)


