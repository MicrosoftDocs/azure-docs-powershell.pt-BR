---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: D70A61D8-0C9A-4BDB-A546-37C32D25797C
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/start-azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Start-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Start-AzWebApp.md
ms.openlocfilehash: 09c618e617775e0c2bfffab1794f2427f97d811c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93598287"
---
# <span data-ttu-id="15939-101">Start-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="15939-101">Start-AzWebApp</span></span>

## <span data-ttu-id="15939-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="15939-102">SYNOPSIS</span></span>
<span data-ttu-id="15939-103">Inicia um aplicativo Web do Azure.</span><span class="sxs-lookup"><span data-stu-id="15939-103">Starts an Azure Web App.</span></span>

## <span data-ttu-id="15939-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="15939-104">SYNTAX</span></span>

### <span data-ttu-id="15939-105">Eles</span><span class="sxs-lookup"><span data-stu-id="15939-105">S1</span></span>
```
Start-AzWebApp [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="15939-106">S2</span><span class="sxs-lookup"><span data-stu-id="15939-106">S2</span></span>
```
Start-AzWebApp [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="15939-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="15939-107">DESCRIPTION</span></span>
<span data-ttu-id="15939-108">O cmdlet **Start-AzWebApp** inicia um aplicativo Web do Azure.</span><span class="sxs-lookup"><span data-stu-id="15939-108">The **Start-AzWebApp** cmdlet starts an Azure Web App.</span></span>

## <span data-ttu-id="15939-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="15939-109">EXAMPLES</span></span>

### <span data-ttu-id="15939-110">Exemplo 1: iniciar um aplicativo Web</span><span class="sxs-lookup"><span data-stu-id="15939-110">Example 1: Start a Web App</span></span>
```
PS C:\>Start-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp"
```

<span data-ttu-id="15939-111">Esse comando inicia o aplicativo Web chamado ContosoWebApp que pertence ao grupo de recursos chamado Default-Web-Oesteus.</span><span class="sxs-lookup"><span data-stu-id="15939-111">This command starts the Web App named ContosoWebApp that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="15939-112">OS</span><span class="sxs-lookup"><span data-stu-id="15939-112">PARAMETERS</span></span>

### <span data-ttu-id="15939-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15939-113">-DefaultProfile</span></span>
<span data-ttu-id="15939-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="15939-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="15939-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="15939-115">-Name</span></span>
<span data-ttu-id="15939-116">Nome do WebApp</span><span class="sxs-lookup"><span data-stu-id="15939-116">WebApp Name</span></span>

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

### <span data-ttu-id="15939-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="15939-117">-ResourceGroupName</span></span>
<span data-ttu-id="15939-118">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="15939-118">Resource Group Name</span></span>

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

### <span data-ttu-id="15939-119">-WebApp</span><span class="sxs-lookup"><span data-stu-id="15939-119">-WebApp</span></span>
<span data-ttu-id="15939-120">Objeto WebApp</span><span class="sxs-lookup"><span data-stu-id="15939-120">WebApp Object</span></span>

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

### <span data-ttu-id="15939-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15939-121">CommonParameters</span></span>
<span data-ttu-id="15939-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="15939-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15939-123">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="15939-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15939-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="15939-124">INPUTS</span></span>

### <span data-ttu-id="15939-125">System. String</span><span class="sxs-lookup"><span data-stu-id="15939-125">System.String</span></span>

### <span data-ttu-id="15939-126">Microsoft. Azure. Commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="15939-126">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="15939-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="15939-127">OUTPUTS</span></span>

### <span data-ttu-id="15939-128">Microsoft. Azure. Commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="15939-128">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="15939-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="15939-129">NOTES</span></span>

## <span data-ttu-id="15939-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="15939-130">RELATED LINKS</span></span>

[<span data-ttu-id="15939-131">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="15939-131">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="15939-132">New-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="15939-132">New-AzWebApp</span></span>](./New-AzWebApp.md)

[<span data-ttu-id="15939-133">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="15939-133">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)

[<span data-ttu-id="15939-134">Restart-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="15939-134">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="15939-135">Parar-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="15939-135">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)


