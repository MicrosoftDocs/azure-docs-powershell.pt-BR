---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: A12FFDB1-9849-4150-9716-068BE6EFC681
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/stop-azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Stop-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Stop-AzWebApp.md
ms.openlocfilehash: d08303ec0057a42569455c9e52c38e561de73e4d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116017"
---
# <span data-ttu-id="67d02-101">Stop-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="67d02-101">Stop-AzWebApp</span></span>

## <span data-ttu-id="67d02-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="67d02-102">SYNOPSIS</span></span>
<span data-ttu-id="67d02-103">Interrompe um Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="67d02-103">Stops an Azure Web App.</span></span>

## <span data-ttu-id="67d02-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="67d02-104">SYNTAX</span></span>

### <span data-ttu-id="67d02-105">S1</span><span class="sxs-lookup"><span data-stu-id="67d02-105">S1</span></span>
```
Stop-AzWebApp [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="67d02-106">S2</span><span class="sxs-lookup"><span data-stu-id="67d02-106">S2</span></span>
```
Stop-AzWebApp [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="67d02-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="67d02-107">DESCRIPTION</span></span>
<span data-ttu-id="67d02-108">O **cmdlet Stop-AzWebApp** interrompe um Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="67d02-108">The **Stop-AzWebApp** cmdlet stops an Azure Web App.</span></span>

## <span data-ttu-id="67d02-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="67d02-109">EXAMPLES</span></span>

### <span data-ttu-id="67d02-110">Exemplo 1: Parar um Aplicativo Web</span><span class="sxs-lookup"><span data-stu-id="67d02-110">Example 1: Stop a Web App</span></span>
```
PS C:\>Stop-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp"
```

<span data-ttu-id="67d02-111">Esse comando interrompe o Web App chamado ContosoWebApp que pertence ao grupo de recursos chamado Default-Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="67d02-111">This command stops the Web App named ContosoWebApp that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="67d02-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="67d02-112">PARAMETERS</span></span>

### <span data-ttu-id="67d02-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67d02-113">-DefaultProfile</span></span>
<span data-ttu-id="67d02-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="67d02-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="67d02-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="67d02-115">-Name</span></span>
<span data-ttu-id="67d02-116">Nome webapp</span><span class="sxs-lookup"><span data-stu-id="67d02-116">WebApp Name</span></span>

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

### <span data-ttu-id="67d02-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="67d02-117">-ResourceGroupName</span></span>
<span data-ttu-id="67d02-118">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="67d02-118">Resource Group Name</span></span>

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

### <span data-ttu-id="67d02-119">-WebApp</span><span class="sxs-lookup"><span data-stu-id="67d02-119">-WebApp</span></span>
<span data-ttu-id="67d02-120">Objeto WebApp</span><span class="sxs-lookup"><span data-stu-id="67d02-120">WebApp Object</span></span>

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

### <span data-ttu-id="67d02-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67d02-121">CommonParameters</span></span>
<span data-ttu-id="67d02-122">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="67d02-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67d02-123">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="67d02-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67d02-124">Entradas</span><span class="sxs-lookup"><span data-stu-id="67d02-124">INPUTS</span></span>

### <span data-ttu-id="67d02-125">System.String</span><span class="sxs-lookup"><span data-stu-id="67d02-125">System.String</span></span>

### <span data-ttu-id="67d02-126">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="67d02-126">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="67d02-127">Saídas</span><span class="sxs-lookup"><span data-stu-id="67d02-127">OUTPUTS</span></span>

### <span data-ttu-id="67d02-128">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="67d02-128">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="67d02-129">Notas</span><span class="sxs-lookup"><span data-stu-id="67d02-129">NOTES</span></span>

## <span data-ttu-id="67d02-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="67d02-130">RELATED LINKS</span></span>

[<span data-ttu-id="67d02-131">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="67d02-131">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="67d02-132">Novo-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="67d02-132">New-AzWebApp</span></span>](./New-AzWebApp.md)

[<span data-ttu-id="67d02-133">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="67d02-133">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)

[<span data-ttu-id="67d02-134">Restart-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="67d02-134">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="67d02-135">Start-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="67d02-135">Start-AzWebApp</span></span>](./Start-AzWebApp.md)


