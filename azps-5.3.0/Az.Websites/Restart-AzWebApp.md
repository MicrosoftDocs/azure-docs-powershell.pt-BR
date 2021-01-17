---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 297071E5-FC06-4493-BCC2-37D4929E4025
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/restart-azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Restart-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Restart-AzWebApp.md
ms.openlocfilehash: faa3264dbf9fa65a2970f578c635868d185f2ef8
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98427780"
---
# <span data-ttu-id="378fe-101">Restart-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="378fe-101">Restart-AzWebApp</span></span>

## <span data-ttu-id="378fe-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="378fe-102">SYNOPSIS</span></span>
<span data-ttu-id="378fe-103">Reinicia um aplicativo Web do Azure.</span><span class="sxs-lookup"><span data-stu-id="378fe-103">Restarts an Azure Web App.</span></span>

## <span data-ttu-id="378fe-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="378fe-104">SYNTAX</span></span>

### <span data-ttu-id="378fe-105">Eles</span><span class="sxs-lookup"><span data-stu-id="378fe-105">S1</span></span>
```
Restart-AzWebApp [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="378fe-106">S2</span><span class="sxs-lookup"><span data-stu-id="378fe-106">S2</span></span>
```
Restart-AzWebApp [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="378fe-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="378fe-107">DESCRIPTION</span></span>
<span data-ttu-id="378fe-108">O cmdlet **Restart-AzWebApp** interrompe e, em seguida, inicia um aplicativo Web do Azure.</span><span class="sxs-lookup"><span data-stu-id="378fe-108">The **Restart-AzWebApp** cmdlet stops and then starts an Azure Web App.</span></span>
<span data-ttu-id="378fe-109">Se o aplicativo Web estiver em um estado parado, use o cmdlet Start-AzWebApp.</span><span class="sxs-lookup"><span data-stu-id="378fe-109">If the Web App is in a stopped state, use the Start-AzWebApp cmdlet.</span></span>

## <span data-ttu-id="378fe-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="378fe-110">EXAMPLES</span></span>

### <span data-ttu-id="378fe-111">Exemplo 1: reiniciar um aplicativo Web</span><span class="sxs-lookup"><span data-stu-id="378fe-111">Example 1: Restart a Web App</span></span>
```
PS C:\>Restart-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="378fe-112">Esse comando interrompe o aplicativo Web do Azure chamado ContosoSite que pertence ao grupo de recursos chamado Default-Web-Oesteus e, em seguida, o reinicia.</span><span class="sxs-lookup"><span data-stu-id="378fe-112">This command stops the Azure Web App named ContosoSite that belongs to the resource group named Default-Web-WestUS and then restarts it.</span></span>

## <span data-ttu-id="378fe-113">OS</span><span class="sxs-lookup"><span data-stu-id="378fe-113">PARAMETERS</span></span>

### <span data-ttu-id="378fe-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="378fe-114">-DefaultProfile</span></span>
<span data-ttu-id="378fe-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="378fe-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="378fe-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="378fe-116">-Name</span></span>
<span data-ttu-id="378fe-117">Nome do WebApp</span><span class="sxs-lookup"><span data-stu-id="378fe-117">WebApp Name</span></span>

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

### <span data-ttu-id="378fe-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="378fe-118">-ResourceGroupName</span></span>
<span data-ttu-id="378fe-119">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="378fe-119">Resource Group Name</span></span>

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

### <span data-ttu-id="378fe-120">-WebApp</span><span class="sxs-lookup"><span data-stu-id="378fe-120">-WebApp</span></span>
<span data-ttu-id="378fe-121">Objeto WebApp</span><span class="sxs-lookup"><span data-stu-id="378fe-121">WebApp Object</span></span>

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

### <span data-ttu-id="378fe-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="378fe-122">CommonParameters</span></span>
<span data-ttu-id="378fe-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="378fe-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="378fe-124">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="378fe-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="378fe-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="378fe-125">INPUTS</span></span>

### <span data-ttu-id="378fe-126">System. String</span><span class="sxs-lookup"><span data-stu-id="378fe-126">System.String</span></span>

### <span data-ttu-id="378fe-127">Microsoft. Azure. Commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="378fe-127">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="378fe-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="378fe-128">OUTPUTS</span></span>

### <span data-ttu-id="378fe-129">Microsoft. Azure. Commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="378fe-129">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="378fe-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="378fe-130">NOTES</span></span>

## <span data-ttu-id="378fe-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="378fe-131">RELATED LINKS</span></span>

[<span data-ttu-id="378fe-132">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="378fe-132">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="378fe-133">New-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="378fe-133">New-AzWebApp</span></span>](./New-AzWebApp.md)

[<span data-ttu-id="378fe-134">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="378fe-134">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)

[<span data-ttu-id="378fe-135">Start-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="378fe-135">Start-AzWebApp</span></span>](./Start-AzWebApp.md)

[<span data-ttu-id="378fe-136">Parar-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="378fe-136">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)


